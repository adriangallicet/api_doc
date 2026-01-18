

# 👤 Usuarios

## POST /register

Registra un nuevo usuario.

### Body
```json
{
  "name": "Juan",
  "email": "juan@mail.com",
  "password": "password"
}
```

### Response
```json
{
  "status": "success"
}
```
## Errores
Existen 2 posibles errores:
- El email debe ser único para evitar datos duplicados.
- Error de servidor


<br>

⬅️ [Volver a Autenticacion](auth.md) - [Dispositivos](devices.md) ➡️ 

