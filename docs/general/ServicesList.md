# Services List

### API Endpoint: /Provider/Services/List

**Method**: POST

**Description**: Retrieves the list of services.

#### Response

**Example Response**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "id": 2,
      "name": "تبديل البطاريات ",
      "eng_name": "Battery Services",
      "allow_quick_order": true,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 3,
      "name": "تبديل الكفرات ",
      "eng_name": "Tires Services",
      "allow_quick_order": true,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 5,
      "name": "تغيير الزيت",
      "eng_name": "Change Oil",
      "allow_quick_order": true,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 7,
      "name": " تلميع السيارات",
      "eng_name": "Car Polishing",
      "allow_quick_order": true,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 10019,
      "name": "ميكانيك",
      "eng_name": "Mechanic",
      "allow_quick_order": false,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 10036,
      "name": "باقة غسيل السيارة ",
      "eng_name": "باقة غسيل السيارة ",
      "allow_quick_order": false,
      "is_active": true,
      "binary_image": null
    },
    {
      "id": 10042,
      "name": "متجر سيارتك",
      "eng_name": "Sayaratech Store",
      "allow_quick_order": true,
      "is_active": true,
      "binary_image": null
    }
  ]
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `array` - An array of objects representing the services with the following properties:
  - `id`: `integer` - The ID of the service.
  - `name`: `string` - The name of the service in Arabic.
  - `eng_name`: `string` - The name of the service in English.
  - `allow_quick_order`: `boolean` - Indicates if quick order is allowed for the service.
  - `is_active`: `boolean` - Indicates if the service is active.
  - `binary_image`: `string|null` - A binary image associated with the service (if any).

