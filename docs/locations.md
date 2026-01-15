# 📍 Locaciones

## GET /location

Obtiene las locaciones del usuario.

---

## POST /location

### Body
```json
{
  "location": {
    "name": "Casa",
    "description": "Mi casa"
  }
}
```
## DELETE /location
### Query Params
```
locationId=<mongo_id>
```
