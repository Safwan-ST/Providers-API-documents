# Get Employee Banned Working Hours

### API Endpoint: /Provider/User/GetBannedWorkingHours

**Method**: POST

**Description**: Retrieves the banned working hours for a user.

#### Query Parameters

- `id`: `integer` (required) - The ID of the user whose banned working hours are being retrieved.


**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `array` - An array of objects representing the banned working hours with the following properties:
  - `ban_date`: `string` - The banned date and time in ISO 8601 format.
  - `ban_date_time`: `string` - The banned date and time in ISO 8601 format.
  - `ban_hour`: `integer` - The banned hour.
  - `ban_minute`: `integer` - The banned minute.
  - `ban_day`: `integer` - The banned day.
  - `ban_month`: `integer` - The banned month.
  - `ban_year`: `integer` - The banned year.
  - `notes`: `string` - Any additional notes or comments.
  

#### Response

**Example Response**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "ban_date": "2024-08-02T17:52:00",
      "ban_date_time": "2024-08-02T17:52:00",
      "ban_hour": 17,
      "ban_minute": 52,
      "ban_day": 2,
      "ban_month": 8,
      "ban_year": 2024,
      "notes": "comments"
    }
  ]
}
```



