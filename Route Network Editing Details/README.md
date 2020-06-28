Route Network Editing Commands and Events (Happy Paths)
==============================


Use Case 1: New lonely route segment digitized by user
-------------------
The user draws a new route segment in the map, that don’t start or end at any existing route nodes or crosses any existing route segments

![image text](Images/lonely-route-segment-digitized.png)

Now, because the route network is mapped to a graph (vertices and edges), the system must help the user create eventually missing nodes.

In this case, both ends of the drawn route segment in not snapped to any existing route nodes, so two new route nodes must be added to the route network event topic before the route segment drawn by the user can be added.

**Events emitted to event.route-network topic:**

```yaml
{
  "EventType": "RouteNodeAdded",
  "EventId": "6f479ac9-bb93-4d88-af6c-4f3a7a5ccb02",
  "EventTs": "2020-06-28T10:53:01Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C1",
  "NodeId": "N1",
  "Geometry": "[578800, 6179700]"
}
```

```yaml
{
  "EventType": "RouteNodeAdded",
  "EventId": "2559f041-14e7-4856-80f3-3b96e389e0e5",
  "EventTs": "2020-06-28T10:53:02Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C1",
  "NodeId": "N2",
  "Geometry": "[578810,6179700]"
}
```

```yaml
{
  "EventType": "RouteSegmentAdded",
  "EventId": "957f670e-9213-4b17-aa8b-42bbddcabf68",
  "EventTs": "2020-06-28T10:53:03Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C1",
  "SegmentId": "S1",
  "FromNodeId": "N1",
  "ToNodeId": "N2",
  "Geometry": "[[578800, 6179700],[578810,6179700]]"
}
```
The id's "C1", "N1", "N2" and "S1" will be uuid's in the real system. The shorthand id's are used to make the examples easier to follow.

Notice that the id: C1 is the same in all three events. This is important, so that route network event consumers know that the three events are the results of the "NewRouteSegmentDigitizedByUser" command with id C1. Especially when we get to splitting segments, this is very important information for some of the consumers.

Also notice from the events shown above, that the order is important.
A segment must never be added to the route network event topic, unless the from and to node exists in the topic beforehand.
This makes it easy for consumers to work with the events in the topic - i.e. a consumer that maintain a graph in a graph database.
Applying the events in the route network topic to a graph in order, and the graph is guaranteed to be valid.

If the edit command of the user cannot be translated into one or more route network events that individually can be applied to a graph with success, then the events must not be added to the topic!

Use Case 2: New route segment digitized from/to an existing node by user
-------------------
The user draws a new route segment where one end is snapped to an existing route node.

![image text](Images/segment-digitized-from-existing-node.png)

Again the system has to help the user, because graph-wise it's illegal to add an edge (mapped to route segment) without having two vertices (mapped to route nodes). So we need to add the missing node first.

**Events emitted to event.route-network topic:**

```yaml
{
  "EventType": "RouteNodeAdded",
  "EventId": "f4bffaf5-c772-4507-91ed-b3b80632aa71",
  "EventTs": "2020-06-28T10:54:01Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C2",
  "NodeId": "N3",
  "Geometry": "[578820,6179690]"
}
```

```yaml
{
  "EventType": "RouteSegmentAdded",
  "EventId": "03de6f0d-6660-4a21-bb11-20c406a15c37",
  "EventTs": "2020-06-28T10:53:02Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C2",
  "SegmentId": "S2",
  "FromNodeId": "N2",
  "ToNodeId": "N3",
  "Geometry": "[[578810,6179700],[578820,6179690]]"
}
```

Notice that the command type is the same as the previous use case, but the command id has changed.

In this example we can derive that the user has drawn a polyline starting at N2 and down to N3, because the from node of the new segment is pointing to N2. If the user had started drawing from where N3 is located and to up to N2, then the from and to node would have been swapped.


Use Case 3: New route segment digitized between two existing nodes
-------------------
The user draws a new route segment between two existings nodes.

![image text](Images/segment-digitized-between-existing-nodes.png)

Here the system don't have to add any additional objects.

**Events emitted to event.route-network topic:**

```yaml
{
  "EventType": "RouteSegmentAdded",
  "EventId": "3c80690f-6179-4e8e-b358-8faedd16f2e4",
  "EventTs": "2020-06-28T10:54:01Z",
  "CmdType": "NewRouteSegmentDigitizedByUser",
  "CmdId": "C3",
  "SegmentId": "S3",
  "FromNodeId": "N2",
  "ToNodeId": "N3",
  "Geometry": "[[578810,6179700], more intermediate coordinates,[578820,6179690]]"
}
```

