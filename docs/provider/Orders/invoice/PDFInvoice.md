### Generate PDF Invoice

**Endpoint**: `POST /Provider/PDFInvoice`

**Description**: Generate a PDF invoice for a given ID.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Query Parameters**:
- `id` (int, required): The ID of the invoice.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (string): File bytes containing the PDF invoice.

**Response Example**:
```json
{
    "status": true,
    "message": "تمت العملية بنجاح",
    "error": "",
    "Data": "JVBERi0xLjQKJeLjz9MKMiAwIG9iago8PC9..."
}
```
