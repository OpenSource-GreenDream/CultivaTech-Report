# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

## 5.1.1. Software Development Environment Configuration.

Para llevar a cabo el desarrollo de CultivaTech, GreenDream ha establecido un conjunto de herramientas que serán utilizadas en las diferentes actividades del proyecto. Estas herramientas nos van a permitir poder organizar el trabajo del equipo, diseñar las interfaces, desarrollar los componentes de software, gestionar el código fuente y documentar los servicios implementados.

La selección del entorno de trabajo se realizó considerando las tecnologías definidas para la solución y procurando que los integrantes puedan mantener una forma de trabajo consistente durante las distintas etapas del proyecto. A continuación, se detallan las herramientas seleccionadas para cada actividad:

| **Categoría** | **Herramienta** | **Uso en CultivaTech** | **Ruta de acceso / descarga** | 
|---|---|---|---|
| Gestión del proyecto | Trello | Organización del Product Backlog, asignación de actividades y seguimiento del avance de los Sprints. | [https://trello.com/](https://trello.com/) |
| Diseño de interfaces | Figma | Creación de wireframes, mockups y prototipos de las interfaces de CultivaTech. | [https://www.figma.com/](https://www.figma.com/) |
| Investigación de usuarios | UXPressia | Construcción de User Personas, Empathy Maps, Journey Maps e Impact Maps. | [https://uxpressia.com/](https://uxpressia.com/) |
| Diagramación | Lucidchart | Elaboración de diagramas relacionados con los flujos y modelos del sistema. | [https://www.lucidchart.com/](https://www.lucidchart.com/) |
| Desarrollo de Landing Page | Visual Studio Code | Edición y desarrollo de la Landing Page mediante HTML5, CSS3 y JavaScript. | [https://code.visualstudio.com/](https://code.visualstudio.com/) |
| Desarrollo Frontend | Angular | Implementación de la aplicación web de CultivaTech y sus funcionalidades de interacción con el usuario. | [https://angular.io/](https://angular.io/) |
| Componentes de interfaz | Angular Material | Implementación de componentes de interfaz para la aplicación web de CultivaTech. | [https://material.angular.io/](https://material.angular.io/) |
| Desarrollo de Web Services | IntelliJ IDEA | Entorno utilizado para desarrollar los servicios RESTful con Java y Spring Boot. | [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/) |
| Framework Backend | Spring Boot | Construcción de los Web Services que proporcionarán las funcionalidades y datos requeridos por las aplicaciones. | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot) |
| Persistencia de datos | Spring Data JPA | Gestión de la persistencia y comunicación entre los servicios backend y la base de datos. | [https://spring.io/projects/spring-data-jpa](https://spring.io/projects/spring-data-jpa) |
| Gestión de paquetes | npm | Instalación y administración de las dependencias utilizadas por los proyectos frontend. | [https://www.npmjs.com/](https://www.npmjs.com/) |
| Control de versiones | Git | Registro y seguimiento de los cambios realizados sobre el código fuente. | [https://git-scm.com/](https://git-scm.com/) |
| Repositorio | GitHub | Almacenamiento de los repositorios y colaboración mediante ramas y Pull Requests. | [https://github.com/](https://github.com/) |
| Documentación de APIs | Swagger / OpenAPI | Descripción y consulta de los endpoints desarrollados para los Web Services. | [https://swagger.io/](https://swagger.io/) |
| Diseño de base de datos | MySQL Workbench | Modelado y diseño de la estructura de datos utilizada por la solución. | [https://www.mysql.com/products/workbench/](https://www.mysql.com/products/workbench/) |

Además de las herramientas principales, el equipo empleará herramientas y funcionalidades de apoyo que permitirán mantener la calidad del desarrollo y facilitar el trabajo colaborativo durante la implementación de CultivaTech:

- **GitHub Pull Requests:** utilizados para realizar revisiones de los cambios antes de integrarlos a las ramas principales de los repositorios.
- **GitHub Issues:** utilizados para registrar tareas, incidencias y actividades pendientes durante el desarrollo del proyecto.
- **Swagger UI:** utilizado para visualizar y probar los endpoints de los Web Services documentados mediante OpenAPI.
- **npm:** utilizado para gestionar las dependencias necesarias para el desarrollo de los componentes Frontend.

El equipo busca mantener un entorno de trabajo consistente entre sus integrantes, utilizando herramientas compatibles con las tecnologías definidas para CultivaTech. Esto permitirá reducir problemas relacionados con diferencias en las configuraciones y facilitar la integración de los avances desarrollados de manera individual.

Asimismo, se seguirán convenciones y buenas prácticas para la gestión del código fuente, considerando el uso de GitFlow para organizar las ramas de desarrollo, Conventional Commits para mantener una estructura uniforme en los mensajes de commit y Semantic Versioning para la identificación de las versiones del producto.

Finalmente, las herramientas seleccionadas permiten cubrir las diferentes actividades involucradas en el ciclo de vida de CultivaTech, incluyendo Project Management, Requirements Engineering, UX/UI Design, Software Development, Software Documentation y Software Deployment. De esta manera, el entorno definido proporciona el soporte necesario para organizar, diseñar, desarrollar, documentar y desplegar los diferentes componentes de la solución.

## 5.1.2. Source Code Management.

La gestión del codigo fuente de CultivaTech se realizará utilizando Git como sistema de control de versiones y GitHub como plataforma para almacenar los repositorios y facilitar el trabajo colaborativo entre los integrantes de GreenDream. Esta organización permitirá mantener un historial de cambios, controlar las diferentes versiones del proyecto y realizar una integración ordenada de los avances desarrollados durante los Sprints.

A continuación, se presentan los usuarios de GitHub de los integrantes del equipo: 

| **Integrante** | **Usuario GitHub** |
|---|---|
| Jean Pierre Condor Sandoval | `jeanpcs` |
| Jorge Manuel Retuerto Rodriguez | `Calin1407` |
| Maria Luisa Munayco Apolaya | `malumunayco` |
| Renzo Piero Santos Minaya | `RSSint` |
| Rongela Karen Silva Hualpa | `amazcoffee2-spec` |

#### Repositorios del proyecto 

Los productos que forman parte de la solución CultivaTech serán gestionados mediante repositorios en GitHub. Cada producto contará contará con un repositorio destinado a mantener su código fuente y los recursos necesarios para su desarrollo.

| **Producto** | **Repositorio** |
|---|---|
| Informe | [Repositorio-Informe](https://github.com/OpenSource-GreenDream/CultivaTech-Report)|
| Landing Page | [Repositorio-Landing-Page]() |
| Frontend Web Application | [Repositorio-Frontend-Web-Application]() |
| Web Services | [Repositorio-Web-Services]() |

El repositorio correspondiente a los **Web Services** incluirá tanto el proyecto desarrollado con Spring Boot como los archivos asociados a las pruebas unitarias y de integración/aceptación, permitiendo verificar el correcto funcionamiento de los servicios implementados.

#### GitFlow WorkFlow 

Para organizar el desarrollo de CultivaTech, el equipo utilizará **GitFlow** como workflow de control de versiones. Este modelo permitirá separar el desarrollo de nuevas funcionalidades de las versiones estables del producto, facilitando la integración y revisión de los cambios realizados por los integrantes. 

Las ramas principales cosideradas para el proyecto serán `main` y `develop`.

**main**

La rama `main` contendrá las versiones estables de los productos, correspondientes a versiones que hayan sido revisadas y que estén listas para su publicación o despliegue.

**develop**

La rama `develop` será utilizada como rama principal de integración durante el desarrollo. En ella se incorporarán las funcionalidades terminadas antes de formar parte de una versión estable.

**feature**

Cada nueva funcionalidad será desarrollada mediante una rama `feature` independiente, creada a partir de `develop`. Esto permitirá que cada integrante pueda trabajar sobre una funcionalidad específica sin afectar directamente la rama de desarrollo principal.

La convención utilizada será:

```text
feature/<feature-name>
```

El nombre de la funcionalidad se escribirá en inglés, utilizando palabras descriptivas separadas por guiones.

Algunos ejemplos relacionados con CultivaTech son:

```text
feature/soil-monitoring
feature/crop-dashboard
feature/user-authentication
feature/soil-data-analysis
```

Una vez finalizada una funcionalidad, los cambios serán revisados mediante un **Pull Request** antes de integrarse a `develop`.

**release**

Las ramas `release` serán utilizadas cuando el equipo prepare una nueva versión de CultivaTech para su publicación. Estas ramas permitirán realizar pruebas finales, correcciones menores y ajustes necesarios antes de integrar la versión en `main`.

La convención utilizada será:

```text
release/vX.Y.Z
```

Por ejemplo:

```text
release/v1.0.0
release/v1.1.0
release/v1.2.0
```

El nombre de las versiones seguirá el estándar **Semantic Versioning (SemVer)**, utilizando el formato:

```text
MAJOR.MINOR.PATCH
```

Donde:

- **MAJOR:** se incrementa cuando se realizan cambios incompatibles con versiones anteriores.
- **MINOR:** se incrementa cuando se agrega nueva funcionalidad manteniendo la compatibilidad.
- **PATCH:** se incrementa cuando se realizan correcciones compatibles con la versión actual.

**hotfix**

Las ramas `hotfix` serán utilizadas para corregir errores críticos encontrados en una versión estable del producto. Estas ramas se crearán a partir de `main` para solucionar el problema sin incorporar cambios de desarrollo que todavía no hayan sido publicados.

La convención utilizada será:

```text
hotfix/<bug-name>
```

Por ejemplo:

```text
hotfix/soil-data-error
hotfix/login-validation
hotfix/api-response-error
```

Después de solucionar y validar el error, los cambios serán integrados tanto en `main` como en `develop`, evitando que la corrección se pierda en futuras versiones.

#### Conventional Commits

Para mantener un historial de cambios claro y uniforme, el equipo utilizará **Conventional Commits** para definir los mensajes de los commits realizados durante el desarrollo.

Los principales tipos de commit serán:

| **Prefijo** | **Descripción** |
|---|---|
| `feat` | Implementación de una nueva funcionalidad. |
| `fix` | Corrección de un error. |
| `docs` | Cambios relacionados con la documentación. |
| `style` | Cambios de formato que no modifican la lógica del sistema. |
| `refactor` | Reestructuración del código sin modificar su comportamiento. |
| `perf` | Mejoras relacionadas con el rendimiento. |
| `test` | Creación o modificación de pruebas. |
| `chore` | Tareas de mantenimiento, configuración o soporte del proyecto. |

Los mensajes seguirán la estructura:

```text
<type>(<scope>): <description>
```

Por ejemplo:

```text
feat(frontend): add soil monitoring dashboard
feat(api): add soil data endpoint
fix(frontend): correct crop dashboard layout
docs(scm): document source code management
test(api): add soil monitoring tests
```

De esta manera, la utilización de Git, GitHub, GitFlow, Semantic Versioning y Conventional Commits permitirá mantener una gestión organizada del código fuente de CultivaTech, facilitar la colaboración entre los integrantes y asegurar la trazabilidad de los cambios realizados durante el desarrollo del proyecto.

## 5.1.3. Source Code Style Guide & Conventions.

## 5.1.4. Software Deployment Configuration.
