
# Retrieve Provider Profile

**Endpoint**: `POST /Provider/Profile`

**Description**: Retrieves the profile information of the logged-in provider.

**Response Parameters**:
- `status` (boolean): Indicates if the operation was successful (`true` or `false`).
- `message` (string): Describes the outcome of the operation.
- `error` (string): Provides details of any errors encountered during the operation.
- `Data` (object): Contains the profile information of the provider.
  - `provider_id` (int or null): The identifier of the provider (nullable).
  - `profile_id` (int): The profile ID of the provider.
  - `name` (string): The name of the provider.
  - `mobile` (string): The mobile number of the provider.
  - `email` (string): The email address of the provider.
  - `username` (string): The username of the provider.
  - `join_date` (string or null): The join date of the provider (nullable).
  - `id_number` (string or null): The ID number of the provider (nullable).
  - `branch_id` (int or null): The ID of the branch associated with the provider (nullable).
  - `branch_name` (string): The name of the branch associated with the provider.
  - `branch_eng_name` (string): The English name of the branch associated with the provider.
  - `provider_name` (string): The name of the provider.
  - `is_provider_admin` (boolean): Indicates if the provider is an admin.
  - `is_branch_manager` (boolean): Indicates if the provider is a branch manager.
  - `is_technician` (boolean): Indicates if the provider is a technician.
  - `total_completed_requests` (int): The total number of completed requests by the provider.
  - `total_pending_requests` (int): The total number of pending requests assigned to the provider.
  - `total_canceled_requests` (int): The total number of canceled requests by the provider.
  - `avg_evaluation` (float): The average evaluation rating received by the provider.
  - `provider_logo` (string or null): The URL or path to the provider's logo image (nullable).

#### Example

**Response**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "provider_id": null,
    "profile_id": 21211,
    "name": "test111",
    "mobile": "0556204787",
    "email": "teekkaayy.08+taimoorprovider@gmail.com",
    "username": "test111",
    "join_date": null,
    "id_number": null,
    "branch_id": null,
    "branch_name": "",
    "branch_eng_name": "",
    "provider_name": "test111",
    "is_provider_admin": true,
    "is_branch_manager": false,
    "is_technician": false,
    "total_completed_requests": 142,
    "total_pending_requests": 12,
    "total_canceled_requests": 12,
    "avg_evluation": 4.037974,
    "provider_logo": null
  }
}
```

