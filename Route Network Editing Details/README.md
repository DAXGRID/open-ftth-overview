Route Network Editing Commands and Events
==============================


Use Case 1: New Route Segment Digitized by User
-------------------
The user draws a new route segment in the map, that don’t start or end at any existing route nodes or crosses any existing route segments

![image text](Images/lonely-route-segment-digitized.png)

Now, because the route network is mapped to a graph (vertices and edges), the system must help the user create eventually missing nodes.
In this case, both ends of the drawn route segment in not snapped to any existing route nodes, so two new route nodes must be added to the route network event topic before the route segment draw by the user is added.

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

