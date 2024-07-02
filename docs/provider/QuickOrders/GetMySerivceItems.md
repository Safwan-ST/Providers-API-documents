# Get My Serivce Items
### API Endpoint: /Provider/Orders/Instant/GetMySerivceItems

**Method**: GET

**Description**: Retrieves service items and service fees based on the provided service ID and car model ID.

#### Query Parameters

- `service_id`: `integer` (required) - The ID of the service.
- `car_model_id`: `integer` (required) - The ID of the car model.

#### Response

**Success Response Example**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "service_items": [
      {
        "service_brand_id": 75,
        "brand_name": "تلميع سيارات ",
        "brand_eng_name": "PolishWash",
        "items": [
          {
            "id": 10126,
            "name": "‎تلميع داخلي ",
            "eng_name": "internal polish",
            "price": 1.51
          },
          {
            "id": 10127,
            "name": "تلميع داخلي وخارجي ",
            "eng_name": "external and internal polish",
            "price": 2.51
          },
          {
            "id": 10128,
            "name": "‎تلميع خارجي ",
            "eng_name": "external polish",
            "price": 3.51
          }
        ]
      }
    ],
    "service_fees": [
      {
        "id": 2907,
        "name": "تلميع السيارات رسوم إضافية",
        "eng_name": "Car Polishing additional fee",
        "price": 3.25
      },
      {
        "id": 2908,
        "name": "رسوم خدمة تلميع السيارات",
        "eng_name": "Car Polishing service charges",
        "price": 3.75
      }
    ]
  }
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `object` - The data returned by the request, which contains:
  - `service_items`: `array` - An array of objects representing the service items, each with the following properties:
    - `service_brand_id`: `integer` - The ID of the service brand.
    - `brand_name`: `string` - The name of the service brand in Arabic.
    - `brand_eng_name`: `string` - The name of the service brand in English.
    - `items`: `array` - An array of objects representing the items under the service brand, each with the following properties:
      - `id`: `integer` - The ID of the item.
      - `name`: `string` - The name of the item in Arabic.
      - `eng_name`: `string` - The name of the item in English.
      - `price`: `float` - The price of the item.
  - `service_fees`: `array` - An array of objects representing the service fees, each with the following properties:
    - `id`: `integer` - The ID of the service fee.
    - `name`: `string` - The name of the service fee in Arabic.
    - `eng_name`: `string` - The name of the service fee in English.
    - `price`: `float` - The price of the service fee.

