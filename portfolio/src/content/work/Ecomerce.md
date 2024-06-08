---
title: Ecomerce/Backend
publishDate: 2019-10-02 00:00:00
img: /assets/stock-4.jpg
img_alt: Soft pink and baby blue water ripples together in a subtle texture.
description: |
  Se estructuró y desplegó un sitio web de comercio electrónico, implementando funciones de autenticación, utilizando contenedores Docker y desplegándolo en la plataforma Render.
tags:
  - E-comerce
  - Nest
  - Auth 0
---

### Resumen
El proyecto es un sitio web de comercio electrónico backend (Nest) donde los usuarios pueden comprar y vender productos en línea. Se estructuró de manera organizada para gestionar usuarios, productos y órdenes de compra de una manera clara y fácil de entender. Además, se implementaron funciones de autenticación para garantizar la seguridad de los usuarios al iniciar sesión y registrarse. Todo el sitio web se desplegó utilizando contenedores Docker en la plataforma Render, lo que significa que está listo para ser utilizado en línea de manera eficiente y segura.

### Deploy

https://nest-demo-latest-4y3q.onrender.com/api

### Estructura del proyecto

El proyecto sigue la estructura de directorios recomendada por NestJS. A continuación, se presenta un resumen de los directorios más importantes:

- Estructura del proyecto:
  - `auth`: Maneja los servicios de signin y signup.
  - `file-upload`: Se usa Cloudinary para la carga de archivos y generar un URL.
  - `users`: Controla la lógica de usuarios, protege rutas según la autenticación, y utiliza DTO.
  - `decorators`: Es un decorador personalizado donde se define el rol del usuario (admin o user).
  - `middlewares`: Se utiliza un middleware global para indicar la ruta, fecha y hora.
  - `products`: Controla la lógica de los productos y protege las rutas según la autenticación.
  - `orders`: Controla la lógica de las órdenes que realizan los usuarios, protege las rutas según la autenticación y utiliza DTO.
  - `categories`: Agrega categorías de productos.
 

### Módulos y funcionalidades

#### Autenticación y autorización

El módulo `auth` se encarga de la autenticación y autorización de usuarios. Incluye los siguientes archivos:

- `auth.controller.ts`: Controlador para manejar rutas relacionadas con la autenticación.
- `auth.guard.ts`: Guardia de autenticación para proteger rutas.
- `auth.service.ts`: Servicio para manejar la lógica de autenticación.
- `roles.enum.ts`: Enumeración de roles de usuario.

#### Carga de archivos

El módulo `file-upload` permite cargar archivos en la aplicación. Incluye los siguientes archivos:

- `file-upload.controller.ts`: Controlador para manejar rutas relacionadas con la carga de archivos.
- `file-upload.module.ts`: Módulo que configura el servicio de carga de archivos.
- `file-upload.service.ts`: Servicio para manejar la lógica de carga de archivos.
- `file-upload.repository.ts`: Repositorio para almacenar información de los archivos cargados.

#### Usuarios

El módulo `users` gestiona los usuarios de la aplicación. Incluye los siguientes archivos:

- `users.controller.ts`: Controlador para manejar rutas relacionadas con los usuarios.
- `users.dto.ts`: Objetos de transferencia de datos (DTO) para definir las entradas y salidas de datos.
- `users.module.ts`: Módulo que configura el servicio de usuarios.
- `users.repository.ts`: Repositorio para almacenar y recuperar información de los usuarios.
- `users.service.ts`: Servicio para manejar la lógica de los usuarios.

#### Productos

El módulo `products` gestiona los productos de la aplicación. Incluye los siguientes archivos:

- `products.controller.ts`: Controlador para manejar rutas relacionadas con los productos.
- `products.dto.ts`: Objetos de transferencia de datos (DTO) para definir las entradas y salidas de datos.
- `products.module.ts`: Módulo que configura el servicio de productos.
- `products.repository.ts`: Repositorio para almacenar y recuperar información de los productos.
- `products.service.ts`: Servicio para manejar la lógica de los productos.

#### Ordenes

El módulo `orders` gestiona los ordenes de la aplicación. Incluye los siguientes archivos:

- `orders.controller.ts`: Controlador para manejar rutas relacionadas con los Ordenes.
- `orders.dto.ts`: Objetos de transferencia de datos (DTO) para definir las entradas y salidas de datos.
- `orders.module.ts`: Módulo que configura el servicio de Ordenes.
- `orders.repository.ts`: Repositorio para almacenar y recuperar información de los Ordenes.
- `orders.service.ts`: Servicio para manejar la lógica de los Ordenes.


### Endpoints

##### Autenticación

- POST /auth/login: Realiza el inicio de sesión de un usuario.
- POST /auth/register: Registra un nuevo usuario.

##### Usuarios

- GET /users: Obtiene una lista de usuarios.
- GET /users/:id: Obtiene un usuario específico por su ID.
- PUT /users/:id: Actualiza un usuario específico por su ID.
- DELETE /users/:id: Elimina un usuario específico por su ID.

##### Productos

- GET /products: Obtiene una lista de productos.
- GET /products/:id: Obtiene un producto específico por su ID.
- POST /products: Crea un nuevo producto.
- PUT /products/:id: Actualiza un producto específico por su ID.
- DELETE /products/:id: Elimina un producto específico por su ID.

##### Órdenes

- GET /orders: Obtiene una lista de órdenes.
- GET /orders/:id: Obtiene una orden específica por su ID.
- POST /orders: Crea una nueva orden.
- PUT /orders/:id: Actualiza una orden específica por su ID.
- DELETE /orders/:id: Elimina una orden específica por su ID.