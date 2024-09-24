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