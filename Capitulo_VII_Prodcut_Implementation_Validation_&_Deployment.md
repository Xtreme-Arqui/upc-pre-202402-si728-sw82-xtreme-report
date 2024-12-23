# Capitulo VII: Product Implementation, Validation & Deployment
En esta sección, como equipo, explicamos y evidenciamos el proceso de implementar, comprobar, desplegar y validar la solución compuesta por los productos digitales que forman parte del alcance. Este capítulo abarca secciones para la organización del proceso de trabajo en Sprints, la descripción y prácticas asociadas a Software Configuration Management, el Video About-The-Product y las evidencias de Implementation, Testing, Deployment y Validations para cada uno de los productos, en términos del producto en sí y la colaboración por Sprint.
## 7.1. Software Configuration Management
En esta sección, como equipo, establecemos las decisiones y convenciones que permitirán mantener la consistencia durante el ciclo de vida del proyecto. Incluimos secciones internas para Source Code Management, Development Environment Configuration y Deployment Configuration, asegurando que todos los aspectos del desarrollo y despliegue del software estén bien organizados y documentados.
### 7.1.1. Software Development Environment Configuration.
En esta sección, como equipo, especificamos y describimos los productos de software que utilizaremos en el proyecto, indicando su propósito y cómo acceder a ellos. Esto incluye herramientas para Project Management, Requirements Management, Product UX/UI Design, Software Development, Software Testing, Software Deployment y Software Documentation. Nuestro objetivo es asegurar que todos los miembros del equipo tengan acceso a las herramientas necesarias para colaborar eficazmente en el ciclo de vida del proyecto.

**Project Management:**
1. **Markdown**

    -   **Propósito:** Crear y organizar la documentación del proyecto en archivos .md, permitiendo una fácil segmentación por capítulos. Facilita la generación de informes en PDF para entregas académicas.
    - **Ruta:** Sintaxis básica de escritura y formato en GitHub

2. **Git & GitHub**

    - **Propósito:** Sistema de control de versiones distribuido para rastrear cambios en el código fuente y facilitar la colaboración entre los miembros del equipo.
    - **Ruta de descarga Git:** https://git-scm.com/downloads
    - **Ruta GitHub:** https://github.com/

3. **Discord**

    - **Propósito:** Plataforma de comunicación y colaboración para llamadas, chat en tiempo real y compartir archivos entre los miembros del equipo.
    - **Ruta:** https://discord.com/download

4. **Trello**

    - **Propósito:** Herramienta de gestión de proyectos basada en tableros Kanban para organizar tareas, asignar responsabilidades y hacer seguimiento del progreso del proyecto.
    - **Ruta:** https://trello.com/

**Product UX/UI Design:**

5. **Miro**

    - **Propósito:** As-Is y To-Be Scenario Maps
    - **Ruta:** https://miro.com/es/

6. **Figma**

    - **Propósito:** Diseño colaborativo de interfaces de usuario, creación de wireframes, mockups y prototipos interactivos.
    - **Ruta:** https://www.figma.com/

7. **Lucidchart**

    - **Propósito:** Creación de diagramas de flujo, mapas mentales y diagramas de arquitectura para visualizar procesos y estructuras del proyecto.
    - **Ruta:** https://www.lucidchart.com/

8. **Vertabelo**

    - **Propósito:** Herramienta gratuita para la elaboración de diagramas de base de datos.
    - **Ruta:** https://vertabelo.com/

9. **Structurizr**

    - **Propósito:** Elaboración de diagramas C4.
    - **Ruta:** https://structurizr.com/

10. **UXPressia**

    - **Propósito:** Elaboración de User Personas, Empathy Maps, Journey Maps e Impact Maps.
    - **Ruta:** https://uxpressia.com/

**Software Development:**

11. Visual Studio Code

    - **Propósito:** Editor de código principal para el desarrollo del frontend y backend, con extensiones para mejorar la productividad.
    - **Ruta de descarga:** https://code.visualstudio.com/

12. **Angular CLI**

    - **Propósito:** Framework para el desarrollo del frontend de la aplicación web, facilitando la creación de componentes y servicios.
    - **Instalación:** Ejecutar npm install -g @angular/cli después de instalar Node.js

13. **Spring Boot**

    - **Propósito:** Framework para el desarrollo del backend, proporcionando un entorno preconfigurado para aplicaciones Java.
    - **Ruta:** https://spring.io/projects/spring-boot

**Software Deployment:**

14. **GitHub Pages**

    - **Propósito:** Desplegar la landing Page.
    - **Ruta:** https://pages.github.com/

15. **Netify**

    - **Propósito:** Desplegar la Aplicacion Web
    - **Ruta:** https://www.netlify.com

**Software Documentation:**

16. **Swagger UI**
    - **Propósito:** Herramienta para documentar y probar APIs RESTful generadas con Spring Boot.
    - **Configuración:** Integrada en el proyecto Spring Boot mediante dependencias Maven.

### 7.1.2. Source Code Management.
Nuestro equipo ha adoptado GitHub como plataforma principal para el control de versiones y la gestión del código fuente. Implementamos una estrategia de ramificación basada en GitFlow, adaptada a nuestras necesidades específicas, para garantizar un flujo de trabajo eficiente y una gestión de código robusta.

**Repositorios de GitHub**

Hemos establecido los siguientes repositorios para nuestros productos:

1. **Landing Page:** https://github.com/Xtreme-Arqui/landing-page-Aventurero

2. **Frontend Web Application:** https://github.com/Xtreme-Arqui/Frontend

3. **Documentación del Proyecto:** https://github.com/Xtreme-Arqui/upc-pre-202402-si728-sw82-xtreme-report

4. **Backend Aplication:** https://github.com/Xtreme-Arqui/back

**Implementación de GitFlow**

Nuestra implementación de GitFlow se basa en el modelo propuesto por Vincent Driessen, con algunas adaptaciones para optimizar nuestro flujo de trabajo:

1. **Rama Principal (main):**

    - **Denominación:** main
    - **Propósito:** Representa el estado de producción actual.
    - **Características:** Siempre estable y lista para despliegue.

2. **Rama de Desarrollo (develop):**

    - **Denominación:** develop
    - **Propósito:** Integra las últimas características desarrolladas.
    - **Características:** Punto de partida para nuevas funcionalidades, sometida a pruebas continuas.

