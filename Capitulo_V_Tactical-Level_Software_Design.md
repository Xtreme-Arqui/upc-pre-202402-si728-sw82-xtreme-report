# Capítulo V: Tactital-Level Software Design

## 5.1. Bounded Context Account

### 5.1.1. Domain Layer

- Entidades Principales: Usuario, Rol, Permiso.
- Objetos de Valor: Dirección de Email, Nombre de Usuario.
- Servicios de Dominio: Gestión de Autenticación, Gestión de Roles.
- Repositorios: Repositorio de Usuarios, Repositorio de Roles.

### 5.1.2 Interface Layer

- APIs:
  - POST /usuarios/registro (para registrar nuevos usuarios)
  - POST /usuarios/login (para iniciar sesión)
  - GET /usuarios/{id} (para obtener información del usuario)
- Controladores: UsuarioController (gestiona las operaciones de usuarios).
- Event Handlers: UserCreatedEventHandler (maneja eventos post-creación de usuario).

### 5.1.3 Application Layer

- Servicios de Aplicación:
    - UsuarioService (gestiona la creación, autenticación y actualización de usuarios).
    - SeguridadService (encargado de la seguridad y la encriptación de datos).
- Comandos: CreateUserCommand, UpdateUserCommand.
- Eventos de Dominio: UserCreated, UserUpdated.

### 5.1.4 Infrastructure Layer

- Implementación de Repositorios: UsuarioRepositoryImpl (implementación con acceso a base de datos).
- Integraciones: Servicios de terceros para verificación de email, SMS para autenticación de dos factores.
- Proveedores de Datos: Proveedores para almacenamiento de información de usuario encriptada.

### 5.1.6 Bounded Context Software Architecture Component Level Diagrams

Este diagrama incluiría la conexión entre controladores, servicios de aplicación, y entidades del dominio, así como las interacciones con sistemas externos para autenticación y verificación.

<img src="./Resources/images//5.1.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.1.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.1.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.1.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.1.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.1.7.2 Bounded Context Database Design Diagram.PNG">

## 5.2 Bounded Context Agency

### 5.2.1 Domain Layer
- Entidades Principales: Agencia, Perfil de Agencia.
- Objetos de Valor: Dirección, Contacto.
- Servicios de Dominio: Gestión de Agencias.
- Repositorios: Repositorio de Agencias.

### 5.2.2 Interface Layer
- APIs:
  - POST /agencias (para crear nuevas agencias)
  - GET /agencias/{id} (para obtener detalles de una agencia)
  - PUT /agencias/{id} (para actualizar una agencia)
- Controladores: AgenciaController (gestiona las operaciones relacionadas con agencias).
- Event Handlers: AgencyProfileUpdatedEventHandler (maneja eventos de actualización de perfiles).

### 5.2.3 Application Layer
- Servicios de Aplicación:
  - AgenciaService (gestiona la creación, actualización y visualización de agencias).
- Comandos: CreateAgencyCommand, UpdateAgencyCommand.
- Eventos de Dominio: AgencyCreated, AgencyUpdated.

### 5.2.4 Infrastructure Layer
- Implementación de Repositorios: AgenciaRepositoryImpl (implementación con acceso a base de datos).
- Integraciones: Servicios de terceros para validación de datos de contacto o ubicación.
- Proveedores de Datos: Proveedores para almacenamiento de información de agencia.

### 5.2.6 Bounded Context Software Architecture Component Level Diagrams
<img src="./Resources/images/5.2.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.2.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.2.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.2.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.2.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.2.7.2 Bounded Context Database Design Diagram.PNG">

## 5.3 Bounded Context Service
### 5.3.1 Domain Layer
- Entidades Principales: Servicio, Categoría de Servicio.
- Objetos de Valor: Descripción de Servicio, Precio.
- Servicios de Dominio: Gestión de Servicios.
- Repositorios: Repositorio de Servicios.

### 5.3.2 Interface Layer
- POST /servicios (para agregar nuevos servicios)
- GET /servicios/{id} (para obtener detalles de un servicio)
- PUT /servicios/{id} (para actualizar un servicio)
- DELETE /servicios/{id} (para eliminar un servicio)
- Controladores: ServicioController (gestiona las operaciones relacionadas con servicios).
- Event Handlers: ServiceUpdatedEventHandler (maneja eventos de actualización de servicios).

### 5.3.3
- Servicios de Aplicación:
  - ServicioService (gestiona la creación, actualización, eliminación y consulta de servicios).
- Comandos: CreateServiceCommand, UpdateServiceCommand, DeleteServiceCommand.
- Eventos de Dominio: ServiceCreated, ServiceUpdated, ServiceDeleted.

### 5.3.4
- Implementación de Repositorios: ServicioRepositoryImpl (implementación con acceso a base de datos).
- Integraciones: Integraciones con sistemas de facturación o plataformas de pago para gestionar los precios y transacciones de los servicios.
- Proveedores de Datos: Proveedores para almacenamiento de información de servicio.

### 5.3.6 Bounded Context Software Architecture Component Level Diagrams
<img src="./Resources/images/5.3.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.3.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.3.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.3.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.3.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.3.7.2 Bounded Context Database Design Diagram.PNG">

