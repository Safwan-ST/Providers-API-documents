### Get Request Details

**Endpoint**: `POST /Provider/RequestDetails`

**Description**: Retrieve detailed information about a specific service request.

**Authentication**: Requires Bearer Token Authentication in the header.

**Request Query Parameters**:
- `id` (int, required): The id of the service request.

**Response Parameters**:
- `status` (boolean): Indicates whether the operation was successful.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (object): Contains the detailed information of the request:
  - `request` (object): Contains request-specific details:
    - `id` (int): The identifier for the request.
    - `mile_age` (null or int): The mileage of the vehicle.
    - `note` (string): Any notes associated with the request.
    - `is_prepaid` (boolean): Indicates if the request is prepaid.
    - `isRejected` (boolean): Indicates if the request is rejected.
    - `is_simple_service` (boolean): Indicates if the request is a simple service.
    - `is_for_vehicle_repair` (boolean): Indicates if the request is for vehicle repair.
    - `is_for_oil` (boolean): Indicates if the request is for oil service.
    - `is_for_tires` (boolean): Indicates if the request is for tire service.
    - `is_for_battaries` (boolean): Indicates if the request is for battery service.
    - `service_master_group_id` (int): The ID of the service master group.
    - `is_package_service` (boolean): Indicates if the request is a package service.
    - `is_shipping_service` (boolean): Indicates if the request is a shipping service.
    - `is_for_pickup` (boolean): Indicates if the request is for pickup service.
    - `service_master_group_name` (string): The name of the service master group in Arabic.
    - `service_master_group_eng_name` (string): The name of the service master group in English.
  - `invoice` (object): Contains invoice-specific details:
    - `total` (int): The total amount.
    - `coupon_discount` (int): The coupon discount amount.
    - `coupon_name` (string): The name of the coupon.
    - `coupon_percentage` (int): The percentage of the coupon discount.
    - `is_fixed_discount_amount` (boolean): Indicates if the discount amount is fixed.
    - `prepaid_amount` (int): The prepaid amount.
    - `amount_to_pay` (int): The amount to be paid.
    - `isPaid` (boolean): Indicates if the invoice is paid.
    - `paid_amount` (int): The amount paid.
    - `status` (string): The status of the invoice.
    - `status_color` (string): The color representing the status.
  - `status` (object): Contains status-specific details:
    - `id` (int): The status ID.
    - `name` (string): The status name in Arabic.
    - `eng_name` (string): The status name in English.
  - `customer` (object): Contains customer-specific details:
    - `id` (int): The customer ID.
    - `name` (string): The customer name in Arabic.
    - `eng_name` (string): The customer name in English.
    - `phone` (string): The customer's phone number.
    - `address` (object): Contains address-specific details:
      - `address_type` (object): Contains address type details:
        - `id` (int): The address type ID.
        - `name` (string): The address type name in Arabic.
        - `eng_name` (string): The address type name in English.
      - `loc_desc` (string): The location description.
      - `lat` (string): The latitude of the address.
      - `lng` (string): The longitude of the address.
      - `area` (object): Contains area-specific details:
        - `id` (int): The area ID.
        - `name` (string): The area name in Arabic.
        - `eng_name` (string): The area name in English.
      - `zone` (object): Contains zone-specific details:
        - `id` (int): The zone ID.
        - `name` (string): The zone name in Arabic.
        - `eng_name` (string): The zone name in English.
  - `car` (object): Contains car-specific details:
    - `car_profile_id` (int): The car profile ID.
    - `car_model_id` (int): The car model ID.
    - `car_model_name` (string): The car model name in Arabic.
    - `car_model_eng_name` (string): The car model name in English.
    - `car_vendor_id` (int): The car vendor ID.
    - `car_vendor_name` (string): The car vendor name in Arabic.
    - `car_vendor_eng_name` (string): The car vendor name in English.
    - `car_color_id` (int): The car color ID.
    - `car_color_name` (string): The car color name in Arabic.
    - `car_color_eng_name` (string): The car color name in English.
    - `expected_duration_of_repair` (int): The expected duration of the repair.
    - `no_cylenders` (int): The number of cylinders.
    - `vin` (string): The Vehicle Identification Number (VIN).
    - `plate_no` (string): The car's plate number.
    - `oil_capcity` (int): The oil capacity.
    - `fuel_type` (object): Contains fuel type details:
      - `id` (int): The fuel type ID.
      - `name` (string): The fuel type name in Arabic.
      - `eng_name` (string): The fuel type name in English.
    - `vender_binary_image` (string): The vendor binary image.
  - `shipping_address` (object): Contains shipping address details (if applicable).
  - `shipping_courier` (object): Contains shipping courier details (if applicable).
  - `items` (array): An array of item objects, where each object contains:
    - `id` (int): The item ID.
    - `item_id` (int): The ID of the item.
    - `brand_id` (int): The ID of the brand.
    - `item_name` (string): The item name in Arabic.
    - `item_eng_name` (string): The item name in English.
    - `item_desc` (string): The item description.
    - `brand_name` (string): The brand name in Arabic.
    - `brand_eng_name` (string): The brand name in English.
    - `qty` (int): The quantity.
    - `price` (int): The price.
    - `qty1` (int): The secondary quantity.
    - `price1` (int): The secondary price.
    - `is_check_option` (boolean): Indicates if the item is a check option.
    - `check_optioin_id` (int): The ID of the check option.
    - `is_extra_service` (boolean): Indicates if the item is an extra service.
    - `is_approved_by_customer` (boolean): Indicates if the item is approved by the customer.
    - `is_mandatory` (boolean): Indicates if the item is mandatory.
    - `item_group_name` (string): The item group name in Arabic.
    - `item_group_eng_name` (string): The item group name in English.
    - `check_optioin_name` (string): The name of the check option in Arabic.
    - `check_optioin_eng_name` (string): The name of the check option in English.
    - `manufacture_year` (int): The manufacture year of the item.
    - `item_type` (object): Contains item type details:
      - `id` (int): The item type ID.
      - `name` (string): The item type name in Arabic.
      - `eng_name` (string): The item type name in English.
  - `extra_fees` (array): An array of extra fee objects.
  - `service` (object): Contains service-specific details:
    - `id` (int): The service ID.
    - `name` (string): The service name in Arabic.
    - `eng_name` (string): The service name in English.
  - `original_items` (array): An array of original item objects.
  - `attached_images` (object): Contains attached images before and after the service.
  - `evaluation` (object): Contains evaluation details.
  - `helper` (object): Contains helper-specific details:
    - `step_permission` (object): Contains step permission details:
      - `show_customer_info` (boolean): Indicates if customer info can be shown.
      - `can_save_update` (boolean): Indicates if updates can be saved.
      - `can_cancel` (boolean): Indicates if the request can be canceled.
      - `can_pay` (boolean): Indicates if payment can be made.
      - `can_close` (boolean): Indicates if the request can be closed.
      -

 `is_pending` (boolean): Indicates if the request is pending.
      - `can_reject` (boolean): Indicates if the request can be rejected.
      - `can_show_extra_service_tab` (boolean): Indicates if the extra service tab can be shown.
      - `can_show_check_options_tab` (boolean): Indicates if the check options tab can be shown.