3. **Ramas de Funcionalidades (feature branches):**

    - **Denominación:** feature/nombre-de-la-funcionalidad
    - **Propósito:** Desarrollo aislado de nuevas características.
    - **Características:** Se ramifican desde develop y se fusionan de vuelta a ella.

4. **Ramas de Lanzamiento (release branches):**

    - **Denominación:** release/v{X.Y.Z}
    - **Propósito:** Preparación para un nuevo lanzamiento de producción.
    - **Características:** Permite ajustes finales y correcciones menores antes del lanzamiento.

5. **Ramas de Corrección Urgente (hotfix branches):**

    - **Denominación:** hotfix/v{X.Y.Z+1}
    - **Propósito:** Correcciones críticas en producción.
    - **Características:** Se ramifican desde main y se fusionan tanto en main como en develop.

**Convenciones de Nomenclatura**

1. **Ramas de Funcionalidades:**

    - **Formato:** feature/breve-descripcion-de-la-funcionalidad
    - **Ejemplo:** feature/integracion-sensor-temperatura

2. **Ramas de Lanzamiento:**

    - **Formato:** release/vX.Y.Z
    - **Ejemplo:** release/v1.2.0

3. **Ramas de Corrección Urgente:**

    - **Formato:** hotfix/vX.Y.Z
    - **Ejemplo:** hotfix/v1.2.1

**Versionado Semántico**

Adoptamos el Versionado Semántico 2.0.0 para nuestros lanzamiento:

- **X (Major):** Cambios incompatibles con versiones anteriores
- **Y (Minor):** Nuevas funcionalidades compatibles con versiones anteriores
- **Z (Patch):** Correcciones de errores compatibles con versiones anteriores

**Convenciones para Commits**

Seguimos las directrices de Conventional Commits para mantener un historial de cambios claro y estructurado:

    <tipo>[alcance opcional]: <descripción>

    [cuerpo opcional]

    [notas de pie opcionales]

Tipos de commits más comunes:

- `feat`: Nueva funcionalidad
- `fix`: Corrección de errores
- `docs`: Cambios en la documentación
- `style`: Cambios que no afectan el significado del código (espacios en blanco, formato, etc.)
- `refactor`: Cambio de código que no corrige un error ni añade una característica
- `test`: Adición o modificación de pruebas
- `chore`: Cambios en el proceso de construcción o herramientas auxiliares

Ejemplos:

- `feat(auth): implementar autenticación de dos factores`
- `fix(sensor): corregir lectura errónea del sensor de altitud`
- `docs(README): actualizar instrucciones de instalación  `  

**Flujo de Trabajo**

1. Los desarrolladores crean ramas de funcionalidades desde develop.
2. Al completar una funcionalidad, se crea un Pull Request para fusionar con develop.
3. Las ramas de lanzamiento se crean desde develop cuando se prepara una nueva versión.
4. Tras las pruebas finales, la rama de lanzamiento se fusiona en main y develop.
5. Si se detectan errores críticos en producción, se crea una rama de corrección urgente desde main.

Esta estructura nos permite mantener un desarrollo ordenado, facilitar la colaboración entre miembros del equipo y garantizar la estabilidad de nuestras versiones de producción.
### 7.1.3. Source Code Style Guide & Conventions.
Para mantener la consistencia y legibilidad de nuestro código a lo largo del proyecto, hemos adoptado las siguientes guías de estilo y convenciones para los diferentes lenguajes y tecnologías que utilizamos. Estas pautas se basan en las mejores prácticas de la industria y se adaptan a las necesidades específicas de nuestro proyecto.

**HTML**

Seguimos las recomendaciones del "HTML Style Guide and Coding Conventions" de W3Schools y el "Google HTML/CSS Style Guide":

1. **Declaración del tipo de documento:**

    -   Siempre incluir al inicio del documento: `<!DOCTYPE html>`

2. **Uso de minúsculas:**

    -   Utilizar minúsculas para todos los nombres de elementos y atributos.
    - Ejemplo: `<body>, <section>, <div class="container">`

3. **Comillas en atributos:**

    - Usar comillas dobles para los valores de los atributos.
    - Ejemplo: `<img src="image.jpg" alt="Descripción de la imagen">`

4. **Indentación:**

    - Utilizar 2 espacios para la indentación.
    - Mantener una estructura clara y jerárquica.

5. **Comentarios:**

- Usar comentarios para explicar secciones complejas o no evidentes.
- Formato: `<!-- Comentario -->`

**CSS**

Adoptamos las siguientes convenciones basadas en el "Google HTML/CSS Style Guide":

1. **Nomenclatura de clases:**

    - Usar kebab-case para los nombres de clases.
    - Ejemplo: `.header-navigation`, `.user-profile`

2. **Selectores:**

    - Evitar selectores demasiado específicos para mejorar la reutilización.
    - Preferir clases sobre IDs para estilos reutilizables.

3. **Propiedades:**

    - Ordenar las propiedades alfabéticamente dentro de cada regla.
    - Usar notación abreviada cuando sea posible.
    - Ejemplo: `margin: 10px 20px;` en lugar de definir cada lado por separado.

4. **Valores:**

    - Omitir unidades para valores cero: `margin: 0;` en lugar de margin: 0px;
    - Usar notación hexadecimal de 3 caracteres cuando sea posible: `#fff` en lugar de `#ffffff`

**JavaScript/TypeScript**

Seguimos las directrices del "Google JavaScript Style Guide" y "Google TypeScript Style Guide":

1. **Nomenclatura:**

    - Variables y funciones: camelCase
    - Clases y tipos: PascalCase
    - Constantes: UPPER_SNAKE_CASE

2. **Declaración de variables:**

    - Preferir `const` sobre `let.` Usar `let` solo cuando sea necesario reasignar.
    - Evitar `var.`

3. **Funciones:**

    - Preferir funciones de flecha para funciones anónimas.
    - Ejemplo: `const suma = (a, b) => a + b;`

4. **Semicolons:**

    - Usar punto y coma al final de cada declaración.

5. **Comillas:**

    - Preferir comillas simples para strings.
    - Usar comillas invertidas para template literals.

**Angular (TypeScript)**

Adoptamos las recomendaciones de la "Angular Style Guide":

1. **Estructura de archivos:**

    - Un componente por archivo.
    - Nombrar archivos siguiendo el patrón: feature-name.type.ts
    - Ejemplo: `user-profile.component.ts, authentication.service.ts`

2. **Componentes:**

    - Usar el decorador @Component con un selector en kebab-case.
    - Ejemplo: `selector: 'app-user-profile'`

