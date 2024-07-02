# Set Employee Banned Working Hours
### API Endpoint: /Provider/User/SetBannedWorkingHours

**Method**: POST

**Description**: Sets the banned working hours for a user.

#### Query Parameters

- `id`: `integer` (required) - The ID of the user whose banned working hours are being set.

#### Request Body

An array of objects, each representing a banned working hour with the following properties:

- `band_year`: `integer` (required) - The year of the banned working hour.
- `band_month`: `integer` (required) - The month of the banned working hour.
- `band_day`: `integer` (required) - The day of the banned working hour.
- `band_hour`: `integer` (required) - The hour of the banned working hour.
- `band_minutes`: `integer` (required) - The minute of the banned working hour.
- `notes`: `string` (optional) - Any additional notes or comments.

**Example Request Body**

```json
[
  {
    "band_year": 2024,
    "band_month": 7,
    "band_day": 2,
    "band_hour": 17,
    "band_minutes": 52,
    "notes": "comments"
  }
]
```

#### Response

**Example Response**

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

