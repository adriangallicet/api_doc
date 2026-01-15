# 📡 IoT API Documentation

API REST para la gestión de usuarios, dispositivos IoT, locaciones y métricas.

---

## 🌐 Base URL

http://localhost:3001/api

---

## 🔐 Autenticación

La API utiliza **JWT (JSON Web Token)**.

- El token se obtiene al hacer login
- El token debe enviarse en los headers de cada request protegido

token: <jwt>

---

## 📦 Tecnologías

- Node.js
- Express
- MongoDB
- Mongoose
- JWT

## 📘 Contenido

- [🔐 Autenticación](auth.md)
- [👤 Usuarios](users.md)
- [📟 Dispositivos](devices.md)
- [📍 Locaciones](locations.md)
- [📊 Datos y métricas](data.md)
- [🔗 Webhooks](webhooks.md)
- [📦 Modelos](models.md)

---

