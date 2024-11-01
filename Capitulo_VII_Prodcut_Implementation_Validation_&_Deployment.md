# Capitulo VII: Prodcut Implementation, Validation & Deployment
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
## 7.2. Solution Implementation.
### 7.2.1. Sprint 1
#### 7.2.1.1. Sprint Planning 1.
#### 7.2.1.2. Sprint Backlog 1.
#### 7.2.1.3. Development Evidence for Sprint Review.
#### 7.2.1.4. Testing Suite Evidence for Sprint Review.
#### 7.2.1.5. Execution Evidence for Sprint Review.
#### 7.2.1.6. Services Documentation Evidence for Sprint Review.
#### 7.2.1.7. Software Deployment Evidence for Sprint Review.
#### 7.2.1.8. Team Collaboration Insights during Sprint.
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
### 7.3.3. Evaluaciones según heurísticas.
## 7.4. Video About-the-Product
