

# Retrieve Provider Schedule Calendar List

**Endpoint**: `POST /Provider/ScheduleCalendarList`

**Description**: Retrieves the schedule calendar for a provider based on the specified parameters.

**Query Parameters**:
- `id` (int, required): The identifier of the provider.

**Response Parameters**:
- `status` (boolean): Indicates if the operation was successful (`true` or `false`).
- `message` (string): Describes the outcome of the operation.
- `error` (string): Provides details of any errors encountered during the operation.
- `Data` (array): Contains an array of schedule information for each date.
  - `date` (string): The date in format "M/D/YYYY".
  - `dayname` (string): The name of the day in Arabic.
  - `hours` (array): An array of objects representing available hours for appointments.
    - `provider_id` (int): The ID of the provider.
    - `branch_id` (int): The ID of the branch.
    - `user_id` (int): The ID of the user.
    - `hour` (int): The hour of the available time slot.
    - `minute` (string): The minute of the available time slot.

#### Example

**Params**:
```json
{
    "id": 14765
}
```

**Response**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "date": "7/10/2024",
      "dayname": "الأربعاء",
      "hours": [
        {
          "provider_id": 10031,
          "branch_id": 82,
          "user_id": 20206,
          "hour": 0,
          "minute": "00"
        }
      ]
    },
    {
      "date": "7/11/2024",
      "dayname": "الخميس",
      "hours": [
        {
          "provider_id": 10031,
          "branch_id": 82,
          "user_id": 20206,
          "hour": 0,
          "minute": "00"
        }
      ]
    }
  ]
}
```