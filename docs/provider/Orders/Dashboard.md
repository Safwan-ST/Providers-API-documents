### Dashboard Statistics

**Endpoint**: `POST /Provider/Dashboard`

**Description**: Retrieves statistics for the provider's dashboard.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Body**: No request body parameters.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (object): Contains various statistics with the following attributes:
  - `total_follow_requests` (integer): Total number of follow requests.
  - `total_paid_invoices` (string): Total amount paid in invoices.
  - `total_served_requests` (integer): Total number of served requests.
  - `total_served_cars` (integer): Total number of served cars.
  - `today_to_follow` (integer): Number of follow requests today.
  - `no_of_active_branches` (integer): Number of active branches.
  - `no_of_active_technicians` (integer): Number of active technicians.

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العملية بنجاح",
  "error": "",
  "Data": {
    "total_follow_requests": 395,
    "total_paid_invoices": "1945033.8",
    "total_served_requests": 1618,
    "total_served_cars": 555,
    "today_to_follow": 0,
    "no_of_active_branches": 14,
    "no_of_active_technicians": 22
  }
}
```
