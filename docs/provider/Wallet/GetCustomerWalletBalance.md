### Get Customer Wallet Balance

### API Endpoint: `POST /Provider/GetCustomerWalletBalance`


### Description:
This endpoint retrieves the wallet balance of a customer associated with a specific request ID.

#### Query Parameters:
- `id` (int, required): Request ID for fetching customer wallet balance.

#### Response Example:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": 0
}
```

#### Response Parameters:
- `status` (boolean): Indicates the success or failure of the operation.
- `message` (string): A message indicating the outcome of the operation.
- `error` (string): Contains any error details if applicable.
- `Data` (number): The wallet balance of the customer associated with the provided request ID.



