# 🔐 Autenticación

Esta API utiliza cookies HttpOnly para manejar la autenticación del usuario.

Cuando un usuario inicia sesión correctamente, el servidor genera un JWT y lo guarda en una cookie llamada auth_token.
Esta cookie es almacenada por el navegador al iniciar sesión y se envía automáticamente en cada solicitud al servidor,
sin necesidad de especificar ningún header manual.

¿Cómo funciona?

- El token NO se guarda en localStorage

- El token NO se envía en headers

- El token NO es accesible desde JavaScript

- El navegador envía automáticamente la cookie en cada request


### Relación con la API

Las pantallas de login y registro utilizan los siguientes métodos:

- `POST /login`
- `POST /logout`
- `GET /verify`


## Endpoints disponibles

- `/login`
- `/logout`
- `/verify`


## POST /login
Inicia sesión y establece una cookie de autenticación.

## Vista en la aplicación

  <img src="assets/login.jpg" alt="Vista de autenticación" width="65%">


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
  "userData": {
    "_id": "...",
    "name": "Juan",
    "email": "user@mail.com"
  }
}
```
✔ El servidor setea automáticamente la cookie auth_token.

### Errores

401 → Credenciales inválidas
```json
{
  "status": "error",
  "error": "Invalid Credentials"
}
```
## GET /verify

Verifica si el usuario tiene una sesión válida usando la cookie y devuelve sus datos básicos-

### Response 200

```json
{
  "status": "success",
  "userData": {
    "_id": "...",
    "name": "Juan",
    "email": "user@mail.com"
  }
}
```
### Errores
401 → credenciales invalidas
```json
{
  "status": "error",
  "error": { error }
}
```
## POST /logout

Cierra la sesión eliminando la cookie de autenticación.

### Response 200
```json
{
  "status": "success"
}
```
✔ El servidor elimina la cookie auth_token.

## 📦 Endpoints protegidos

Todos los endpoints protegidos siguen esta regla:

No usan token en headers

Usan la cookie HttpOnly automáticamente

Si la cookie no es válida → 401 Unauthorized

## 🔐 Seguridad

Cookies configuradas con:

- httpOnly: true

- secure: true

- sameSite: none

El token no es accesible desde JavaScript

Protección frente a XSS

## 📝 Notas finales

Esta API no utiliza localStorage

No es necesario manejar tokens manualmente

El manejo de sesión es transparente para el cliente

<br>

⬅️ [Volver a Usuarios](users.md) - [Dispositivos](devices.md) ➡️ 




