3. **Servicios:**

    - Usar el decorador `@Injectable` con `providedIn: 'root'` para servicios singleton.

4. **Módulos:**

    - Agrupar funcionalidades relacionadas en módulos.
    - Nombrar módulos con el sufijo Module.
    - Ejemplo: `UserModule`, `AuthenticationModule`

**Java (Spring Boot)**

Seguimos las convenciones del "Google Java Style Guide" y las recomendaciones de "Spring Boot Features":

1. **Nomenclatura:**

    - Clases: PascalCase
    - Métodos y variables: camelCase
    - Constantes: UPPER_SNAKE_CASE

2. **Organización de paquetes:**

    - Estructura basada en funcionalidades.
    - Ejemplo: `com.iotecnicos.usermanagement`, `com.iotecnicos.authentication`

3. **Anotaciones de Spring:**

    - Usar anotaciones apropiadas: `@RestController`, `@Service`, `@Repository`
    - Configurar componentes con `@Autowired` para inyección de dependencias.

4. **API RESTful:**

    - Usar `@GetMapping`, `@PostMapping`, etc., para definir endpoints.
    - Seguir principios RESTful en el diseño de la API.

**Gherkin (para archivos .feature)**

Adoptamos las "Gherkin Conventions for Readable Specifications":

1. **Estructura:**

    - Usar el formato "Given-When-Then" para los escenarios.
    - Utilizar "And" para pasos adicionales dentro de cada sección.

2. **Lenguaje:**

    - Escribir en inglés, usando un lenguaje claro y conciso.
    - Evitar jerga técnica en las descripciones de escenarios.

3. **Escenarios:**

    - Comenzar cada escenario con "Scenario:" seguido de un título descriptivo.
    - Mantener los escenarios cortos y enfocados en una sola funcionalidad.

Ejemplo:

```gherkin
Feature: User Authentication

Scenario: Successful login
  Given the user is on the login page
  When they enter valid credentials
  And they click the login button
  Then they should be redirected to the dashboard
```

Estas convenciones y guías de estilo nos ayudarán a mantener un código limpio, consistente y fácil de mantener a lo largo de todo el proyecto. Todos los miembros del equipo deben adherirse a estas pautas para asegurar la calidad y uniformidad del código.
### 7.1.4. Software Deployment Configuration.
En esta seccion se mostrara la configuracion que se realizo para el landing page, frontend y backend
1. **Landing Page**
- Primero ingresar al repositorio del Landing Page e ingresar en Settings
<img src="./Resources/images/landing-1.png">

- Segundo seleccionar Pages y escoger la rama main y guardar
<img src="./Resources/images/landing-2.png">

2. **Frontend**
- Primero, ingresar a Netlify y sincronizar nuestra cuenta de github, para acceder a nuestro repositorio
<img src="./Resources/images/front-1.jpg">

- Segundo, otorgar permisos para que Netlify acceda a nuestro repositorio
<img src="./Resources/images/front-2.jpg">

- Tercero, seleccionar el repositorio donde se encuentra el frontend e instalar
<img src="./Resources/images/front-3.jpg">

- Finalmente, se muestra el frontend desplegado
<img src="./Resources/images/front-4.png">

3. **Backend**

- Primero, creamos la base de datos en railway 
<img src="./Resources/images/db-1.jpg">

- Segundo, conectamos la base de datos local a railway
<img src="./Resources/images/db-2.jpg">

- Tercero, creamos el backend en Azure, indicando el nombre y la suscripcion
<img src="./Resources/images/back-1.jpg">

- Cuarto, indicamos la version de Java y la region
<img src="./Resources/images/back-2.jpg">

- Quinto, verificamos que la informacion otorgada sea correcta y vamos a deployment
<img src="./Resources/images/back-3.jpg">

- Sexto, sincronizamos nuestra cuenta de Github con Azure para acceder al repositorio y colocamos los campos requeridos
<img src="./Resources/images/back-4.jpg">

- Septimo, una vez creado nos mostrara si se creo correctamente
<img src="./Resources/images/back-5.jpg">

- Octavo, verificamos en Github Actions el deploy en Azure
<img src="./Resources/images/back-6.jpg">

- Finalmente, podremos acceder al backend desplegado
<img src="./Resources/images/back-7.jpg">
  
## 7.2. Solution Implementation.
### 7.2.1. Sprint 1
#### 7.2.1.1. Sprint Planning 1.

| Sprint \# | Sprint 1 |
| :---- | :---- |
| **Sprint Planning Background ** |  |
| Date | 2024-10-21 |
| Time | 21:20 PM |
| Location | Virtual (Plataforma Discord) |
| Prepared By | Arnol Caceres |
| Attendees (to planning meeting) | Arnol Caceres, Emerson Quispe, Fiorella Valencia, Franco Surco y Piero Stefano |
| Sprint n-1 Review Summary | No se aplica para esta entrega |
| Sprint n-1 Retrospective Summary | No se aplica para esta entrega |
| **Sprint Goal & User Stories ** | 24 |
| Sprint 1 Goal | \- Corregir los puntos de documentación de la entrega anterior \- Desplegar landing page de Turistas y Agencias \- Desplegar primera versión de frontend \- Desplegar primera versión de backend |
| Sprint 1 Velocity | Para este sprint calculamos que podemos aceptar 130 Story Points |
| Sum of Story Points | 127 |

