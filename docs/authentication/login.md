Here's the Markdown documentation for the `POST /Auth/Token/Authenticate` API:

### Authenticate User

**Endpoint**: `POST /Auth/Token/Authenticate`

**Description**: Authenticates a user and retrieves an access token for further API requests.

**Request Body Parameters**:
- `Username` (required): The username of the user.
- `Password` (required): The password of the user.

**Response Parameters**:
- `status`: Indicates if the operation was successful (`true` or `false`).
- `message`: Describes the outcome of the operation.
- `error`: Provides details of any errors encountered during the operation.
- `Data`: Contains the authentication token (`JWT`) if the authentication was successful.

#### Example

**Request**:
```json
{
  "Username": "sayaratech",
  "Password": "sayaratech"
}
```

**Response**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6InNheWFyYXRlY2giLCJBZ2VuY3lfSUQiOiIxMDAzMSIsIlVzZXJJZCI6IjIwMTMzIiwicm9sZSI6IlByb3ZpZGVycyIsIm5iZiI6MTcxOTc2NDM4NSwiZXhwIjoxNzE5NzcxNTg1LCJpYXQiOjE3MTk3NjQzODUsImlzcyI6Imh0dHBzOi8vc2F5YXJhdGVjaC5jb20vIiwiYXVkIjoiaHR0cHM6Ly9zYXlhcmF0ZWNoLmNvbS8ifQ.OZy7W9tEiAJkUn9MEPHLHWj2Vv6qYGhlSI0TeKivJkE"
}
```

