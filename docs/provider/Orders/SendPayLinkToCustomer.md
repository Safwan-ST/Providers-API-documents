### Send Pay Link to Customer

**Endpoint**: `POST /Provider/SendPayLinkToCustomer`

**Description**: Sends a payment link to the customer.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Query Parameters**:
- `id` (int, required): The identifier of the customer.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (null): No data is returned for this operation.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```