#### 7.2.1.2. Sprint Backlog 1.
| Sprint \# | Sprint 1 |  |  |  |  |  |  |
| ----- | ----- | ----- | ----- | ----- | :---- | :---- | :---- |
| User Story |  | Work-Item / Task |  |  |  |  |  |
|  Id | Título | id | Descripcion | Estimation (Hours) |  | Assigned To | Status(To-do / InProcess / ToReview / Done) |
| US-14 | Ver portada | US-14-1 | **Como** usuario **deseo** visualizar una portada en landing page **para** poder captar mi atención y no me aburra al momento de leer el contenido | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-15 | Información de la aplicación | US-15-1 | **Como** usuario **deseo** ver información acerca de la aplicación **para** poder saber las funcionalidades que ofrece la aplicación | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-16 | Motivos por el cual unirnos | US-16-1 | **Como** usuario **deseo** ver motivos por el cual unirnos a la aplicación **para** poder saber los beneficios que ofrece la aplicación | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-17 | Redirección a la aplicación | US-17-1 | **Como** usuario **deseo** que haya un call-to-action **para** poder entrar a la aplicación | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-18 | Footer de la landing page | US-18-1 | **Como** usuario **deseo** que haya un footer **para** poder ver las redes sociales y los contactos de la aplicación | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-19 | About the product | US-19-1 | **Como** usuario **deseo** que haya un video acerca de la aplicación **para** poder ver las funcionalidades que tiene de una manera más visual. | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-20 | Responsive design | US-20-1 | **Como** usuario **deseo** que la aplicación sea responsiva **para** poder visualizar la landing page desde cualquier dispositivo. | 3 | Franco Surco \- Arnol Caceres |  | Done |
| US-01 | Añadir servicio | US-01-1 | **Como** agencia **deseo** agregar mis servicios **para que** mis clientes sepan más sobre lo que ofrezco. | 8 | Emerson Quispe \- Fiorella Valencia \- Piero Stefano |  | Done |
| US-05 | Crear ofertas | US-05-1 | **Como** turista **deseo** ver ofertas y paquetes recomendados de diferentes agencias **para** escoger la mejor opción que se acomode a lo que necesito. | 8 | Emerson Quispe \- Fiorella Valencia \- Piero Stefano |  | Done |
| US-11 | Monitorear clientes  | US-11-1 | **Como** agencia **deseo** tener control del estado del servicio ofrecido a mis clientes **para** indicar cuando un servicio se ha cumplido satisfactoriamente. | 8 | Emerson Quispe \- Fiorella Valencia \- Piero Stefano |  | Done |
| US-13 | Ver servicio | US-13-1 | **Como** turista **deseo** acceder a los detalles de un servicio ofrecido por una agencia **para** decidir si adquirirlo o no. | 5 | Emerson Quispe \- Franco Surco |  | Done |
| US-06 | Buscar agencias | US-06-1 | **Como** turista **deseo** buscar agencias haciendo uso de varios filtros **para** escoger la mejor agencia según lo que necesito. | 5 | Emerson Quispe \- Franco Surco |  | Done |
| US-02 | Personalizar viaje | US-02-1 | **Como** turista **deseo** personalizar el viaje que haré con una agencia, modificando aspectos del viaje **para** tener una mejor experiencia. | 8 | Emerson Quispe \- Fiorella Valencia \- Piero Stefano |  | Done |
| US-03 | Visualizar reseña | US-03-1 | **Como** agencia **deseo** visualizar las reseñas que tiene mi negocio **para** saber que puedo mejorar o agregar. | 5 | Emerson Quispe \- Arnol Caceres |  | Done |
| US-07 | Ver valoraciones | US-07-1 | **Como** turista **deseo** ver las valoraciones de otros usuarios con cada agencia **para** saber si la agencia es segura o de confianza. | 5 | Emerson Quispe \- Franco Surco |  | Done |
| US-08 | Editar página de negocio | US-08-1 | **Como** agencia **deseo** editar la página de mi negocio **para** colocar toda mi información y los medios de contacto. | 3 | Emerson Quispe \- Arnol Caceres |  | Done |
| US-05 | Crear ofertas | US-05-1 | **Como** agencia **deseo** crear ofertas y descuentos de mis servicios **para** atraer a más clientes. | 3 | Fiorella Valencia \- Piero Stefano |  | Done |
| US-11 | Calificar servicio | US-11-1 | **Como** turista **deseo** calificar el servicio que contraté **para** mostrar mi agrado o desagrado y más usuarios sepan sobre el mismo. | 3 | Fiorella Valencia \- Piero Stefano |  | Done |
| US-09 | Cambiar plan de suscripción | US-09-1 | **Como** agencia **deseo** cambiar mi plan de suscripción **para** ofrecer más servicios a mis clientes. | 8 | Fiorella Valencia \- Piero Stefano |  | Done |
| US-10 | Crear promociones | US-10-1 | **Como** agencia **deseo** crear campañas de promoción **para** llegar a más clientes. | 5 | Franco Surco \- Arnol Caceres |  | Done |
| US-21 | Acceso al aplicativo | US-21-1 | **Como** usuario de “Go2Climb” **Quiero** poder utilizar la aplicación desde diferentes navegadores **Para** poder buscar agencias y servicios de alpinismo sin estar limitado a un navegador. | 3 | Piero Stefano |  | Done |
| US-22 | Velocidad de carga | US-22-1 | **Como** usuario de la plataforma  **Quiero** que la velocidad de carga de la aplicación sea rápida y eficiente, **Para** poder acceder rápidamente a la información de las agencias y servicios  sin demoras.  | 3 | Piero Stefano |  | Done |
| US-23 | Interfaz interactiva y deductiva | US-23-1 | **Como** usuario **Quiero** poder buscar y reservar vuelos y hoteles de manera rápida y sencilla **Para** que pueda planificar mis viajes sin problemas | 3 | Emerson Quispe |  | Done |
| US-24 | Protección de data | US-24-1 | **Como** usuario **Quiero** que mi información personal y financiera esté protegida contra el acceso no autorizado o el robo **Para** que pueda reservar vuelos y hoteles con confianza  | 5 | Fiorella Valencia \- Piero Stefano |  | In-Process |
| US-26 | Comentarios para las actividades | US-26-1 | **Como** turista de la plataforma, **quiero** poder compartir mis comentarios y opiniones sobre las actividades proporcionadas por las empresas, **para** que otros usuarios puedan tomar decisiones informadas sobre su participación en esas actividades. | 5 | Fiorella Valencia \-  Emerson Quispe  |  | Done |
| US-27 | Monitorear datos del turista | US-27-1 | **Como** turista deseo revisar mis datos de actividad (pasos, latidos del corazón, temperatura y ubicación) obtenidos a través de mis botas o reloj durante mi experiencia de alpinismo **para** poder monitorear mi estado físico y condiciones durante la actividad. | 8 | Fiorella Valencia \- Emerson Quispe \- Franco Surco |  | In-Process |
| US-28 | Ver datos de turistas por agencia | US-28-1 | **Como** agencia de turismo deseo poder acceder a los datos de actividad de los turistas que han utilizado mis servicios, **para** poder monitorear su progreso y ofrecer recomendaciones de seguridad. | 8 | Fiorella Valencia \-  Emerson Quispe |  | In-Process |
#### 7.2.1.3. Development Evidence for Sprint Review.
En esta sección, como equipo, explicamos y presentamos los avances en implementación con relación a los productos de la solución según el alcance del Sprint 1. Incluimos una introducción que resume los principales avances y una tabla con los commits relacionados con la implementación.
<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>Repository</th>
            <th>Branch</th>
            <th>Commit ID</th>
            <th>Commit Message</th>
            <th>Commit Message Body</th>
            <th>Commit Date</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Web-Application-Front</td>
            <td>develop</td>
            <td></td>
            <td></td>
            <td>-</td>
            <td></td>
        </tr>
        <tr>
            <td>Web-Application-Front</td>
            <td>develop</td>
            <td></td>
            <td></td>
            <td>-</td>
            <td></td>
        </tr>
        <tr>
            <td>Web-Application-Front</td>
            <td></td>
            <td></td>
            <td></td>
            <td>-</td>
            <td></td>
        </tr>
        <tr>
            <td>Web-Application-Front</td>
            <td>develop</td>
            <td></td>
            <td></td>
            <td>-</td>
            <td></td>
        </tr>
        <tr>
            <td>Mobile-Application</td>
            <td>Main</td>
            <td></td>
            <td></td>
            <td>-</td>
            <td></td>
        </tr>
        <tr>
            <td>Mobile-Application</td>
            <td>feature/notifications</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Backend</td>
            <td>Main</td>
            <td>894a234567e0bffde38c95f5d5f99921a9099104</td>
            <td>Primer Commit</td>
            <td>-</td>
            <td>Oct 27,2024</td>
        </tr>
        <tr>
            <td>Backend</td>
            <td>Main</td>
            <td>e18bee3a398c7e66aa0a2a16084678e37b40f61c</td>
            <td>Four commit</td>
            <td>-</td>
            <td>Nov 02,2024</td>
        </tr>
        <tr>
            <td>Backend</td>
            <td>Main</td>
            <td>87fcb6d4a0f4e0bb0b7089b0a589176086e0fcf9</td>
            <td>Add or update the Azure App Service build and deployment workflow config</td>
            <td>-</td>
            <td>Nov 02,2024</td>
        </tr>
    </tbody>
