

## MoveNextStep

**Endpoint:** `/Provider/MoveNextStep`  
**Method:** `POST`  
**Query Parameter:**
- `id` (int): Request ID to move to the next step

**Request Body:**
```json
{
  "courier_name": "string",
  "tracking_number": "string",
  "tracking_url": "string",
  "pickup_address": "string"
}
```
(Note: The request body can be null)

### Response Parameters:
- `status` (boolean): Indicates if the operation was successful.
- `message` (string): Describes the outcome of the operation.
- `error` (string): Contains.
- `Data` (object): Contains detailed information related to the request and its current state.
  - `request` (object): Details about the request being processed.
  - `helper` (object): Additional helper data including permissions and lists related to the request.

**Response:**
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "request": {
      "id": 15158,
      "mile_age": null,
      "note": "",
      "is_prepaid": null,
      "isRejected": false,
      "is_simple_service": true,
      "is_for_vehicle_repair": true,
      "is_for_oil": false,
      "is_for_tires": false,
      "is_for_battaries": false,
      "service_master_group_id": 3,
      "is_package_service": null,
      "is_shipping_service": null,
      "is_for_pickup": null,
      "service_master_group_name": "إصلاح المركبات والحوادث",
      "service_master_group_eng_name": "Vehicle and accident repair",
      "invoice": {
        "total": 300,
        "coupon_discount": 0,
        "coupon_name": "",
        "coupon_percentage": 0,
        "is_fixed_discount_amount": true,
        "prepaid_amount": null,
        "amount_to_pay": 300,
        "isPaid": false,
        "paid_amount": 0,
        "status": "غير مدفوعه",
        "status_color": "#FF0000"
      },
      "status": {
        "id": 102,
        "name": "جاهز للخدمة\r\n",
        "eng_name": "Ready To Serve"
      },
      "customer": {
        "id": 10258,
        "name": "561316069",
        "eng_name": "561316069",
        "phone": "",
        "address": {
          "address_type": {
            "id": 1,
            "name": "المنزل",
            "eng_name": "Home"
          },
          "loc_desc": "",
          "lat": "24.707954448228315384615384615",
          "lng": "46.640213923527646153846153846",
          "area": {
            "id": 40,
            "name": "الرائد",
            "eng_name": "Al Raed"
          },
          "zone": {
            "id": 13,
            "name": "R8",
            "eng_name": "R8"
          }
        }
      },
      "car": {
        "car_profile_id": 17961,
        "car_model_id": 12,
        "car_model_name": "لاند كروزر",
        "car_model_eng_name": "Land cruiser",
        "car_vendor_id": 1,
        "car_vendor_name": "تويوتا",
        "car_vendor_eng_name": "Toyota",
        "car_color_id": 0,
        "car_color_name": "",
        "car_color_eng_name": null,
        "expected_duration_of_repair": 0,
        "no_cylenders": 6,
        "vin": "",
        "plate_no": "",
        "oil_capcity": 7,
        "fuel_type": {
          "id": 1,
          "name": "بنزين",
          "eng_name": "Petrol"
        },
        "vender_binary_image": ""
      },
      "shipping_address": null,
      "shipping_courier": null,
      "items": [
        {
          "id": 39482,
          "item_id": 13986,
          "brand_id": null,
          "item_name": "رسوم السطحة",
          "item_eng_name": "Car Carrier",
          "item_desc": "test",
          "brand_name": null,
          "brand_eng_name": null,
          "qty": 1,
          "price": 300,
          "qty1": 0,
          "price1": 0,
          "is_check_option": false,
          "check_optioin_id": null,
          "is_extra_service": null,
          "is_approved_by_customer": null,
          "is_mandatory": null,
          "item_group_name": null,
          "item_group_eng_name": null,
          "check_optioin_name": null,
          "check_optioin_eng_name": null,
          "manufacture_year": null,
          "item_type": {
            "id": 1,
            "name": "منتجات",
            "eng_name": "Products"
          }
        }
      ],
      "extra_fees": [],
      "service": {
        "id": 10019,
        "name": "ميكانيك",
        "eng_name": "Mechanic"
      },
      "original_items": [
        {
          "item_id": 13986,
          "brand_id": null,
          "item_name": "رسوم السطحة",
          "item_desc": "test",
          "brand_name": null,
          "brand_eng_name": null,
          "qty": 1,
          "price": 300,
          "qty1": 0,
          "price1": 0,
          "is_check_option": false,
          "check_optioin_id": null,
          "check_optioin_name": null,
          "check_optioin_eng_name": null,
          "item_type": {
            "id": 1,
            "name": "منتجات",
            "eng_name": "Products"
          }
        }
      ],
      "attached_images": {
        "before": [],
        "after": []
      },
      "evaluation": null
    },
    "helper": {
      "step_permission": {
        "show_customer_info": true,
        "can_save_update": false,
        "can_cancel": true,
        "can_pay": false,
        "can_close": false,
        "can_reset_booking_schedule": false,
        "can_upload_invoice": false,
        "can_move_to_next_step": true,
        "can_notify_customer_about_payment": false,
        "next_step": {
          "id": 103,
          "name": "في الطريق إلى العميل\r\n",
          "eng_name": "On the way to customer"
        }
      },
      "extra_fees_list": [
        {
          "id": 2845,
          "name": "تتتتت",
          "eng_name": "tttt",
          "price": 100,
          "orderno": 1
        }
      ],
      "item_groups": [
        {
          "id": 13,
          "name": "ميكانيك",
          "eng_name": "Mechanic",
          "items": [
            {
              "id": 13987,
              "name": "ميكانيك",
              "eng_name": "Mechanic"
            },
            {
              "id": 13997,
              "name": "اعمال الفرامل ",
              "eng_name": "break "
            },
            {
              "id": 13998,
              "name": "صيانة المحرك ",
              "eng_name": null
            },
            {
              "id": 14079,
              "name": "ميكانيك",
              "eng_name": "ميكانيك"
            },
            {
              "id": 14080,
              "name": "سمكرة ",
              "eng_name": "سمكرة "
            },
            {
              "id": 14081,
              "name": "سمكرة ",
              "eng_name": "سمكرة "
            }
          ]
        }
      ],
      "checks_list": [],
      "checks_options_list": [],
      "cancel_reaons_list": [],
      "chat_option": {
        "can_send_chat_message": true,
        "can_view_chat_messages": true,
        "from_id": 20133,
        "from_name": "sayaratech",
        "to_ids": [
          20445,
          20217
        ],
        "to_fcm_tokens": []
      },
      "change_technician_option": {
        "can_change_technician": true,
        "list": [
          {
            "id": 20206,
            "name": "representative",
            "has_warning": false,
            "warning_msg": null,
            "warning_eng_msg": null
          },
          {
            "id": 21208,
            "name": "zov",
            "has_warning": false,
            "warning_msg": null,
            "warning_eng_msg": null
          }
        ]
      }
    }
  }
}
```



