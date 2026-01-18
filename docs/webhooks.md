# 🔔 Webhooks

El objetivo de este módulo es responder a las solicitudes de configuracion que realizan los dispositivos.


## Relación con la API

Los dispositivos IoT no poseen guardada ningún tipo de configuracion en memoria. Por lo tanto, al encender, solicitan
lo necesario para llevar a cabo su tarea:
- `tópico Mqtt raíz al cual deben suscribirse para poder comunicarse con el sistema para recepción y envío`
- `número de actuadores que debe controlar`

## Método único a único endpoint

- `POST /getDevicecredentials`


## POST /getDevicecredentials

Dispositivo obtiene la configuración necesaria en base a la combinación única de dId, el cual es introducido por el usuario a la hora de crear el dispositivo
e _id valor asignado por la propia BD al crear la entrada en la colección.

### Body
```json
{
  "dId": "device-001",
  "_id": "675cb7729919b5f06e5ad5a4"
}
```
### Response 200
```json
{
  "topic": "userId/deviceId/",
  "actuators": []
}
```

### Errores

401 → Credenciales inválidas
- `El dispositivo debe existir en BD, y la combinación dID e _id debe coincidir`


<br>

⬅️ [Volver a Datos y Métricas](data.md) - [Modelos](models.md) ➡️ 
