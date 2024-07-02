# Managers List
### API Endpoint: /Provider/Users/Managers/List

**Method**: POST

**Description**: Retrieves the list of managers.

#### Response

**Example Response**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "id": 21211,
      "full_name": "test111",
      "is_active": true
    },
    {
      "id": 21238,
      "full_name": "mostafa",
      "is_active": true
    },
    {
      "id": 21337,
      "full_name": "taimoor branch manager",
      "is_active": true
    },
    {
      "id": 21400,
      "full_name": "app taimoor branch manager",
      "is_active": true
    },
    {
      "id": 21414,
      "full_name": "string",
      "is_active": true
    }
  ]
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `array` - An array of objects representing the managers with the following properties:
  - `id`: `integer` - The ID of the manager.
  - `full_name`: `string` - The full name of the manager.
  - `is_active`: `boolean` - Indicates if the manager is active.

