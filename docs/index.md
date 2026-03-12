# 📡 API IoT

Documentación de la API REST para la gestión de usuarios, dispositivos IoT, locaciones y métricas.

Este repositorio forma parte del proyecto **Plataforma IoT**, desarrollado como trabajo de tesis de Ingeniería en<br> Telecomunicaciones.
El repositorio principal del proyecto funciona como punto de acceso a la documentación<br> general y a los distintos componentes del sistema:
🔗 https://github.com/adriangallicet/tesis-plataforma-iot 


## ¿Qué es una API REST?

Una **API REST** (Representational State Transfer) es una interfaz que permite que distintas aplicaciones se<br> comuniquen entre sí a través de **HTTP**, utilizando reglas y convenciones simples.

En una API REST:

- Cada **recurso** (usuarios, dispositivos, datos, etc.) se accede mediante una **URL**
- Se utilizan los métodos HTTP estándar:
  - **GET** → obtener información
  - **POST** → crear información
  - **PUT** → actualizar información
  - **DELETE** → eliminar información
- Las respuestas suelen enviarse en formato **JSON**
- El servidor no guarda estado entre peticiones (stateless)


## ¿Cómo funciona esta API REST?
  <img src="assets/rest-diagrama.jpg" alt="Diagrama de funcionamiento" width="70%">


Ella permite:

- Registrar y autenticar usuarios
- Gestionar dispositivos IoT
- Asociar dispositivos a locaciones
- Almacenar y consultar generados por los dispositivos
- Exponer endpoints para integración con dispositivos IoT

Todas las peticiones se realizan sobre la siguiente URL base:




## 🌐 Base URL

http://localhost:3001/api


## 📦 Tecnologías

- Node.js
- Express
- MongoDB
- Mongoose
- JWT

## 📘 Contenido
- [👤 Usuarios](users.md)
- [🔐 Autenticación](auth.md)
- [📟 Dispositivos](devices.md)
- [📍 Locaciones](locations.md)
- [📊 Datos y métricas](data.md)
- [🔗 Webhooks](webhooks.md)
- [📦 Modelos](models.md)


<br>

   [Usuarios](users.md) ➡️ 

