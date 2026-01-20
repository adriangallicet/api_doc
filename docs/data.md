
# 📊 Datos y Metricas

Este módulo permite registrar y consultar los datos generados por los dispositivos IoT.  
Los datos representan estados reportados por un dispositivo en un momento determinado.

## Relación con la API

Los dispositivos envían información a la API utilizando el endpoint de creación de datos.  
Posteriormente, estos datos pueden ser consultados para análisis o visualización.

## Métodos disponibles a endpoint único

- `GET /data`
- `POST /data`

## POST /data

Registra un nuevo dato enviado por un dispositivo.

Este endpoint es utilizado para registrar un cambio de estado en uno de los actuadores del dispositivo IoT. <br>Puntualmente un estado alto, es decir, encendido del dispositivo que se hace control mediante el relé.
### Headers
token: { jwt }

### Body
```json
{
  "locationName": "hospital centenario",
  "deviceName": "pasillo central",
  "deviceId": "675cb7729919b5f06e5ad5a4",
  "habitacion": "101",
  "valor": 1000,
  "createdTime": 1735330059103
}
```

### Response 201 created
```json
{
  "status": "success",
  "message": "Data saved successfully"
}
```

### Errores

500 → Error de servidor
```json
{
  "status": "error",
  "message": "Failed to save data"
}
```


## GET /data

Obtiene los datos asociados a un Usuario

### Headers
token: { jwt }

### Query params
```
period=anual

URL completa:
http://localhost:3001/api/data?period=anual
```

### Response 200
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

### Errores

400 → Bad request

```json
{
  "status": "error",
  "message": "Periodo no válido. Debe ser semanal o anual"
}
```
404 → Not Found
```json
{
  "status": "error",
  "message": "No se encontraron datos para el periodo solicitado"
}
```
500 → Error de servidor
```json
{
  "status": "error",
  "message": "Error al obtener los datos"
}
```

<br>

⬅️ [Volver a Locaciones](locations.md) - [Webhooks](webhooks.md) ➡️ 