</table>

#### 7.2.1.4. Testing Suite Evidence for Sprint Review.
En esta sección, el equipo presenta el conjunto de pruebas automatizadas realizadas durante el Sprint 1, incluyendo Unit Tests, Integration Tests y Acceptance Tests. Se detallan las clases y comportamientos asociados a cada test, y se incluyen ejemplos de los archivos .feature y Steps para los tests de BDD. También proporcionamos la ruta del repositorio y los commits relacionados con los avances en testing.

#### 7.2.1.5. Execution Evidence for Sprint Review.
En esta sección, se proporciona un resumen de los logros alcanzados durante el Sprint 1. Se incluyen capturas de pantalla de las principales vistas implementadas, y se añade un enlace a un video que muestra y explica la visualización y navegación logradas durante este Sprint.

- Despliegue del Frontend
<img src="./Resources/images/frontend-7.png">
<img src="./Resources/images/frontend-8.png">


#### 7.2.1.6. Services Documentation Evidence for Sprint Review.
En esta sección, se detalla la documentación de los Endpoints creados y actualizados durante el Sprint 1. Se presenta un resumen de los logros alcanzados en la documentación de los Web Services para este Sprint. La sección incluye una tabla que muestra las acciones implementadas para cada Endpoint

<img src="./Resources/images/swagger-1.png">
<img src="./Resources/images/swagger-2.png">
<img src="./Resources/images/swagger-3.png">
<img src="./Resources/images/swagger-4.png">
<img src="./Resources/images/swagger-5.png">


#### 7.2.1.7. Software Deployment Evidence for Sprint Review.
- Landing Page
<img src="./Resources/images/landing-5.png">

- Frontend
<img src="./Resources/images/front-5.png">

-Backend

<img src="./Resources/images/back-6.jpg">

<img src="./Resources/images/back-7.jpg">

#### 7.2.1.8. Team Collaboration Insights during Sprint.
- Frontend
<img src="./Resources/images/team-1.png">

- Backend
<img src="./Resources/images/team-2.png">

### 7.2.1. Sprint 2

#### 7.2.2.1. Sprint Planning 2.
| Sprint \# | Sprint 2 |
| :---- | :---- |
| **Sprint Planning Background** |  |
| Date | 2024-11-10 |
| Time | 19:20 PM |
| Location | Virtual (Plataforma Discord) |
| Prepared By | Arnol Caceres |
| Attendees (to planning meeting) | Arnol Caceres, Emerson Quispe, Fiorella Valencia, Franco Surco y Piero Stefano |
| Sprint n-2 Review Summary | Se realizaron varios moldeamientos a los productos actuales gracias a las entrevistas realizadas durante este Sprint, ademas de realizar las primeras versiones de cada producto(Web Application, Mobile Application, IoT Embedded App, Cloud Service, Edge Service, etc). |
| Sprint n-2 Retrospective Summary | Se evidenció una falta de fuentes confiables al momento de realizar las investigaciones previas para el desarrollo, documentación y despliegue de los productos. Por esta razón, se detallará mejor la documentación del siguiente Sprint |
| **Sprint Goal & User Stories** | 4 |
| Sprint 2 Goal | \- Corregir los puntos de documentación de la entrega anterior \- Desplegar segunda versión de frontend \- Desplegar segunda versión de backend \- Desplegar primera version del wokwi \- Desplegar primera version del mobile   |
| Sprint 2 Velocity | Para este sprint calculamos que podemos aceptar 24 Story Points |
| Sum of Story Points | 24 |
#### 7.2.2.2. Sprint Backlog 2.
| Sprint \# | Sprint 1 |  |  |  |  |  |  |
| ----- | ----- | ----- | ----- | ----- | :---- | :---- | :---- |
| User Story |  | Work-Item / Task |  |  |  |  |  |
|  Id | Título | id | Descripcion | Estimation (Hours) |  | Assigned To | Status(To-do / InProcess / ToReview / Done) |
| US-24 | Protección de data | US-24-1 | **Como** usuario **Quiero** que mi información personal y financiera esté protegida contra el acceso no autorizado o el robo **Para** que pueda reservar vuelos y hoteles con confianza  | 5 | Fiorella Valencia \- Piero Stefano |  | Done |
| US-25 | Comentarios para las actividades | US-26-1 | **Como** desarrollador **Quiero** poder mantener y actualizar la aplicación fácilmente a lo largo del tiempo **Para** que pueda seguir siendo útil y relevante a medida que cambian las necesidades del negocio | 5 | Fiorella Valencia \-  Emerson Quispe \- Franco Surco \- Arnol Caceres|  | Done |
| US-27 | Monitorear datos del turista | US-27-1 | **Como** turista deseo revisar mis datos de actividad (pasos, latidos del corazón, temperatura y ubicación) obtenidos a través de mis botas o reloj durante mi experiencia de alpinismo **para** poder monitorear mi estado físico y condiciones durante la actividad. | 8 | Fiorella Valencia \- Emerson Quispe \- Franco Surco |  | Done |
| US-28 | Ver datos de turistas por agencia | US-28-1 | **Como** agencia de turismo deseo poder acceder a los datos de actividad de los turistas que han utilizado mis servicios, **para** poder monitorear su progreso y ofrecer recomendaciones de seguridad. | 8 | Fiorella Valencia \-  Emerson Quispe \- Piero Stefano \- Arnol Caceres|  | Done |

