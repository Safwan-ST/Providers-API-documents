
# Get Ticket Details

**Endpoint**: `POST /Tickets/Details`

**Description**: Retrieves details of a specific support ticket.

**Authentication**: Requires Bearer Token Authentication in the header.

**Query Parameters**:
- `ticket_id` (int, required): The ID of the ticket to retrieve details for.

**Response Parameters**:
- `status` (boolean): Indicates if the operation was successful (`true` or `false`).
- `message` (string): Describes the outcome of the operation.
- `error` (string): Provides details of any errors encountered during the operation.
- `Data` (object): Contains detailed information about the ticket.
  - `id` (int): The ID of the ticket.
  - `created_by` (string): The username of the user who created the ticket.
  - `created_date` (string): The date and time when the ticket was created (in ISO 8601 format).
  - `body` (string): The detailed description or body of the ticket.
  - `is_closed` (boolean): Indicates if the ticket is closed (`true` or `false`).
  - `closed_date` (string or null): The date and time when the ticket was closed (in ISO 8601 format), or `null` if not closed.
  - `related_request` (object): Details of the related service request, if applicable.
    - `request_id` (int): The ID of the related service request.
    - `request_type_name` (string): The name of the service request type.
    - `request_type_eng_name` (string): The English name of the service request type.
    - `request_status_name` (string): The name of the current status of the service request.
    - `request_status_eng_name` (string): The English name of the current status of the service request.
    - `request_customer_name` (string): The name of the customer associated with the service request.
    - `request_customer_eng_name` (string): The English name of the customer associated with the service request.
  - `category_id` (int): The ID of the ticket category.
  - `category_name` (string): The name of the ticket category.
  - `category_eng_name` (string): The English name of the ticket category.
  - `status` (object): The current status of the ticket.
    - `status_id` (int): The ID of the ticket status.
    - `status_name` (string): The name of the ticket status.
    - `status_eng_name` (string): The English name of the ticket status.
    - `status_color` (string): The color code associated with the ticket status.
  - `replies` (array): An array of replies to the ticket, each reply object includes:
    - `id` (int): The ID of the reply.
    - `body` (string): The body or content of the reply.
    - `created_date` (string): The date and time when the reply was created (in ISO 8601 format).
    - `created_by` (string): The username of the user who created the reply.
    - `attachments` (array): An array of attachments associated with the reply, each attachment object includes:
      - `id` (int): The ID of the attachment.
      - `name` (string): The name of the attachment.
      - `contents` (string): The binary content or description of the attachment.
  - `attachments` (array): An array of attachments associated directly with the ticket, each attachment object includes:
    - `id` (int): The ID of the attachment.
    - `name` (string): The name of the attachment.
    - `contents` (string): The binary content or description of the attachment.

#### Example

**Request**:
```json
{
    "ticket_id": 192
}
```

**Response**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": {
    "id": 192,
    "created_by": "sayaratech",
    "created_date": "2024-05-02T01:30:38.943",
    "body": "tttt",
    "is_closed": false,
    "closed_date": null,
    "related_request": {
      "request_id": 15445,
      "request_type_name": "ميكانيك",
      "request_type_eng_name": "Mechanic",
      "request_status_name": "الاستلام وبدء الفحص",
      "request_status_eng_name": "Hading and Checking car",
      "request_customer_name": "Ali Test",
      "request_customer_eng_name": "Ali Test"
    },
    "category_id": 4,
    "category_name": "اخرى",
    "category_eng_name": "Others",
    "status": {
      "status_id": 0,
      "status_name": "جديد",
      "status_eng_name": "New",
      "status_color": "#fc8403"
    },
    "replies": [
     
      {
        "id": 130,
        "body": "adsadssa",
        "created_date": "2024-05-13T17:38:40.817",
        "created_by": "sayaratech",
        "attachments": [
          {
            "id": 129,
            "name": "premium_photo-1664474619075-644dd191935f.jpg",
            "contents": "Byetes file"
          }
        ]
      },
  
    ],
    "attachments": []
  }
}
```
