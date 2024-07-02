# Find Customer By Phone No
### API Endpoint: /Provider/Orders/Instant/FindCustomerByPhoneNo

**Method**: POST

**Description**: Finds a customer by their phone number.

#### Query Parameters

- `phone`: `string` (required) - The phone number of the customer.

#### Response

**Success Response Example**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "info": {
      "id": 10355,
      "name": "test@gmail.com",
      "eng_name": "test@gmail.com",
      "email": "test@gmail.com",
      "phone": "966010000000"
    },
    "cars": [
      {
        "id": 18778,
        "car_model_id": 103,
        "car_model_name": "فوكس",
        "car_model_eng_name": "Focus",
        "car_vendor_id": 3,
        "car_vendor_name": "فورد",
        "car_vendor_eng_name": "Ford",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      },
      {
        "id": 18911,
        "car_model_id": 195,
        "car_model_name": "اي 5",
        "car_model_eng_name": "A5",
        "car_vendor_id": 11,
        "car_vendor_name": "اودي",
        "car_vendor_eng_name": "Audi",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      },
      {
        "id": 18912,
        "car_model_id": 197,
        "car_model_name": "اي 7",
        "car_model_eng_name": "A7",
        "car_vendor_id": 11,
        "car_vendor_name": "اودي",
        "car_vendor_eng_name": "Audi",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      },
      {
        "id": 18913,
        "car_model_id": 188,
        "car_model_name": "ال اكس",
        "car_model_eng_name": "LX",
        "car_vendor_id": 10,
        "car_vendor_name": "لكزس",
        "car_vendor_eng_name": "Lexus",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      },
      {
        "id": 18914,
        "car_model_id": 185,
        "car_model_name": "اي اس",
        "car_model_eng_name": "ES",
        "car_vendor_id": 10,
        "car_vendor_name": "لكزس",
        "car_vendor_eng_name": "Lexus",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      },
      {
        "id": 18915,
        "car_model_id": 61,
        "car_model_name": "كارينز",
        "car_model_eng_name": "Carens",
        "car_vendor_id": 8,
        "car_vendor_name": "كيا",
        "car_vendor_eng_name": "KIA",
        "car_color_id": 1,
        "car_color_name": "ابيض ",
        "car_color_eng_name": "White",
        "car_models_engine_id": 323,
        "car_models_engine": "4",
        "car_fuel_type_id": 1,
        "car_fuel_type_name": "بنزين",
        "car_fuel_type_eng_name": "Petrol",
        "car_lic_eng_no": null,
        "car_lice_no": "NA"
      }
    ]
  }
}
```

**Not Found Response Example**

```json
{
  "status": false,
  "message": "الزبون غير موجود",
  "error": "",
  "Data": null
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `object | null` - The data returned by the request, which contains:
  - `info`: `object` - Information about the customer, which includes:
    - `id`: `integer` - The ID of the customer.
    - `name`: `string` - The name of the customer.
    - `eng_name`: `string` - The English name of the customer.
    - `email`: `string` - The email of the customer.
    - `phone`: `string` - The phone number of the customer.
  - `cars`: `array` - An array of objects representing the cars of the customer with the following properties:
    - `id`: `integer` - The ID of the car.
    - `car_model_id`: `integer` - The model ID of the car.
    - `car_model_name`: `string` - The model name of the car in Arabic.
    - `car_model_eng_name`: `string` - The model name of the car in English.
    - `car_vendor_id`: `integer` - The vendor ID of the car.
    - `car_vendor_name`: `string` - The vendor name of the car in Arabic.
    - `car_vendor_eng_name`: `string` - The vendor name of the car in English.
    - `car_color_id`: `integer` - The color ID of the car.
    - `car_color_name`: `string` - The color name of the car in Arabic.
    - `car_color_eng_name`: `string` - The color name of the car in English.
    - `car_models_engine_id`: `integer` - The engine ID of the car model.
    - `car_models_engine`: `string` - The engine type of the car model.
    - `car_fuel_type_id`: `integer` - The fuel type ID of the car.
    - `car_fuel_type_name`: `string` - The fuel type name of the car in Arabic.
    - `car_fuel_type_eng_name`: `string` - The fuel type name of the car in English.
    - `car_lic_eng_no`: `string | null` - The license number in English (if any).
    - `car_lice_no`: `string` - The license number.

