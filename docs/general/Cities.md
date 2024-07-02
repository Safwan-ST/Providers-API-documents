## General Endpoints

### Get Cities

**Endpoint**: `GET /Provider/Cities/List`

**Description**: This endpoint retrieves a list of cities where services are available.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (array): An array of cities, where each object contains:
  - `city_id` (int): identifier for the city.
  - `name` (string): The name of the city in Arabic.
  - `eng_name` (string): The name of the city in English.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "city_id": 1,
      "name": "الرياض",
      "eng_name": "Riyadh"
    },
    {
      "city_id": 3,
      "name": "حائل",
      "eng_name": "Hail"
    },
    {
      "city_id": 4,
      "name": "الدمام ",
      "eng_name": "Dammam"
    },
    {
      "city_id": 5,
      "name": "حائل",
      "eng_name": "Hail"
    },
    {
      "city_id": 6,
      "name": "جده",
      "eng_name": "جده"
    },
    {
      "city_id": 7,
      "name": "المدينة المنورة",
      "eng_name": "Medina"
    },
    {
      "city_id": 8,
      "name": "جده ",
      "eng_name": "Jeddah"
    },
    {
      "city_id": 9,
      "name": "الطائف",
      "eng_name": "Taif"
    },
    {
      "city_id": 10,
      "name": "بريده",
      "eng_name": "buraydah"
    }
  ]
}
```