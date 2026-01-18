# 📟 Dispositivos

Este módulo permite gestionar los dispositivos IoT del sistema.  
Un dispositivo representa un equipo físico con uno o más actuadores, asociado a una ubicación.

## Vista en la aplicación

![Vista del módulo de dispositivos](assets/Dispositivos.jpg)

### Relación con la API

El formulario **Nuevo dispositivo** utiliza el endpoint:

- `POST /device`

Campos enviados:
- `name` → Nombre del dispositivo
- `dId` → Identificador único
- `denomination` → Código interno
- `actuators` → Número de actuadores
- `location` → ID de la locación



## Endpoints disponibles

- `GET /device`
- `POST /device`
- `DELETE /device`


## GET /device

Obtiene todos los dispositivos registrados del usuario autenticado.

### Headers
token: { jwt }


### Response 200
```json
{
  "status": "success",
  "devices": [
    {
      "dId": "device-001",
      "name": "Sensor",
      "location": "Casa",
      "actuators": 0
    }
  ]
}



```
Errores

401 → No autorizado

## POST /device

Registra un nuevo dispositivo.

### Headers
token: { jwt }

```json
Body
{
  "dId": "device-002",
  "name": "Luz",
  "denomination": "100",
  "actuators": 1,
  "location": "loc-001"
}
```

### Response 200
```json
{
  "status": "success"
}
```

### Errores

400 → Datos inválidos

409 → Dispositivo duplicado

500 → Error de servidor

## DELETE /device

Elimina un dispositivo existente.
### Query Params
```
dId=device-001

Request completa:
http://localhost:3001/api/device?dId=device-001
```
### Response 200
```json
{
  "status": "success"
}
```
### Errores

404 → Dispositivo no encontrado

401 → No autorizado
<br>

⬅️ [Volver a Usuarios](users.md) - [Locaciones](locations.md) ➡️ 


