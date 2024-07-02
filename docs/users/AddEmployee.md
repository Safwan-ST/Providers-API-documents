 # Add User

### API Endpoint: /Provider/Users/Add

**Method**: POST

**Description**: Adds a new user to a Branch.

#### Request Body

```json
{
  "id": null,
  "username": "string",
  "pwd": "string",
  "full_name": "string",
  "email": "string",
  "mobile": "string",
  "is_active": true,
  "branch_id": 265,
  "usertype_id": 1,
  "id_number": "string",
  "id_expire_date": "2024-07-01T19:46:25.716Z",
  "list_of_supported_services": [2],
  "list_of_supported_car_veners": [],
  
   "car_vendor_id": null,
  "car_model_id": null,
  "car_color_id": null,
  "car_model_year": null,
  "car_doc_image_binary_image": null,
  "id_number_imgage_binary_image": null
}
```

**Parameters**:

- `id`: `null` (integer or null, required) - The ID of the user. Use `null` when adding a new user.
- `username`: `string` (required) - The username of the user.
- `pwd`: `string` (required) - The password of the user.
- `full_name`: `string` (required) - The full name of the user.
- `email`: `string` (required) - The email of the user.
- `mobile`: `string` (required) - The mobile number of the user.
- `is_active`: `boolean` (required) - The active status of the user.
- `branch_id`: `integer` (required) - The ID of the branch the user is associated with.
- `usertype_id`: `integer` (required) - The type ID of the user.
- `id_number`: `string` (required) - The ID number of the user.
- `id_expire_date`: `date-time` (required) - The expiration date of the user's ID.
- `list_of_supported_services`: `array of integers` (optional) - List of IDs of supported services.
- `list_of_supported_car_veners`: `array of integers` (optional) - List of IDs of supported car vendors.



**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `object` - The data object containing the newly added user's details.
  - `id`: `integer` - The ID of the newly added user.
  - `full_name`: `string` - The full name of the user.
  - `username`: `string` - The username of the user.
  - `mobile`: `string` - The mobile number of the user.
  - `email`: `string` - The email of the user.
  - `branch_id`: `integer` - The ID of the branch the user is associated with.
  - `is_active`: `boolean` - The active status of the user.
  - `under_review`: `boolean` - Whether the user is under review.
  - `under_review_comments`: `string or null` - Any comments regarding the review.
  - `branch_name`: `string` - The name of the branch in Arabic.
  - `branch_eng_name`: `string` - The name of the branch in English.
  - `id_number`: `string` - The ID number of the user.
  - `id_expire_date`: `date-time` - The expiration date of the user's ID.
  - `user_type_name`: `string` - The name of the user type in Arabic.
  - `user_type_eng_name`: `string` - The name of the user type in English.
  - `usertype_id`: `integer` - The type ID of the user.
  - `car`: `object` - The car details of the user.
    - `car_vendor_id`: `integer or null` - The car vendor ID.
    - `car_model_year`: `integer or null` - The car model year.
    - `car_model_id`: `integer or null` - The car model ID.
    - `car_color_id`: `integer or null` - The car color ID.
  - `supported_services`: `array of objects` - List of supported services.
    - `sevice_master_id`: `integer` - The service master ID.
    - `eng_name`: `string` - The name of the service in English.
    - `name`: `string` - The name of the service in Arabic.
  - `supported_car_venders`: `array of objects` - List of supported car vendors.

  
#### Response

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "id": 21414,
    "full_name": "string",
    "username": "string",
    "mobile": "string",
    "email": "string",
    "branch_id": 265,
    "is_active": true,
    "under_review": true,
    "under_review_comments": null,
    "branch_name": "tenth Android app branch Arabic all cars",
    "branch_eng_name": "10th Android app branch English all cars",
    "id_number": "string",
    "id_expire_date": "2024-07-01T19:46:25.717",
    "user_type_name": "مدير فرع",
    "user_type_eng_name": "Branch Manager",
    "usertype_id": 1,
    "car": {
      "car_vendor_id": null,
      "car_model_year": null,
      "car_model_id": null,
      "car_color_id": null
    },
    "supported_services": [
      {
        "sevice_master_id": 2,
        "eng_name": "Battery Services",
        "name": "تبديل البطاريات"
      }
    ],
    "supported_car_venders": []
  }
}
```



