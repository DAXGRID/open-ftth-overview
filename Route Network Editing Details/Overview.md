<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 1: New lonely route segment digitized by user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/lonely-route-segment-digitized.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded (N1)</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteNodeAdded (N2)</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S1)</td>
            <td></td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 2: New route segment digitized from/to an existing node by user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-digitized-from-existing-node.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded (N3)</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S2)</td>
            <td></td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 3: New route segment digitized between two existing nodes</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-digitized-between-existing-nodes.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteSegmentAdded (S3)</td>
            <td></td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 4: Existing route segment splitted by a new route node drawn by the user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-splitted-by-node.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N4)</td>
            <td></td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S4)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S5)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S1)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
</table>

<br><br><br><br>

<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 5: Existing route segment split by one end belonging to a new segment drawn by the user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-splitted-by-segment-1.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N5)</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S7)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S8)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S2)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded (N6)</td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S6)</td>
            <td></td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
          <td colspan=3 width=1000>
            <h2>UC 6: Existing route segment splitted by both end belonging to a new segment drawn by the user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-splitted-by-segment-2.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N7)</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S10)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S11)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S6)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N8)</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S12)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S13)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S11)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>                
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteSegmentAdded (S9)</td>
            <td></td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 7: Two existing route segments are splitted by ends belonging to a new segment drawn by the user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-splitted-by-segment-3.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N7) </td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S10)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S11)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S6)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded (N8)</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S12)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S13)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S3)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>                
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteSegmentAdded (S9)</td>
            <td></td>
        </tr>
</table>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 8: New segment split due to intersecting nodes</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-split-due-to-nodes.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded (N7) </td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S9)</td>
            <td>Insert segment</td>
        </tr>
        <tr>
            <td rowspan=3>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteSegmentAdded (S10)</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S11)</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved (S9)</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>                
</table>


<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 9: Route segment deleted by user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-deleted-1.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=1>RouteSegmentDeletedByUser</td>
            <td>RouteSegmentMarkedForDeletion (S10) </td>
            <td></td>
        </tr>
</table>


<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 10: Route node deleted by user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/node-deleted-1.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=1>RouteNodeDeletedByUser</td>
            <td>RouteNodeMarkedForDeletion (N6) </td>
            <td></td>
        </tr>
</table>


<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 11: Segment end disconnected from node by user</h2>
            Notice that the user change segment connectivity by means of modifying its geometry.
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-end-disconnected-1.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>RouteSegmentConnetivityChangedByUser</td>
            <td>RouteNodeAdded (N9) </td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S14)</td>
            <td>Insert a clone of S11 with new geometry and connectivity (connected to N5 and N9)</td>
        </tr>
        <tr>
            <td>RouteSegmentMarkedForDeletion (S11)</td>
            <td>Revert geometry to how the segment looked like before user edited it, and mark it to be deleted in the database</td>
        </tr>
</table>

<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 12: Segment disconnected from both of its nodes by user</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-end-disconnected-2.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>RouteSegmentConnetivityChangedByUser</td>
            <td>RouteNodeAdded (N9) </td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteNodeAdded (N10)</td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded (S14)</td>
            <td>Insert a clone of S11 with new geometry and connectivity (connected to N9 and N10)</td>
        </tr>
        <tr>
            <td>RouteSegmentMarkedForDeletion (S11)</td>
            <td>Revert geometry to how the segment looked like before user edited it, and mark it to be deleted in the database</td>
        </tr>
</table>


<br><br><br><br>

<table>
        <tr>
         <td colspan=3 width=1000>
            <h2>UC 13: Segment end disconnected and reconnected to another node</h2>
            <img width=800 src="https://raw.githubusercontent.com/DAXGRID/open-ftth-overview/master/Route%20Network%20Editing%20Details/Images/segment-disconnect-reconnect-to-node.png">
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>RouteSegmentConnetivityChangedByUser</td>
            <td>RouteSegmentAdded (S15) </td>
            <td>Insert a clone of S4 but with new geometry and connectivity (connected to N4 and N9)</td>
        </tr>
        <tr>
            <td>RouteSegmentMarkedForDeletion (S4)</td>
            <td>Revert geometry to how the segment looked like before user edited it, and mark it to be deleted in the database</td>
        </tr>
        <tr>
            <td>RouteNodeMarkedForDeletion (N1)</td>
            <td>Mark N1 to be deleted, but only of degree = 0 (no long connected to any edges) and name and kind is null</td>
        </tr>
</table>





















