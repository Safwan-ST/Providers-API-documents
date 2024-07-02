
### Close Request Endpoint

#### Endpoint
```
POST /Provider/CloseRequest
```

#### Query Parameters
- `id`: *(integer, required)* - Request ID to be closed.

#### Request Body
This endpoint does not require a request body.

#### Response Example
```json
{
  "status": true,
  "message": "تمت العملية بنجاح",
  "error": "",
  "Data": null
}
```

#### Response Parameters
- `status`: *(boolean)* - Indicates whether the operation was successful.
- `message`: *(string)* - Describes the status of the operation in Arabic.
- `error`: *(string)* - Any error details, if applicable (currently empty in successful cases).
- `Data`: *(null)* - Placeholder for any additional data returned (currently null).
