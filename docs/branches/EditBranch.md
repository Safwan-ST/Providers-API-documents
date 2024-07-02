
# Edit Branch
## `POST /Provider/Branches/Edit`

### Description
Edit a new branch with the provided details.

### Response Example

```json
{
  "id": 0,
  "name": "string",
  "eng_name": "string",
  "city_id": 0,
  "manager_id": 0,
  "phone": "string",
  "email": "string",
  "more_info": "string",
  "is_active": true,
  "list_of_supported_services": [
    0
  ],
  "list_of_supported_car_veners": [
    0
  ]
}
```

### Response Parameters

- `id` (int): The ID of the newly added branch.
- `name` (string): The name of the branch.
- `eng_name` (string): The name of the branch in English.
- `city_id` (int): The ID of the city where the branch is located.
- `manager_id` (int): The ID of the branch manager.
- `phone` (string): The phone number of the branch.
- `email` (string): The email address of the branch.
- `more_info` (string): Additional information about the branch.
- `is_active` (boolean): Indicates if the branch is active.
- `list_of_supported_services` (array): List of supported service IDs.
- `list_of_supported_car_veners` (array): List of supported car vendor IDs.

---

