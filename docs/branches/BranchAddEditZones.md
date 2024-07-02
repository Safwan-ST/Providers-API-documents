
# Add Edit Zones
## /Provider/Branches/AddEditZones

### Method
`POST`

### Description
Adds or edits zones for a branch.

### Query Parameters
- `id` (int): Branch ID to add or edit the zones.

### Request Body
- `zones` (list<int>): Array of zone IDs to add or edit to the branch.

### Response Example
```json
{
  "status": true,
  "message": "تمت المهمه بنجاح",
  "error": "",
  "Data": null
}
```
```