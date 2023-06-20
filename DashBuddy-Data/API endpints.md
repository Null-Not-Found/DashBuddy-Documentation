# DashBuddy-Data API endpoints
<table>
  <tr>
    <th>Endpoint</th>
    <th>Params</th>
    <th>Request body</th>
    <th>Response</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>/GraphQL</td>
    <td>none</td>
    <td>GraphQL Query</td>
    <td>
      JSON object
    </td>
    <td>
      Main endpoint for getting the data dynamically
    </td>
  <tr>
    <td>/brands/Get</td>
    <td>None</td>
    <td>None</td>
    <td>
      An array of brands:
      [
        {
          "id": string,
          "name": string,
          "description: string",
          "owner_id": string,
          "updated_at": Date,
          "deleted_at": Date,
          "created_at": Date,
        }
      ]
    </td>
    <td>
      Gets all brands from the database.
    </td>
  </tr>
  <tr>
    <td>/brands/Get/:id</td>
    <td>id: String (Id of brand)</td>
    <td>
      None
    </td>
    <td> 
        {
          "id": string,
          "name": string,
          "description: string",
          "owner_id": string,
          "updated_at": Date,
          "deleted_at": Date,
          "created_at": Date,
        }
    </td>
    <td>
      Gets a single brand from the database by ID
    </td>
  </tr>
  <tr>
    <td>/products/Get</td>
    <td>None</td>
    <td>None</td>
    <td>
      an array of products:
      [
        {
          "id": string,
          "name": string,
          "brand": string,
          "model": string,
          "owner_id": string,
          "fields": ProductField[]
            {
              "id": string,
              "attribute": string,
              "value": any,
              "updated_at": Date,
              "deleted_at": Date,
              "created_at": Date,
            }
          "gtin": string,
          "product_statuses_id": string,
          "created_at": Date,
          "deleted_at": Date,
          "updated_at": Date,
        }
      ]
    </td>
    <td>
      Gets all products from the database
    </td>
  </tr>
    <tr>
    <td>/products/Get/:id</td>
    <td>id: String (Id of product)</td>
    <td>None</td>
    <td>
        {
          "id": string,
          "name": string,
          "brand": string,
          "model": string,
          "owner_id": string,
          "fields": ProductField[]
            {
              "id": string,
              "attribute": string,
              "value": any,
              "updated_at": Date,
              "deleted_at": Date,
              "created_at": Date,
            }
          "gtin": string,
          "product_statuses_id": string,
          "created_at": Date,
          "deleted_at": Date,
          "updated_at": Date,
        }
    </td>
    <td>
      Gets a single product from the database by ID
    </td>
  </tr>
 </table>
