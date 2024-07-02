
# Employee List

## 'POST /Provider/Users/List'

### Description
Fetches the list of users based on the provided filters. All fields in the request body are nullable and can be used to filter the search results.

### Request Body Parameters
- `name` (string, nullable): The name of the user to filter by.
- `branch_id` (int, nullable): The ID of the branch to filter by.
- `usertype_id` (int, nullable): The ID of the user type to filter by.

 search by filter all is nullable

### Request Example
```json
{
  "name": "String",
  "branch_id": 1,
  "usertype_id": 2
}
```

### Response Example
```json
{
  "status": true,
  "message": "تمت العملية بنجاح",
  "error": "",
  "Data": [
    {
      "id": 21238,
      "full_name": "mostafa",
      "username": "mostafa",
      "mobile": "0555860161",
      "email": "mostafa@gmail.com",
      "branch_id": 187,
      "is_active": true,
      "under_review": false,
      "under_review_comments": null,
      "branch_name": "عشرون",
      "branch_eng_name": "twenty",
      "id_number": null,
      "id_expire_date": null,
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
          "sevice_master_id": 10019,
          "eng_name": "Mechanic",
          "name": "ميكانيك"
        }
      ],
      "supported_car_venders": [
        {
          "id": 1,
          "name": "تويوتا",
          "eng_name": "Toyota"
        }
      ]
    }
  ]
}
```

### Response Structure
- `status` (boolean): Indicates if the request was successful.
- `message` (string): Message describing the result of the operation.
- `error` (string): Error message, if any.
- `Data` (array): An array of user objects containing:
  - `id` (int): The user's ID.
  - `full_name` (string): The full name of the user.
  - `username` (string): The username of the user.
  - `mobile` (string): The mobile number of the user.
  - `email` (string): The email address of the user.
  - `branch_id` (int): The ID of the branch the user belongs to.
  - `is_active` (boolean): Indicates if the user is active.
  - `under_review` (boolean): Indicates if the user is under review.
  - `under_review_comments` (string, nullable): Comments related to the review, if any.
  - `branch_name` (string): The name of the branch the user belongs to.
  - `branch_eng_name` (string): The English name of the branch.
  - `id_number` (string, nullable): The ID number of the user.
  - `id_expire_date` (string, nullable): The expiration date of the user's ID.
  - `user_type_name` (string): The name of the user type.
  - `user_type_eng_name` (string): The English name of the user type.
  - `usertype_id` (int): The ID of the user type.
  - `car` (object): Information about the user's car, if any.
    - `car_vendor_id` (int, nullable): The ID of the car vendor.
    - `car_model_year` (int, nullable): The year of the car model.
    - `car_model_id` (int, nullable): The ID of the car model.
    - `car_color_id` (int, nullable): The ID of the car color.
  - `supported_services` (array): A list of services supported by the user.
    - `sevice_master_id` (int): The ID of the service.
    - `eng_name` (string): The English name of the service.
    - `name` (string): The name of the service.
  - `supported_car_venders` (array): A list of car vendors supported by the user.
    - `id` (int): The ID of the car vendor.
    - `name` (string): The name of the car vendor.
    - `eng_name` (string): The English name of the car vendor.



