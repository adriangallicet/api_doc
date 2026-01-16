
# 📟 Dispositivos

Todos los endpoints requieren autenticación.

---

## GET /device

Obtiene los dispositivos del usuario autenticado.

### Headers
token: jwt


### Response
```json
{
  "status": "success",
  "data": [
    {
      "_id": "...",
      "dId": "device-001",
      "name": "Sensor",
      "actuators": [],
      "locationName": "Casa"
    }
  ]
}
```
## POST /device

Crea un nuevo dispositivo.

### Body
```json
{
  "newDevice": {
    "dId": "device-001",
    "name": "Sensor",
    "locationId": "123",
    "locationName": "Casa",
    "actuators": []
  }
}

```
## PUT /device

Actualiza el valor de un actuador.

### Body

```json
{
  "dId": "mongo_device_id",
  "actuatorId": "relay1",
  "newValue": true
}


```
## DELETE /device
### Query Params
```
dId=device-001
```
<br>

⬅️ [Volver a Usuarios](users.md) [Locaciones](locations.md) ➡️ 


