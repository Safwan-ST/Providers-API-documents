# Set Working Hours

### API Endpoint: /Provider/User/SetWorkingHours

**Method**: POST

**Description**: Sets the working hours for a user.

#### Request Body

```json
{
  "user_id": 21414,
  "data": [
    {
      "day_no": 1,
      "zones": [
        11
      ],
      "hours": [
        {
          "hour": 5,
          "minute": 30
        }
      ]
    }
  ]
}
```

**Parameters**:

- `user_id`: `integer` (required) - The ID of the user whose working hours are being set.
- `data`: `array of objects` (required) - The list of working hours data for the user.
  - `day_no`: `integer` (required) - The day number (1 for Monday, 2 for Tuesday, etc.).
  - `zones`: `array of integers` (required) - The list of zone IDs for the working day.
  - `hours`: `array of objects` (required) - The list of hours for the working day.
    - `hour`: `integer` (required) - The hour (0-23) of the working time.
    - `minute`: `integer` (required) - The minute (0-59) of the working time.

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `null` - No additional data is returned.

#### Response

```json
{
  "status": true,
  "message": "لقد تمت المهمه بنجاح",
  "error": "",
  "Data": null
}
```


