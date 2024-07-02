# Get Pending List
```
 API Endpoint: `/Provider/Evaluations/GetPendingList`
```

#### Method:
POST

### Endpoint Description:
This endpoint retrieves a list of pending evaluations for service requests. 

#### Response Parameters:
- `status` (boolean): Indicates the success or failure of the request.
- `message` (string): A message indicating the outcome of the request.
- `error` (string): Contains any error details if applicable.
- `Data` (array of objects): Contains a list of pending evaluations.
  - `request_id` (int): The ID of the request awaiting evaluation.
  - `customer` (object):
    - `id` (int): ID of the customer.
    - `name` (string): Name of the customer.
    - `eng_name` (string): English name of the customer.
  - `service` (object):
    - `id` (int): ID of the service.
    - `name` (string): Name of the service.
    - `eng_name` (string): English name of the service.

    
#### Response Example:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "request_id": 16970,
      "customer": {
        "id": 10376,
        "name": "Jamal Khalid",
        "eng_name": "Jamal Khalid"
      },
      "service": {
        "id": 10019,
        "name": "ميكانيك",
        "eng_name": "Mechanic"
      }
    },
    {
      "request_id": 17091,
      "customer": {
        "id": 10384,
        "name": "555455272",
        "eng_name": "555455272"
      },
      "service": {
        "id": 10022,
        "name": "غسيل اكسبريس",
        "eng_name": "Express Wash"
      }
    },
    {
      "request_id": 17092,
      "customer": {
        "id": 10384,
        "name": "555455272",
        "eng_name": "555455272"
      },
      "service": {
        "id": 10022,
        "name": "غسيل اكسبريس",
        "eng_name": "Express Wash"
      }
    }
  ]
}
```




