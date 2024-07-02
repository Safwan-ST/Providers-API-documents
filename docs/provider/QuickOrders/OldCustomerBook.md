# Old Customer Book
### API Endpoint: /api/Provider/Orders/Instant/Book

**Method**: POST

**Description**: Books an instant order with the provided details id the Provider Is Old.

#### Request Body

```json
{
  "MasterServiceID": 4,
  "phone": "312012012",
  "Car": {
    "Car_Vendor_id": 1,
    "Car_Model_id": 11,
    "Car_Color_id": 1,
    "Model_Year": 2023,
    "Board_No": "9873897432987493827",
    "Car_Lic_No": "L S T 111",
    "Last_KMs_Usages": 0,
    "Car_Models_Engine_id": 323,
    "Car_Fule_Type_id": 1
  },
  "BookingDate": "2024-06-20",
  "BookingHour": 13,
  "BookingMinutes": 0,
  "Products": [
    {
      "id": 65,
      "qty": 1,
      "total": 1,
      "UnitPrc": 1,
      "PrdctBrandID": 0,
      "PrdctBrand": "",
      "PrdctOrigin": "",
      "PrdctGuarantee": "",
      "PrdctFullSize": "",
      "PrdctPayloadSmbl": "",
      "PrdtcName": "",
      "IsServiceFees": false
    }
  ],
  "CouponId": null,
  "Notes": "",
  "BrandId": null,
  "attached_images": [],
  "lat": "24.798006438761767",
  "lng": "46.65681796473758"
}
```

**Request Body Parameters**:

- `MasterServiceID`: `integer` (required) - The ID of the master service.
- `phone`: `string` (required) - The phone number of the customer.
- `Car`: `object` (required) - Details of the car, including:
  - `Car_Vendor_id`: `integer` (required) - The ID of the car vendor.
  - `Car_Model_id`: `integer` (required) - The ID of the car model.
  - `Car_Color_id`: `integer` (required) - The ID of the car color.
  - `Model_Year`: `integer` (required) - The model year of the car.
  - `Board_No`: `string` (required) - The board number of the car.
  - `Car_Lic_No`: `string` (required) - The license number of the car.
  - `Last_KMs_Usages`: `integer` (required) - The last kilometers usage of the car.
  - `Car_Models_Engine_id`: `integer` (required) - The ID of the car's engine model.
  - `Car_Fule_Type_id`: `integer` (required) - The ID of the car's fuel type.
- `BookingDate`: `string` (required) - The booking date in YYYY-MM-DD format.
- `BookingHour`: `integer` (required) - The booking hour.
- `BookingMinutes`: `integer` (required) - The booking minutes.
- `Products`: `array` (required) - An array of product objects, each with:
  - `id`: `integer` (required) - The ID of the product.
  - `qty`: `integer` (required) - The quantity of the product.
  - `total`: `float` (required) - The total price of the product.
  - `UnitPrc`: `float` (required) - The unit price of the product.
  - `PrdctBrandID`: `integer` (optional) - The product brand ID.
  - `PrdctBrand`: `string` (optional) - The product brand name.
  - `PrdctOrigin`: `string` (optional) - The product origin.
  - `PrdctGuarantee`: `string` (optional) - The product guarantee.
  - `PrdctFullSize`: `string` (optional) - The product full size.
  - `PrdctPayloadSmbl`: `string` (optional) - The product payload symbol.
  - `PrdtcName`: `string` (optional) - The product name.
  - `IsServiceFees`: `boolean` (optional) - Indicates if the product is a service fee.
- `CouponId`: `integer` (optional) - The coupon ID.
- `Notes`: `string` (optional) - Additional notes.
- `BrandId`: `integer` (optional) - The brand ID.
- `attached_images`: `array` (optional) - An array of attached images.
- `lat`: `string` (required) - The latitude of the booking location.
- `lng`: `string` (required) - The longitude of the booking location.

#### Response

**Success Response Example**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `null` - No additional data is returned.

