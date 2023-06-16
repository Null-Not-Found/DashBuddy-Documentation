# DashBuddy-State API endpoints
<table>
  <tr>
    <th>Endpoint</th>
    <th>Params</th>
    <th>Request body</th>
    <th>Response</th>
    <th>description</th>
  </tr>
  <tr>
    <td>/Post</td>
    <td>None</td>
    <td>None</td>
    <td> 
      {
        "Time": Date UTC (time of response),
        "DId": String (the id of the created dashboard)
      }
    </td>
    <td>
      create new dashboard
    </td>
  </tr>
  <tr>
    <td>/Put</td>
    <td>DId: String (Id of dashboard)</td>
    <td>
      {
        "config": { } (config of the dashboard)
      }
    </td>
    <td> 
      {
        "Time": Date UTC (time of response),
        "Status": String (if it succeeded or not)
      }
    </td>
    <td>
      update existing dashboard
    </td>
  </tr>
  <tr>
    <td>/Get</td>
    <td>DId: String (Id of dashboard)</td>
    <td>None</td>
    <td>
      {
        "Config": {} (config of the dashboard)
      }
    </td>
    <td>
      get dashboard
    </td>
  </tr>
 </table>
