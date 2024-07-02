# Transfer Employee to a new branch
### API Endpoint: /Provider/User/Transfer

**Method**: POST

**Description**: Transfers a user to a new branch.

#### Query Parameters

- `id`: `integer` (required) - The ID of the user to be transferred.
- `new_branch_id`: `integer` (required) - The ID of the new branch to which the user will be transferred.

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `null` - No additional data is returned.

#### Response

```json
{
  "status": true,
  "message": "لقد تمت المهمه بنجاح",
  "error": "",
  "Data": null
}
```



