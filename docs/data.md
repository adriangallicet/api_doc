
# 📊 Datos y Métricas

## POST /data

Guarda una medición.

### Body
```json
{
  "locationName": "Casa",
  "deviceName": "Sensor Temp",
  "deviceId": "device-001",
  "habitacion": "Living",
  "valor": 23.5,
  "createdTime": 1700000000000
}

```
## GET /data

Devuelve métricas agregadas.

### Query Params
```
period=semanal | anual

```
### Response

```json
{
  "status": "success",
  "data": {
    "totalRevenue": 120,
    "totalSales": 10,
    "totalLocations": 2,
    "totalDevices": 5,
    "dataForChart": [
      { "name": "lun", "total": 20 }
    ],
    "recentCount": 10
  }
}

```
