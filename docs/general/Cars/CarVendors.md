## General Endpoints

### Get Cars Vendors List

**Endpoint**: `POST /Provider/CarVendors/List`

**Description**: This endpoint retrieves a list of car vendors.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (array): An array of car vendors, where each object contains:
  - `car_vendor_id` (int): identifier for the car vendor.
  - `name` (string): The name of the car vendor in Arabic.
  - `eng_name` (string): The name of the car vendor in English.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "car_vendor_id": 1,
      "name": "تويوتا",
      "eng_name": "Toyota"
    },
    {
      "car_vendor_id": 2,
      "name": "نيسان",
      "eng_name": "Nissan"
    }
  ]
}
```