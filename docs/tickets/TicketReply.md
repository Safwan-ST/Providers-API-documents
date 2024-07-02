

# Reply to Support Ticket

**Endpoint**: `POST /Tickets/Reply`

**Description**: Adds a reply to an existing support ticket.

**Request Body Parameters**:
- `ticket_id` (required): The ID of the ticket to which the reply is being added.
- `body` (required): The text body of the reply.
- `assigned_to_user_id` (optional): The ID of the user to whom the ticket is assigned.
- `mentioned_to` (optional): An array of user IDs who are mentioned in the reply.
- `files` (optional): An array of files to be attached to the reply. Each file object includes:
  - `file_name_with_extension`: The name of the file with its extension, e.g., `image.jpg`.
  - `content`: The binary content of the file.

**Response Parameters**:
- `status`: Indicates if the operation was successful (`true` or `false`).
- `message`: Describes the outcome of the operation.
- `error`: Provides details of any errors encountered during the operation.
- `Data`: Contains additional data related to the operation. Currently set to `null` for this API.

#### Example

**Request**:
```json
{
  "ticket_id": 192,
  "body": "لقد تم استلام طلبكم وسيتم معالجته في أقرب وقت ممكن.",
  "assigned_to_user_id": 0,
  "mentioned_to": [0],
  "files": [
    {
      "file_name_with_extension": "screenshot.png",
      "content": "Base64-encoded file content"
    }
  ]
}
```

**Response**:
```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```