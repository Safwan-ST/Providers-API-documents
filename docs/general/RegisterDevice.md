# Register Device
### API Endpoint: /Provider/Devices/RegisterDevice

**Method**: POST

**Description**: Registers a device with the provided token, device ID, and OS type.

#### Query Parameters

- `token`: `string` (required) - The device token.
- `device_id`: `string` (required) - The unique ID of the device.
- `os_type`: `string` (required) - The type of the operating system (e.g., Android, iOS).

#### Example Request

```http
POST /Provider/Devices/RegisterDevice?token="asdasda_s"&device_id=Msdaadsd&os_type=Android
```

#### Response

**Success Response Example**

```json
{
  "status": true,
  "message": "تمت العمليه بنجاح",
  "error": "",
  "Data": null
}
```

**Response Parameters**:

- `status`: `boolean` - The status of the request.
- `message`: `string` - A message indicating the result of the request.
- `error`: `string` - Any error message.
- `Data`: `null` - No additional data is returned.

