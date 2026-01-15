# 🔐 Autenticación

## POST /login

Inicia sesión y devuelve un token JWT.

### Body
```json
{
  "email": "user@mail.com",
  "password": "password"
}

```

### Response 200

```json
{
  "status": "success",
  "token": "jwt_token",
  "userData": {
    "_id": "...",
    "name": "Juan",
    "email": "user@mail.com"
  }
}
```

### Errores
401 → Credenciales inválidas

### GET /verify

Verifica si el token es válido.

### Headers
```makefile
token: <jwt>
```
### Response 200
```json
{
  "status": "success"
}

```

















