

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
### Errores
Email duplicado

Error de servidor

