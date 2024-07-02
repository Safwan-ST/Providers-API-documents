
# Branches
### `POST /Provider/Branches/List`

### Description
Retrieves a list of branches along with their details.

### Response Example

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "id": 221,
      "name": "فرع تيمور بالرياض مايو 2024",
      "eng_name": "Taimoor's Riyadh Branch May 2024",
      "phone": "556204787",
      "email": "teekkaayy.08+taimoorbranch@gmail.com",
      "city_id": 1,
      "city_name": "الرياض",
      "city_eng_name": "الرياض",
      "is_active": true,
      "branch_manager_id": 21337,
      "branch_manager_name": "taimoor branch manager",
      "supported_services": [
        {
          "sevice_master_id": 1,
          "eng_name": "Accident Estimation",
          "name": "تقدير الحوادث"
        },
        {
          "car_vendor_id": 18,
          "name": "فيات",
          "eng_name": "Fiat"
        },
        {
          "car_vendor_id": 53,
          "name": "ديهاتسو",
          "eng_name": "Daihatsu"
        }
      ],
      "supported_zones": [
        {
          "zone_id": 9,
          "name": "R1",
          "eng_name": "R1",
          "city_id": 1,
          "city_name": "الرياض",
          "city_eng_name": "Riyadh"
        },
        {
          "zone_id": 17,
          "name": "R10",
          "eng_name": "R10",
          "city_id": 1,
          "city_name": "الرياض",
          "city_eng_name": "Riyadh"
        }
      ]
    }
  ]
}
```

### Response Parameters

- `status` (boolean): Indicates the success of the operation.
- `message` (string): A message indicating the result of the operation.
- `error` (string): Error message, if any.
- `Data` (array): List of branch objects.
  - `id` (int): The ID of the branch.
  - `name` (string): The name of the branch in Arabic.
  - `eng_name` (string): The name of the branch in English.
  - `phone` (string): The phone number of the branch.
  - `email` (string): The email address of the branch.
  - `city_id` (int): The ID of the city where the branch is located.
  - `city_name` (string): The name of the city in Arabic.
  - `city_eng_name` (string): The name of the city in English.
  - `is_active` (boolean): Indicates if the branch is active.
  - `branch_manager_id` (int): The ID of the branch manager.
  - `branch_manager_name` (string): The name of the branch manager.
  - `supported_services` (array): List of services supported by the branch.
    - `service_master_id` (int): The ID of the service.
    - `name` (string): The name of the service in Arabic.
    - `eng_name` (string): The name of the service in English.
  - `supported_zones` (array): List of zones supported by the branch.
    - `zone_id` (int): The ID of the zone.
    - `name` (string): The name of the zone in Arabic.
    - `eng_name` (string): The name of the zone in English.
    - `city_id` (int): The ID of the city where the zone is located.
    - `city_name` (string): The name of the city in Arabic.
    - `city_eng_name` (string): The name of the city in English.

---

