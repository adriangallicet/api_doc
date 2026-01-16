# 🔗 Webhooks / IoT

## POST /getdevicecredentials

Endpoint utilizado por dispositivos IoT.

### Body
```json
{
  "dId": "device-001",
  "_id": "mongo_id"
}

```

### Response

```json
{
  "topic": "userId/deviceId/",
  "actuators": []
}

```

---

| ⬅️ [volver a Datos y Metricas](data.md) | [Modelos](models.md) ➡️ |
|:--|--:|