#### 7.2.2.3. Development Evidence for Sprint Review

En esta sección, como equipo, explicamos y presentamos los avances en implementación con relación a los productos de la solución según el alcance del Sprint 1. Incluimos una introducción que resume los principales avances y una tabla con los commits relacionados con la implementación.
<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>Repository</th>
            <th>Branch</th>
            <th>Commit ID</th>
            <th>Commit Message</th>
            <th>Commit Message Body</th>
            <th>Commit Date</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Fronted</td>
            <td>main</td>
            <td>d4f48e5ba96225a3963e004f9ce7ed2a8291ffa6</td>
            <td>feat: added monitoring component</td>
            <td>-</td>
            <td>Nov 21, 2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>main</td>
            <td>a08a626f37c00527f9d86f3800d26a480c0e62c9</td>
            <td>add: flutter and dart upgrade</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>develop-home</td>
            <td>b2a7539ca5ee1147cc29ad67be7708bc74c2463a</td>
            <td>add: steps and km counter</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>develop-home</td>
            <td>5cd93430164068b02737ff7a5af7b87ba643a6e6</td>
            <td>add: Hear Rate in HomeScreen</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>develop-home</td>
            <td>ce7c4e165220d863af217e611d3827b54a6d97b0</td>
            <td>add: device screen</td>
            <td>-</td>
            <td>Nov 18,2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>develop-account/profile</td>
            <td>ab88e47a3a93f5740d05a7269a6c9642caaf9a53</td>
            <td>add: profile screen</td>
            <td>-</td>
            <td>Nov 18,2024</td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>develop-account/profile</td>
            <td>e07aa8e1a8b3a5c36881d8cc5119a930722fc7d7</td>
            <td>add: account screen</td>
            <td>-</td>
            <td>Nov 18,2024</td>
        </tr>
        <tr>
            <td>Backend_TrailSync</td>
            <td>main</td>
            <td>4a99ba50425c31cf25dcb57bac6e0868c7702394</td>
            <td>feat(boot): add new entity</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Backend_TrailSync</td>
            <td>main</td>
            <td>cbd408317ea535baa07c71f48a9566e5f8c4f6c2</td>
            <td>feat(Boot): add update response</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Backend_TrailSync</td>
            <td>main</td>
            <td>9eca5c1badae912c4948d76d9d7cf1a144c0c2a2</td>
            <td>feat(Boot): add getters and setters</td>
            <td>-</td>
            <td>Nov 17,2024</td>
        </tr>
        <tr>
            <td>Backend_TrailSync</td>
            <td>main</td>
            <td>df513bfee6b71525304bb9883d12ab7abef5cbe7</td>
            <td>feat(Boot)</td>
            <td>-</td>
            <td>Nov 21,2024</td>
        </tr>
        <tr>
            <td>IoT-sensors</td>
            <td>main</td>
            <td>f339adbad458c12079335f2575589831340992c8</td>
            <td>create component for sensors</td>
            <td>-</td>
            <td>Nov 21,2024</td>
        </tr>
        <tr>
            <td>IoT-gps</td>
            <td>main</td>
            <td>87d825ee447480d12c03cff8777bf9547694c968</td>
            <td>create components for gps</td>
            <td>-</td>
            <td>Nov 21,2024</td>
        </tr>
    </tbody>
</table>

#### 7.2.2.4. Testing Suite Evidence for Sprint Review
- Feature: Publicación de servicios en la aplicación web (commit: 2571154)
<img src="./Resources/images/tests/HU03.png">

- Feature: Búsqueda de servicios (commit: 099246f)
<img src="./Resources/images/tests/HU04.png">

- Feature: Contactar con agencia que brinda el servicio (commit: fc3e8ac)
<img src="./Resources/images/tests/HU05.png">

- Feature: Monitoreo de aventureros (commit: 485d6ae)
<img src="./Resources/images/tests/HU06.png">

- Feature: Comentarios a un servicio (commit: a08b5f7)
<img src="./Resources/images/tests/HU07.png">

#### 7.2.2.5. Execution Evidence for Sprint Review

#### 7.2.2.6. Services Documentation Evidence for Sprint Review

#### 7.2.2.7. Software Deployment Evidence for Sprint Review


- Frontend
<img src="./Resources/images/front-5.png">

- Backend
<img src="./Resources/images/back-sprint2-1.jpeg">
<img src="./Resources/images/back-sprint2-2.jpeg">
<img src="./Resources/images/back-sprint2-3.jpeg">

#### 7.2.2.8. Team Collaboration Insights during Sprint.

- Frontend
<img src="./Resources/images/back-sprint2-5.jpeg">

- Backend
<img src="./Resources/images/back-sprint2-4.jpeg">

- Mobile
<img src="./Resources/images/back-sprint2-6.jpeg">

## 7.3. Validation Interviews.
### 7.3.1. Diseño de Entrevistas
# Entrevista de Validación para la Aplicación de Turismo de Alpinismo

## Preguntas de Datos Personales
1. ¿Podría decirme su nombre completo?
2. ¿Qué edad tiene?
3. ¿Cuál es su lugar de residencia actual?
4. ¿Tiene alguna experiencia previa en turismo de montaña o actividades al aire libre?
5. ¿Con qué frecuencia suele realizar actividades como alpinismo o senderismo?

## Preguntas Principales para la Validación de la Aplicación

### Diseño e Interfaz
- ¿Cómo percibe la apariencia de la página principal de la aplicación? ¿Le resulta visualmente atractiva y organizada?
- ¿Diría que la interfaz es intuitiva y fácil de manejar? ¿Por qué o por qué no?

