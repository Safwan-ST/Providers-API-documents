### Follow Requests

**Endpoint**: `POST /Provider/FollowRequests`

**Description**: Retrieve a list of requests based on various filters.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Query Parameters**:
- `is_the_booking_today` (bool): Filter requests for bookings made today.
- `is_the_booking_yesterday` (bool): Filter requests for bookings made yesterday.
- `show_last_seven_days` (bool): Filter requests for bookings made in the last seven days.
- `show_last_thirty_days` (bool): Filter requests for bookings made in the last thirty days.
- `service_ids` (Array[long]): Filter requests based on service IDs.

**Request Query Example**:
```
/Provider/FollowRequests?is_the_booking_today=true&show_last_seven_days=false&service_ids=1,2,3
```

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (array): An array of request objects, each containing details of the requests.
  - `id` (int): The identifier for the request.
  - `status_id` (int): The ID of the status of the request.
  - `status_name` (string): The name of the status in Arabic.
  - `status_eng_name` (string): The name of the status in English.
  - `service_id` (int): The ID of the service.
  - `service_name` (string): The name of the service in Arabic.
  - `service_eng_name` (string): The name of the service in English.
  - `branch_id` (int): The ID of the branch.
  - `branch_name` (string): The name of the branch in Arabic.
  - `branch_eng_name` (string): The name of the branch in English.
  - `assigned_employee_id` (int): The ID of the assigned employee.
  - `assigned_employee_name` (string): The name of the assigned employee.
  - `customer_id` (int): The ID of the customer.
  - `booked_date` (string): The date of the booking (format: MM/DD/YYYY).
  - `booked_time` (string): The time of the booking (format: HH:MM:SS).
  - `is_shipping_service` (boolean): Indicates if it's a shipping service.
  - `is_package_service` (boolean): Indicates if it's a package service.
  - `is_for_pickup` (boolean): Indicates if it's for pickup.
  - `is_the_booking_today` (boolean): Indicates if the booking was made today.
  - `status_category` (object): Object containing status category details.
    - `bg_color` (string): Background color code for the status category.
    - `text_color` (string): Text color code for the status category.
    - `name` (string): Name of the status category in Arabic.
    - `eng_name` (string): Name of the status category in English.
    - `is_new` (boolean): Indicates if the status is new.
    - `is_late` (boolean): Indicates if the status is late.
    - `is_need_attention` (boolean): Indicates if attention is needed.
  - `city_name` (string): The name of the city in Arabic.
  - `city_eng_name` (string): The name of the city in English.
  - `area_name` (string): The name of the area in Arabic.
  - `area_eng_name` (string): The name of the area in English.
  - `car` (object): Object containing details about the car associated with the request.
    - `car_profile_id` (int): The profile ID of the car.
    - `car_model_id` (int): The model ID of the car.
    - `car_model_name` (string): The name of the car model in Arabic.
    - `car_model_eng_name` (string): The name of the car model in English.
    - `car_vendor_id` (int): The vendor ID of the car.
    - `car_vendor_name` (string): The name of the car vendor in Arabic.
    - `car_vendor_eng_name` (string): The name of the car vendor in English.
    - `car_color_id` (int): The color ID of the car.
    - `car_color_name` (string): The name of the car color in Arabic.
    - `car_color_eng_name` (string): The name of the car color in English.
  - `shipping_address` (null): Placeholder for shipping address details (currently null).
  - `shipping_courier` (null): Placeholder for shipping courier details (currently null).

**Response Example**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "id": 14765,
      "status_id": 105,
      "status_name": "بدء الخدمة",
      "status_eng_name": "Start the service",
      "service_id": 1,
      "service_name": "تقدير الحوادث",
      "service_eng_name": "Accident Estimation",
      "branch_id": 60,
      "branch_name": "الفرع الرئيسي",
      "branch_eng_name": "Main Branch",
      "assigned_employee_id": 20137,
      "assigned_employee_name": "GFHFGH",
      "customer_id": 10200,
      "booked_date": "9/28/2023",
      "booked_time": "05:00:00",
      "is_shipping_service": null,
      "is_package_service": null,
      "is_for_pickup": null,
      "is_the_booking_today": false,
      "status_category": {
        "bg_color": "#1EA94E",
        "text_color": "#FFFFFF",
        "name": "جديد",
        "eng_name": "New",
        "is_new": true,
        "is_late": true,
        "is_need_attention": false
      },
      "city_name": "الرياض",
      "city_eng_name": "Riyadh",
      "area_name": "الرائد",
      "area_eng_name": "Al Raed",
      "car": {
        "car_profile_id": 17343,
        "car_model_id": 306,
        "car_model_name": "جيمني",
        "car_model_eng_name": "Jimny",
        "car_vendor_id": 44,
        "car_vendor_name": "سوزوكي",
        "car_vendor_eng_name": "Suzuki",
        "car_color_id": 3,
        "car_color_name": "رمادي",
        "car_color_eng_name": "Gray"
      },
      "shipping_address": null,
      "shipping_courier": null
    }
  ]
}
```