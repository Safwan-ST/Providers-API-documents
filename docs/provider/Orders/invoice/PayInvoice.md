# Pay Invoice

### API Endpoint: `/Provider/PayInvoice`

### Endpoint Description:
This endpoint allows the provider to process a payment for an invoice

#### Method:
POST

#### Query Parameters:
- `id` (int, required): ID of the invoice to pay.
- `coupon_name` (string): Optional. Name of the coupon applied.
- `cash_amount` (double): Amount paid in cash.

#### Response Example:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```

#### Response Parameters:
- `status` (boolean): Indicates the success or failure of the payment operation.
- `message` (string): A message indicating the outcome of the payment operation.
- `error` (string): Contains any error details if applicable.
- `Data` (null): Additional data related to the payment operation, if any.



