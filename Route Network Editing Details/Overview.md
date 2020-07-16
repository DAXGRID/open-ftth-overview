<table>
        <tr>
          <td colspan=3>
            <img width=1000/>
            <h2>UC 1: New lonely route segment digitized by user</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteNodeAdded</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td></td>
        </tr>
</table>


<table>
        <tr>
          <td colspan=3>
          <img width=1000/>
            <h2>UC 2: New route segment digitized from/to an existing node by user</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node in database</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td></td>
        </tr>
</table>

<table>
        <tr>
          <td colspan=3>
          <img width=1000/>
            <h2>UC 3: New route segment digitized between two existing nodes</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=3>NewRouteSegmentDigitizedByUser</td>
            <td>RouteSegmentAdded</td>
            <td></td>
        </tr>
</table>

<table>
        <tr>
          <td colspan=3>
          <img width=1000/>
            <h2>UC 4: Existing route segment splitted by a new route node drawn by the user</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded</td>
            <td></td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
</table>


<table>
        <tr>
          <td colspan=3>
          <img width=1000/>
            <h2>UC 5: Existing route segment split by one end belonging to a new segment drawn by the user</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td></td>
        </tr>
</table>


<table>
        <tr>
          <td colspan=3>
          <img width=1000/>
            <h2>UC 6: Existing route segment splitted by both end belonging to a new segment drawn by the user</h2>
           </td>
        </tr>
        <tr>
            <td width=354><b>Command(s)</b></td>
            <td width=354><b>Event(s)</b></td>
            <td width=354><b>Database operation(s)</b></td>
        </tr>
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>        
        <tr>
            <td rowspan=4>ExistingRouteSegmentSplittedByUser</td>
            <td>RouteNodeAdded</td>
            <td>Insert missing node (that's splitting the segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (first part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentAdded</td>
            <td>Insert segment (second part of splitted segment)</td>
        </tr>
        <tr>
            <td>RouteSegmentRemoved</td>
            <td>Delete (the splitted) segment from database</td>
        </tr>                
        <tr>
            <td rowspan=2>NewRouteSegmentDigitizedByUser</td>
            <td>RouteSegmentAdded</td>
            <td></td>
        </tr>
</table>




















