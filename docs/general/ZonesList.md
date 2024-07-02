# Zones List
### API Endpoint: /Provider/Zones/List

**Method**: POST

**Description**: Retrieves the list of zones.

#### Response

**Example Response**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": [
    {
      "zone_id": 9,
      "name": "R1",
      "eng_name": "R1",
      "city_id": 1,
      "city_name": "الرياض",
      "city_eng_name": "Riyadh"
    },
    {
      "zone_id": 10,
      "name": "R2",
      "eng_name": "R2",
      "city_id": 1,
      "city_name": "الرياض",
      "city_eng_name": "Riyadh"
    }
  
  ]
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `array` - An array of objects representing the zones with the following properties:
  - `zone_id`: `integer` - The ID of the zone.
  - `name`: `string` - The name of the zone.
  - `eng_name`: `string` - The English name of the zone.
  - `city_id`: `integer` - The ID of the city.
  - `city_name`: `string` - The name of the city.
  - `city_eng_name`: `string` - The English name of the city.

