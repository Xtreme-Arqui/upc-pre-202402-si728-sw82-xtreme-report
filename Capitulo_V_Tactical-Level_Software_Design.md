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

## 5.4 Bounded Context Reservation
### 5.4.1 Domain Layer
- Entidades Principales: Reservación, Política de Reservación.
- Objetos de Valor: Fecha de Reservación, Detalles de la Reservación.
- Servicios de Dominio: Gestión de Reservaciones.
- Repositorios: Repositorio de Reservaciones.

### 5.4.2 Interface Layer
- APIs:
  - POST /reservaciones (para crear nuevas reservaciones)
  - GET /reservaciones/{id} (para obtener detalles de una reservación)
  - PUT /reservaciones/{id} (para actualizar una reservación)
  - DELETE /reservaciones/{id} (para cancelar una reservación)
- Controladores: ReservacionController (gestiona las operaciones relacionadas con reservaciones).
- Event Handlers: ReservationUpdatedEventHandler (maneja eventos de actualización de reservaciones).

### 5.4.3 Application Layer
- Servicios de Aplicación:
  - ReservacionService (gestiona la creación, actualización, consulta y cancelación de reservaciones).
- Comandos: CreateReservationCommand, UpdateReservationCommand, DeleteReservationCommand.
- Eventos de Dominio: ReservationCreated, ReservationUpdated, ReservationCancelled

### 5.4.4 Infrastructure Layer
- Implementación de Repositorios: ReservacionRepositoryImpl (implementación con acceso a base de datos).
- Integraciones: Integraciones con sistemas de calendario o plataformas de gestión de eventos para sincronizar reservaciones.
- Proveedores de Datos: Proveedores para almacenamiento de información de reservación

### 5.4.6 Bounded Context Software Architecture Component Level Diagrams
<img src="./Resources/images/5.4.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.4.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.4.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.4.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.4.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.4.7.2 Bounded Context Database Design Diagram.PNG">

## 5.5 Bounded Context IoT Monitoring
### 5.5.1 Domain Layer
- Entidades Principales: Dispositivo, Evento de Monitoreo.
- Objetos de Valor: Ubicación GPS, Métricas de Sensores (como temperatura, pasos, ritmo cardíaco).
- Servicios de Dominio: Gestión de Dispositivos, Análisis de Datos de Sensores.
- Repositorios: Repositorio de Dispositivos, Repositorio de Eventos de Monitoreo.

### 5.5.2 Interface Layer
- APIs:
  - POST /dispositivos (para registrar nuevos dispositivos IoT)
  - GET /dispositivos/{id} (para obtener datos de un dispositivo)
  - POST /eventos (para registrar eventos de monitoreo)
- Controladores: DispositivoController, EventoMonitoreoController (gestionan las operaciones relacionadas con dispositivos y eventos de monitoreo).
- Event Handlers: DeviceDataReceivedEventHandler (maneja la recepción de datos de dispositivos).

### 5.5.3 Application Layer
- Servicios de Aplicación:
- DispositivoService (gestiona la configuración y el estado de los dispositivos IoT).
- MonitoreoService (analiza los datos recibidos de los dispositivos).
- Comandos: RegisterDeviceCommand, LogEventCommand.
- Eventos de Dominio: DeviceRegistered, MonitoringEventLogged.

### 5.5.4 Infrastructure Layer
- Implementación de Repositorios: DispositivoRepositoryImpl, EventoMonitoreoRepositoryImpl (implementaciones con acceso a base de datos).
- Integraciones: Integraciones con plataformas de IoT para recibir datos de sensores.
- Proveedores de Datos: Almacenes de datos para la persistencia de información de dispositivos y eventos.

### 5.5.6 Bounded Context Software Architecture Component Level Diagrams
<img src="./Resources/images/5.5.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.5.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.5.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.5.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.5.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.5.7.2 Bounded Context Database Design Diagram.PNG">

## 5.6 Bounded Context Subscription
### 5.6.1 Domain Layer
- Entidades Principales: Suscripción, Plan de Suscripción.
- Objetos de Valor: Fecha de Suscripción, Precio.
- Servicios de Dominio: Gestión de Suscripciones.
- Repositorios: Repositorio de Suscripciones.

### 5.6.2 Interface Layer
- APIs:
  - POST /suscripciones (para crear nuevas suscripciones)
  - GET /suscripciones/{id} (para obtener detalles de una suscripción)
  - PUT /suscripciones/{id} (para actualizar una suscripción)
  - DELETE /suscripciones/{id} (para cancelar una suscripción)
- Controladores: SuscripcionController (gestiona las operaciones relacionadas con suscripciones).
- Event Handlers: SubscriptionUpdatedEventHandler (maneja eventos de actualización de suscripciones).

### 5.6.3 Application Layer
- Servicios de Aplicación:
- SuscripcionService (gestiona la creación, actualización y cancelación de suscripciones).
- PlanService (gestiona la lógica de negocio de los planes de suscripción).
- Comandos: CreateSubscriptionCommand, UpdateSubscriptionCommand, CancelSubscriptionCommand.
- Eventos de Dominio: SubscriptionCreated, SubscriptionUpdated, SubscriptionCancelled

### 5.6.4 Infrastructure Layer
- Implementación de Repositorios: SuscripcionRepositoryImpl, PlanRepositoryImpl (implementaciones con acceso a base de datos).
- Integraciones: Integraciones con plataformas de pago para gestionar pagos recurrentes y renovaciones.
- Proveedores de Datos: Almacenes de datos para la persistencia de información de suscripciones y planes.

### 5.6.6 Bounded Context Software Architecture Component Level Diagrams
<img src="./Resources/images/5.6.6 Bounded Context Software Architecture Component Level Diagrams.PNG">

### 5.6.7 Bounded Context Software Architecture Code Level Diagrams
#### 5.6.7.1 Bounded Context Domain Layer Class Diagrams
<img src="./Resources/images/5.6.7.1 Bounded Context Domain Layer Class Diagrams.PNG">

#### 5.6.7.2 Bounded Context Database Design Diagram
<img src="./Resources/images/5.6.7.2 Bounded Context Database Design Diagram.PNG">