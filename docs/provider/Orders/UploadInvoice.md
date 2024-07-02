### Upload Invoice

**Endpoint**: `POST /Provider/UploadInvoice`

**Description**: Upload an invoice for a service request.

**Authentication**: Requires Bearer Token Authentication in the header.

**Query Parameters**:
- `id` (int, required): The ID of the service request for which the invoice is being uploaded.

**Request Example**:
```
POST /Provider/UploadInvoice?id=123

```

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (null): No data is returned in the response.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```

