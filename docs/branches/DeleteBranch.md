# Delete Branch
## `POST /Provider/Branches/Delete`

### Description
Deletes a branch with the specified ID.

### Query Parameters

- `id` (int, required): The ID of the branch to be deleted.

### Response Example

```json
{
  "status": true,
  "message": "لقد تمت المهمه بنجاح",
  "error": "",
  "Data": null
}
```

### Response Parameters

- `status` (boolean): Indicates if the branch was successfully deleted.
- `message` (string): A message describing the result of the operation.
- `error` (string): An error message if the operation failed.
- `Data` (null): No additional data returned.

---

