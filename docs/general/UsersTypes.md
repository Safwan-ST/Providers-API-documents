# Users Types
### API Endpoint: /Provider/Users/UserTypes

**Method**: POST

**Description**: Retrieves the list of user types.

#### Response

**Example Response**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "id": 1,
      "name": "مدير فرع",
      "eng_name": "Branch Manager"
    },
    {
      "id": 2,
      "name": "جودة تشغيل\r\n",
      "eng_name": "Running Quality\r\n"
    },
    {
      "id": 3,
      "name": "مالية",
      "eng_name": "Finance"
    },
    {
      "id": 4,
      "name": "موظف مقدم خدمة ",
      "eng_name": "Service provider employee\r\n"
    }
  ]
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `array` - An array of objects representing the user types with the following properties:
  - `id`: `integer` - The ID of the user type.
  - `name`: `string` - The name of the user type in Arabic.
  - `eng_name`: `string` - The name of the user type in English.

