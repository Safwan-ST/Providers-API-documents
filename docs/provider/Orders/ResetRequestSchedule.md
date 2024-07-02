### Reset Request Schedule

**Endpoint**: `POST /Provider/ResetRequestSchedule`

**Description**: Reset the schedule for a specific request.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Query Parameters**:
- `id` (int, required): The ID of the request.
- `date` (date-time, required): The date for the new schedule.
- `hour` (int, required): The hour of the day for the new schedule.
- `minutes` (int, optional): The minutes of the hour for the new schedule (optional).


**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (null): No additional data returned.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العملية بنجاح",
  "error": "",
  "Data": null
}
```
