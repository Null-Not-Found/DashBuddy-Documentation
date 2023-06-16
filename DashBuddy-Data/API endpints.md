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
    <td>brands/Get</td>
    <td>None</td>
    <td>None</td>
    <td>
      Array of brands:
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
      Gets all brands from database.
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
      Gets a single brand from database by ID
    </td>
  </tr>
  <tr>
    <td>products/Get</td>
    <td>None</td>
    <td>None</td>
    <td>
      Array of products:
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
      Gets all products from database
    </td>
  </tr>
    <tr>
    <td>products/Get/:id</td>
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
      Gets single product from database by ID
    </td>
  </tr>
 </table>