**Response Example**:
```json
{
  "status": true,
  "message": "Success",
  "error": null,
  "Data": {
    "request": {
      "id": 123,
      "mile_age": null,
      "note": "Need urgent service",
      "is_prepaid": true,
      "isRejected": false,
      "is_simple_service": true,
      "is_for_vehicle_repair": false,
      "is_for_oil": true,
      "is_for_tires": false,
      "is_for_battaries": false,
      "service_master_group_id": 1,
      "is_package_service": false,
      "is_shipping_service": false,
      "is_for_pickup": true,
      "service_master_group_name": "خدمة بسيطة",
      "service_master_group_eng_name": "Simple Service"
    },
    "invoice": {
      "total": 100,
      "coupon_discount": 10,
      "coupon_name": "SUMMER21",
      "coupon_percentage": 10,
      "is_fixed_discount_amount": false,
      "prepaid_amount": 50,
      "amount_to_pay": 40,
      "isPaid": true,
      "paid_amount": 90,
      "status": "Paid",
      "status_color": "#00FF00"
    },
    "status": {
      "id": 1,
      "name": "مكتمل",
      "eng_name": "Completed"
    },
    "customer": {
      "id": 456,
      "name": "علي",
      "eng_name": "Ali",
      "phone": "+1234567890",
      "address": {
        "address_type": {
          "id": 1,
          "name": "منزل",
          "eng_name": "Home"
        },
        "loc_desc": "123 Main St",
        "lat": "24.7136",
        "lng": "46.6753",
        "area": {
          "id": 2,
          "name": "الرياض",
          "eng_name": "Riyadh"
        },
        "zone": {
          "id": 3,
          "name": "المنطقة الوسطى",
          "eng_name": "Central Region"
        }
      }
    },
    "car": {
      "car_profile_id": 789,
      "car_model_id": 101,
      "car_model_name": "تويوتا كامري",
      "car_model_eng_name": "Toyota Camry",
      "car_vendor_id": 202,
      "car_vendor_name": "تويوتا",
      "car_vendor_eng_name": "Toyota",
      "car_color_id": 303,
      "car_color_name": "أبيض",
      "car_color_eng_name": "White",
      "expected_duration_of_repair": 3,
      "no_cylenders": 4,
      "vin": "123456789ABCDEFG",
      "plate_no": "ABC-1234",
      "oil_capcity": 5,
      "fuel_type": {
        "id": 1,
        "name": "بنزين",
        "eng_name": "Petrol"
      },
      "vender_binary_image": "base64imagestring"
    },
    "shipping_address": null,
    "shipping_courier": null,
    "items": [
      {
        "id": 1,
        "item_id": 1,
        "brand_id": 1,
        "item_name": "زيت محرك",
        "item_eng_name": "Engine Oil",
        "item_desc": "High-quality engine oil",
        "brand_name": "براند",
        "brand_eng_name": "Brand",
        "qty": 1,
        "price": 100,
        "qty1": 0,
        "price1": 0,
        "is_check_option": false,
        "check_optioin_id": 0,
        "is_extra_service": false,
        "is_approved_by_customer": true,
        "is_mandatory": true,
        "item_group_name": "مجموعة الزيت",
        "item_group_eng_name": "Oil Group",
        "check_optioin_name": "",
        "check_optioin_eng_name": "",
        "manufacture_year": 2020,
        "item_type": {
          "id": 1,
          "name": "قطع غيار",
          "eng_name": "Spare Part"
        }
      }
    ],
    "extra_fees": [],
    "service": {
      "id": 1,
      "name": "تغيير زيت",
      "eng_name": "Oil Change"
    },
    "original_items": [],
    "attached_images": {
      "before": [],
      "after": []
    },
    "evaluation": {},
    "helper": {
      "step_permission": {
        "show_customer_info": true,
        "can_save_update": true,
        "can_cancel": false,
        "can_pay": true,
        "can_close": true,
        "is_pending": false,
        "can_reject": false,
        "can_show_extra_service_tab": true,
        "can_show_check_options_tab": true
      }
    }
  }
}
```
