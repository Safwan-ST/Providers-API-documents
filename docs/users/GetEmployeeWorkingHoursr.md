# Get Employee Working Hours

### API Endpoint: /Provider/User/GetWorkingHours

**Method**: POST

**Description**: Retrieves the working hours for a user.

#### Query Parameters

- `id`: `integer` (required) - The ID of the user whose working hours are being retrieved.


**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `object` - The working hours data.
  - `unit`: `string` - The time unit for the working hours.
  - `data`: `array of objects` - The list of working hours data.
    - `day_name`: `string` - The name of the day.
    - `day_no`: `integer` - The day number (1 for Monday, 2 for Tuesday, etc.).
    - `zones`: `array of objects` - The list of zones.
      - `zone_id`: `integer` - The ID of the zone.
      - `zone_name`: `string` - The name of the zone.
      - `zone_eng_name`: `string` - The English name of the zone.
    - `hours`: `array of objects` - The list of hours for the working day.
      - `hour`: `integer` - The hour (0-23) of the working time.
      - `minute`: `integer` or `null` - The minute (0-59) of the working time or `null` if not specified.

#### Response

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "unit": "15 minutes",
    "data": [
      {
        "day_name": "Monday",
        "day_no": 3,
        "zones": [
          {
            "zone_id": 9,
            "zone_name": "R1",
            "zone_eng_name": "R1"
          },
        ],
        "hours": [
          {
            "hour": 16,
            "minute": 30
          }
        ]
      },
      {
        "day_name": "Saturday",
        "day_no": 1,
        "zones": [
          {
            "zone_id": 9,
            "zone_name": "R1",
            "zone_eng_name": "R1"
          },
        ],
        "hours": [
          {
            "hour": 1,
            "minute": 15
          },
        ]
      }
    ]
  }
}
```