### Contenido y Proceso de Registro
- ¿El contenido presentado en la página de inicio le incita a registrarse? ¿Qué aspectos le resultan más llamativos o relevantes?
- ¿Qué opina sobre el monitoreo que se realiza con dispositivos IoT para obtener datos como la temperatura, localización, latidos del corazón, entre otros? ¿Le parece útil esta funcionalidad?

### Utilidad y Funcionalidades
- ¿Considera que las funciones de la aplicación son útiles para planificar y realizar actividades de alpinismo? ¿Por qué?
- ¿Hay alguna funcionalidad que le gustaría ver añadida para mejorar su experiencia?

### Sugerencias de Mejora
- ¿Hay algún aspecto de la aplicación que piense que necesita ajustes o mejoras? ¿Cuál sería su sugerencia?
- ¿Alguna función adicional le resultaría útil para mejorar su experiencia como usuario de la aplicación?

### Planes de Pago
- ¿Estaría dispuesto a adquirir un plan de pago para acceder a funciones avanzadas? ¿Qué tipo de características o beneficios le motivarían a pagar?

### Opinión General
- ¿Cree que la aplicación cubre las necesidades de las personas interesadas en actividades de alpinismo?
- ¿Recomendaría esta aplicación a otros que comparten el interés por el alpinismo y actividades de aventura? ¿Por qué?

### 7.3.2. Registro de Entrevistas.
En esta sección se registrarán las entrevistas realizadas con la información recolectada de las respuestas realizadas en la sección de diseño de entrevista.

Entrevista 1: 
- Nombre completo: Abel Montoya
- Edad: 23 años
- Distrito: Agustino

**Screenshot aca**

- Link del video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/Eb17RNsxQopHo7o5c1Y29c8BRtGb7QIE9LsL7sPM1TFV_Q?e=W4SLzO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D
- Timing de la entrevista: 00:00 - 00:00
- Duración de la entrevista: 

Resumen:
Abel Montoya, de 23 años, vive en el distrito del Agustino y hace ejercicio tres veces por semana pero no practica alpinismo ni senderismo. Durante la entrevista, mencionó que a pesar que no lo practica si le gastaría en algún momento probarlo mas que todo por la experiencia y las vistas.

Cuando le presentamos nuestra propuesta, mostró gran interés en la lógica del negocio. Según él, esto ahorraría tiempo a los turistas que buscan ciertos lugares que cumplan con sus propios requisitos para esto el buscador con filtro presento una solución. También valoró la idea de poder ver mucho información clave en cada publicación del home como la dificultad, el precio y la descripción del recorrido.

El dispositivo IOT que le presentamos le pareció una idea innovadora y muy útil para las personas que practican estos deporte. Destaco los informes en tiempo real que visualizaría la agencia y el turistas desde su propio dispositivo móvil. Esto seria muy útil para marcar tiempos, pathings y socorrer lo mas pronto a alguien que lo necesite en caso de un accidente. 

Al finalizar la entrevista, Abel sugirió una mejora adicional para nuestra solución: Acelerar los tiempos de carga. Esto, según él, haría mas cómoda y con un mejor flujo la navegación en la web.

Entrevista 2: 
- Nombre completo: Diego Acosta
- Edad: 24 años
- Distrito: San Miguel 

**Screenshot aca**

- Link del video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/Eb17RNsxQopHo7o5c1Y29c8BRtGb7QIE9LsL7sPM1TFV_Q?e=W4SLzO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D
- Timing de la entrevista: 00:00 - 00:00
- Duración de la entrevista: 

Resumen:
Diego Acosta, de 24 años, vive en el distrito de San Miguel y practica senderismo una vez al año en viajes familiares. Durante la entrevista, menciono que le gustaria practicar mas estos deportes pero no sabe quien lo podría orientar.

Cuando le presentamos nuestra propuesta, mostró gran interés en como están distribuidos los paquetes y la información completa que ofrecen. Según él, las estadísticas que muestran en cada publicación son las características mas importantes que alguien interesado podría pedir ya que en su experiencia muchas veces las agencias se guardan información importante. También valoró la idea de poder dejar reseñas en las publicaciones y poder leer la de otros usuarios porque así podría juzgar mejor si quiere o no ese paquete..

El dispositivo IOT que le presentamos le pareció una idea revolucionaria. Destaco que la informacion en tiempo real que se mostrara puede ser muy util para personas que sufran problemas al corazon como taticardias, o infartos. Esto seria muy útil para socorrer de forma rapida a gente que tenga un infarto, un golpe de calor o que simplemente se perdio siendo ubicado rapidamente con el gps. 

Al finalizar la entrevista, Diego destaco bastante el uso de la aplicacion movil para poder ver tus propios datos y mantener el control sobre estos mismos. Esto ayudaria a estar preparados para ciertos inconvenientes que se podrian presentar en media caminata.

Entrevista 3:
- Nombre: Camila
- Apellidos: La Torre
- Edad: 25
- Distrito: Lima, Pueblo Libre
- Ocupación: Médica
- Link: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/Eb17RNsxQopHo7o5c1Y29c8BRtGb7QIE9LsL7sPM1TFV_Q?e=W4SLzO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D
- - Timing de la entrevista: 11:11 - 21:10

Resumen:
Camila La Torre, una médica de 25 años de Lima, evaluó la aplicación de manera positiva. Destacó su diseño visual atractivo y la facilidad de uso de la interfaz, lo cual le resultó intuitivo y bien organizado. El contenido de la página de inicio le pareció lo suficientemente interesante como para motivarla a registrarse, especialmente por la funcionalidad de monitoreo mediante dispositivos IoT, que incluye parámetros como temperatura, localización y ritmo cardíaco, características que consideró muy útiles para actividades de alpinismo. Aunque no sugirió mejoras ni funcionalidades adicionales, expresó que el conjunto actual cumple con sus expectativas. Además, mencionó que estaría dispuesta a pagar por un plan si incluye características avanzadas de seguridad. En general, cree que la aplicación cubre las necesidades de los interesados en alpinismo y estaría dispuesta a recomendarla.

<img src="./Resources/entrevistaCL.png">

Entrevista 4: 
- Nombre completo: Jorge Garcia
- Edad: 21 años 

<img src="./Resources/images/entrevista-1.png">

- Link del video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/Eb17RNsxQopHo7o5c1Y29c8BRtGb7QIE9LsL7sPM1TFV_Q?e=W4SLzO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D
- Timing de la entrevista: 00:00 - 00:00
- Duración de la entrevista: 

