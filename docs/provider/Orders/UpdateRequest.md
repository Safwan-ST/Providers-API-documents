### Update Request

**Endpoint**: `POST /Provider/UpdateRequest`

**Description**: Update an existing service request with new information.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Body Parameters**:
- `id` (int, required): The id of the service request to be updated.
- `note` (string, optional): A note associated with the request.
- `mileAge` (int, optional): The mileage of the vehicle.
- `items` (array of objects, optional): List of items associated with the request. Each object contains:
  - `id` (int): The ID of the item in the request.
  - `item_id` (int): The ID of the item.
  - `item_type_id` (int): The ID of the item type.
  - `brand_id` (int): The ID of the brand.
  - `qty` (int): The quantity of the item.
  - `price` (int): The price of the item.
  - `qty1` (int): The secondary quantity.
  - `price1` (int): The secondary price.
  - `is_check_option` (boolean): Indicates if the item is a check option.
  - `check_optioin_id` (int): The ID of the check option.
- `extra_items` (array of objects, optional): List of extra items associated with the request. Each object contains:
  - `id` (int): The ID of the extra item in the request.
  - `item_id` (int): The ID of the extra item.
  - `qty` (int): The quantity of the extra item.
  - `price` (int): The price of the extra item.
  - `qty1` (int): The secondary quantity.
  - `price1` (int): The secondary price.
  - `description` (string): A description of the extra item.
  - `is_mandatory` (boolean): Indicates if the extra item is mandatory.
- `extra_fees` (array of objects, optional): List of extra fees associated with the request. Each object contains:
  - `id` (int): The ID of the extra fee in the request.
  - `price` (int): The price of the extra fee.
  - `name` (string): The name of the extra fee in Arabic.
  - `eng_name` (string): The name of the extra fee in English.
- `upload_invoice` (boolean, optional): Indicates if the invoice should be uploaded.
- `shipping_courier` (object, optional): Shipping courier details if applicable:
  - `courier_name` (string): The name of the courier.
  - `tracking_number` (string): The tracking number.
  - `tracking_url` (string): The tracking URL.
  - `pickup_address` (string): The pickup address.

**Request Body Example**:
```json
{
  "id": 123,
  "note": "Updated note",
  "mileAge": 15000,
  "items": [
    {
      "id": 1,
      "item_id": 101,
      "item_type_id": 201,
      "brand_id": 301,
      "qty": 2,
      "price": 50,
      "qty1": 1,
      "price1": 25,
      "is_check_option": true,
      "check_optioin_id": 401
    }
  ],
  "extra_items": [
    {
      "id": 1,
      "item_id": 102,
      "qty": 1,
      "price": 75,
      "qty1": 0,
      "price1": 0,
      "description": "Extra service",
      "is_mandatory": true
    }
  ],
  "extra_fees": [
    {
      "id": 1,
      "price": 20,
      "name": "Service Fee",
      "eng_name": "Service Fee"
    }
  ],
  "upload_invoice": true,
  "shipping_courier": {
    "courier_name": "Fast Delivery",
    "tracking_number": "ABC123",
    "tracking_url": "http://trackingurl.com/ABC123",
    "pickup_address": "123 Pickup St"
  }
}
```

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (String): result message.

**Response Example**:
```json
{
  "status": true,
  "message": "Request updated successfully",
  "error": null,
  "Data": "Request updated successfully"
}
'''