Resumen:
Jorge Garcia, de 21 años, aunque no cuenta con experiencia en senderismo, pues menciona que podria darse una oportunidad para pobrar este deporte.

Cuando le presentamos nuestra propuesta, comento que podriamos dar algunas mejoras en el diseño de la aplicacion, quitando algunos espacios en blanco que lo hacen parecer vacio, aunque tambien considera que la informacion de la rutas, las reseñas y el filtro de busqueda hace que la aplicacion sea una gran alternativa para su uso. 

El dispositivo IOT que le presentamos le pareció una idea prometedora. Ya que, a las personas que realizan senderismo con regularidad, les podria causar mayor seguridad 

Al finalizar la entrevista, Jorgue destaco que la aplicacion movil, pueda notificarle sobre los datos va registrando en su ruta.

### 7.3.3. Evaluaciones según heurísticas.
# Evaluación según Heurísticas de UX
**Usabilidad – Diseño Inclusivo – Arquitectura de la Información**  
**APLICACIÓN**: TrailSync  

### TAREAS EVALUADAS
- **Inicio de Sesión**
- **Publicación de un servicio de montañismo**
- **Edición de un Servicio**
- **Búsqueda de servicios o agencias**
- **Filtrado de servicios**

### TAREAS EXCLUIDAS
- **Cerrar Sesión**
- **Editar publicación de una agencia**
- **Publicar comentario**
- **Calificar servicio**
  
### ESCALA DE SEVERIDAD
| Nivel | Descripción                                                                 |
|-------|-----------------------------------------------------------------------------|
| **1** | Problema leve: el usuario puede superarlo fácilmente o ocurre raramente.    |
| **2** | Problema menor: ocurre con cierta frecuencia y puede ser más molesto.       |
| **3** | Problema significativo: sucede regularmente o es difícil de superar. Se debe dar prioridad. |
| **4** | Problema crítico: impide que el usuario continúe. Necesita solución urgente antes del lanzamiento. |

### TABLA RESUMEN
| #  | Problema                                                                                      | Severidad | Heurística/Principio Violado                   |
|----|-----------------------------------------------------------------------------------------------|-----------|------------------------------------------------|
| 1  | La interfaz de inicio de sesión no proporciona retroalimentación sobre errores de entrada     | 2         | Usabilidad: Ayuda para reconocer y recuperarse de errores |
| 2  | Al publicar o editar un servicio, no se muestra una confirmación de éxito                    | 3         | Usabilidad: Visibilidad del estado del sistema |
| 3  | Los filtros de búsqueda de servicios no son intuitivos y limitan las opciones del usuario    | 3         | Usabilidad: Flexibilidad y eficiencia de uso   |

---

### DESCRIPCIÓN DE LOS PROBLEMAS

#### PROBLEMA #1: La interfaz de inicio de sesión no proporciona retroalimentación sobre errores de entrada
- **Severidad**: 2
- **Heurística violada**: Usabilidad - Ayuda para reconocer y recuperarse de errores
- **Descripción**: Cuando los usuarios ingresan información incorrecta en el inicio de sesión (como una contraseña o nombre de usuario incorrecto), no reciben una retroalimentación clara o inmediata sobre el error específico, lo cual dificulta el proceso de autenticación.
- **Recomendación**: Agregar mensajes de error claros para ayudar a los usuarios a entender qué campo está incorrecto (usuario o contraseña) y cómo pueden corregirlo. Esto mejorará la experiencia al reducir la frustración y ayudar a los usuarios a iniciar sesión con más facilidad.



#### PROBLEMA #2: Al publicar o editar un servicio, no se muestra una confirmación de éxito
- **Severidad**: 3
- **Heurística violada**: Usabilidad - Visibilidad del estado del sistema
- **Descripción**: Cuando los usuarios crean o editan un servicio de montañismo, la aplicación no muestra ningún mensaje de confirmación que indique que la acción se realizó con éxito. Esto puede hacer que los usuarios no estén seguros de si el servicio fue publicado o los cambios se guardaron.
- **Recomendación**: Implementar un mensaje de confirmación claro que aparezca después de publicar o editar un servicio. Esto mejorará la confianza del usuario en la aplicación y proporcionará una retroalimentación inmediata de sus acciones.

<img src="./Resources/images/heuristic1.png">

#### PROBLEMA #3: Los filtros de búsqueda de servicios no son intuitivos y limitan las opciones del usuario
- **Severidad**: 3
- **Heurística violada**: Usabilidad - Flexibilidad y eficiencia de uso
- **Descripción**: La función de filtrado para buscar servicios de montañismo no es intuitiva; además, carece de opciones suficientes para refinar las búsquedas de manera eficiente. Esto dificulta que los usuarios encuentren rápidamente el servicio o agencia que buscan.
- **Recomendación**: Mejorar la función de filtrado agregando opciones más detalladas y relevantes para los usuarios. También sería útil rediseñar la interfaz de los filtros para que sea fácil de entender y utilizar, facilitando una búsqueda más rápida y personalizada.

<img src="./Resources/heuristic2.png">

## 7.4. Video About-the-Product
Se presenta el video About the Product. En el cúal se muestra la aplicación de TrailSync.

Enlace: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/EW1dU6UXdgFFomWruiow-bsBNlR9QpbodxxkOYvmElpVVQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=ZpkcKj

<img src="./Resources/abouteam.png">

## 7.5. Video About-the-Team
Se presenta el video About the Team. En el cúal se muestra al equipo de desarrollo.

Enlace: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/EW1dU6UXdgFFomWruiow-bsBNlR9QpbodxxkOYvmElpVVQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=YEL6lf

<img src="./Resources/abouteamreal.png">

| Anexo A. Video Exposiciones |          |          |
|-----------------------------|----------|----------|
| **Entrega**                 | **URL**  |
| TP                          | [https://youtu.be/Zp8DbZzcL7s](https://youtu.be/Zp8DbZzcL7s](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/EYb_-gUlwQBNmaTs4Cztxp0BLAsgRcI4Rp24A51IBpQP8Q?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=zF9YQy) |
| TB2                         | (https://upcedupe-my.sharepoint.com/:v:/g/personal/u20201b944_upc_edu_pe/ER-G7GkTCVRPnjFLEF8nhkUB65BeFO4Jz6koajQrvVGw8w?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=WGXN0D) |
