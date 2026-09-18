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

### 5.1.3. Source Code Style Guide & Conventions

Con el propósito de mantener un código fuente ordenado, legible y consistente, el equipo de GreenDream establecerá un conjunto de convenciones para el desarrollo de CultivaTech. Estas reglas serán aplicadas por todos los integrantes durante la implementación de la Landing Page, la Frontend Web Application y los Web Services.

Para todos los lenguajes utilizados en la solución se empleará **nomenclatura en inglés**, incluyendo nombres de variables, funciones, clases, interfaces, componentes, archivos, métodos y otros elementos del código. Además, se tomarán como referencia las guías de estilo indicadas en el enunciado del proyecto.

#### Convenciones generales

Durante el desarrollo de CultivaTech se aplicarán las siguientes reglas:

- Los nombres de los elementos del código estarán escritos en inglés.
- Se utilizarán nombres descriptivos que permitan identificar fácilmente la función de cada elemento.
- Se evitarán abreviaciones innecesarias.
- Se mantendrá una correcta indentación y formato del código.
- Se priorizará la reutilización de componentes, funciones y servicios.
- Cada componente o clase deberá mantener una responsabilidad específica.
- Los comentarios se utilizarán únicamente cuando sean necesarios para explicar lógica que no resulte evidente a partir del código.
- Se evitará mantener código duplicado o innecesario.

#### Convenciones para HTML

Para la estructura de la Landing Page y las interfaces web se seguirán las recomendaciones de **HTML Style Guide and Coding Conventions** y **Google HTML/CSS Style Guide**.

Las principales convenciones serán:

- Utilizar elementos HTML semánticos como `header`, `nav`, `main`, `section`, `article` y `footer`.
- Mantener una correcta jerarquía de encabezados utilizando `h1`, `h2`, `h3`, entre otros.
- Utilizar atributos `alt` descriptivos en las imágenes.
- Mantener una estructura HTML correctamente indentada.
- Utilizar nombres descriptivos para los atributos y elementos relacionados con la interfaz.
- Evitar el uso innecesario de estilos directamente dentro de los elementos HTML.

Ejemplo:

```html
<section class="soil-monitoring">
    <h2>Soil Monitoring</h2>
    <p>Monitor the conditions of the crop soil.</p>
</section>
```

#### Convenciones para CSS

Para la definición de estilos se tomarán como referencia **Google HTML/CSS Style Guide** y las convenciones establecidas para CSS.

Las principales reglas serán:

- Utilizar nombres de clases descriptivos.
- Utilizar `kebab-case` para las clases CSS.
- Evitar estilos en línea cuando sea posible.
- Mantener agrupadas las reglas relacionadas con cada componente.
- Evitar la duplicación de estilos.
- Eliminar reglas CSS que ya no sean utilizadas.

Ejemplos:

```text
soil-monitoring
crop-dashboard
weather-card
user-profile
```

#### Convenciones para JavaScript

Para el código JavaScript utilizado en la Landing Page se seguirán las recomendaciones de las guías de estilo de JavaScript y las convenciones establecidas por el equipo.

Se aplicarán las siguientes reglas:

- Utilizar `const` cuando el valor de una variable no necesite cambiar.
- Utilizar `let` cuando sea necesario modificar el valor de una variable.
- Evitar el uso de `var`.
- Utilizar nombres descriptivos para variables y funciones.
- Utilizar funciones con responsabilidades específicas.
- Evitar la duplicación de código.
- Mantener una correcta indentación y formato.

Ejemplo:

```javascript
const getSoilData = async () => {
    // Implementation
};
```

#### Convenciones para TypeScript

Para el desarrollo de la Frontend Web Application con Angular se adoptarán las recomendaciones de **Angular Coding Style Guide** y **Google TypeScript Style Guide**.

Las principales convenciones serán:

- Utilizar `camelCase` para variables, propiedades y métodos.
- Utilizar `PascalCase` para clases, interfaces y componentes.
- Utilizar nombres descriptivos en inglés.
- Mantener los componentes enfocados en una responsabilidad específica.
- Separar la lógica de presentación de la lógica relacionada con los servicios.
- Utilizar interfaces y tipos cuando permitan definir claramente la estructura de los datos.
- Mantener una organización consistente de los archivos y módulos del proyecto.

Ejemplo:

```typescript
export interface SoilData {
    humidity: number;
    ph: number;
    fertility: number;
}

export class SoilMonitoringService {
    getSoilData(): SoilData {
        // Implementation
    }
}
```

Para los componentes de Angular se utilizará una nomenclatura consistente, por ejemplo:

```text
SoilMonitoringComponent
CropDashboardComponent
WeatherCardComponent
```

Mientras que los archivos utilizarán nombres descriptivos en `kebab-case`, por ejemplo:

```text
soil-monitoring.component.ts
crop-dashboard.component.ts
weather-card.component.ts
```

#### Convenciones para Java

Para el desarrollo de los Web Services con Spring Boot se seguirá como referencia **Google Java Style Guide**, junto con las convenciones recomendadas para proyectos desarrollados con Spring Boot.

Las principales reglas serán:

- Utilizar `PascalCase` para clases.
- Utilizar `camelCase` para variables y métodos.
- Utilizar nombres descriptivos en inglés.
- Utilizar interfaces cuando sea necesario definir contratos entre componentes.
- Mantener una separación clara entre controllers, services, repositories y otras capas de la aplicación.
- Aplicar principios de responsabilidad única en las clases.
- Utilizar inyección de dependencias proporcionada por Spring.
- Mantener los métodos pequeños y enfocados en una responsabilidad específica.

Ejemplo:

```java
public interface SoilDataService {
    SoilData getSoilData(Long id);
}

public class SoilDataServiceImpl implements SoilDataService {

    @Override
    public SoilData getSoilData(Long id) {
        // Implementation
    }
}
```

Para las clases relacionadas con Spring Boot se utilizarán nombres descriptivos según su responsabilidad, por ejemplo:

```text
SoilDataController
SoilDataService
SoilDataRepository
SoilData
```

#### Convenciones para Gherkin

Para la definición de especificaciones y pruebas de aceptación se tomarán como referencia las **Gherkin Conventions for Readable Specifications**.

Las especificaciones utilizarán las palabras clave de Gherkin para describir el comportamiento esperado de las funcionalidades de CultivaTech.

Se utilizará la estructura:

```gherkin
Feature: Soil monitoring

  Scenario: View soil conditions

    Given the user has selected a crop
    When the user opens the soil monitoring section
    Then the system displays the soil conditions
```

Los escenarios estarán escritos de manera clara y orientada al comportamiento esperado del sistema, evitando describir detalles innecesarios de implementación.

#### Convenciones de nomenclatura

| **Elemento** | **Convención** | **Ejemplo** |
|---|---|---|
| Variables | `camelCase` | `soilHumidity` |
| Funciones | `camelCase` | `getSoilData()` |
| Métodos Java | `camelCase` | `calculateFertility()` |
| Clases Java | `PascalCase` | `SoilDataService` |
| Interfaces | `PascalCase` | `SoilDataRepository` |
| Componentes Angular | `PascalCase` | `SoilMonitoringComponent` |
| Archivos Angular | `kebab-case` | `soil-monitoring.component.ts` |
| Clases CSS | `kebab-case` | `soil-monitoring` |
| Constantes | `UPPER_SNAKE_CASE` | `MAX_SOIL_HUMIDITY` |
| Endpoints REST | `kebab-case` | `/api/soil-data` |

#### Referencias de estilo

Las convenciones adoptadas para CultivaTech se basan en las siguientes referencias establecidas para el desarrollo de la solución:

- **HTML Style Guide and Coding Conventions**
- **Google HTML/CSS Style Guide**
- **Gherkin Conventions for Readable Specifications**
- **Angular Coding Style Guide**
- **Google Java Style Guide**
- **Google TypeScript Style Guide**
- **Spring Boot Features**

La aplicación de estas convenciones permitirá que el código de CultivaTech mantenga una estructura uniforme entre los integrantes del equipo, facilitando la lectura, revisión, integración y mantenimiento de los componentes desarrollados durante el proyecto.


## 5.1.4. Software Deployment Configuration.

Con el propósito de garantizar un proceso de despliegue organizado, reproducible y consistente, el equipo de GreenDream ha definido una estrategia de Deployment basada en **GitHub, GitFlow y servicios de alojamiento en la nube**. Esta configuración permitirá gestionar de manera ordenada la publicación de los productos digitales que conforman CultivaTech, asegurando que únicamente las versiones previamente revisadas y validadas sean desplegadas en los entornos correspondientes.

El proceso de despliegue contempla los tres productos principales de la solución: **Landing Page, Frontend Web Application y RESTful Web Services**.

#### Flujo general de Deployment

El proceso de despliegue inicia con el desarrollo de nuevas funcionalidades en ramas **feature**, creadas a partir de la rama **develop**. Una vez finalizada una funcionalidad, el desarrollador realiza un **Pull Request** para que los cambios sean revisados por los integrantes del equipo y se verifique el cumplimiento de las convenciones establecidas.

Después de la aprobación del Pull Request, los cambios son integrados en la rama **develop**, donde se realizan las pruebas correspondientes. Cuando el producto alcanza un estado estable al finalizar el Sprint, se crea una rama **release** para realizar las validaciones finales antes de su publicación.

Finalmente, la rama **release** es fusionada con **main**, la cual contiene las versiones estables del producto. A partir de esta rama se realiza el proceso de despliegue hacia el entorno de producción correspondiente.

El flujo de trabajo aplicado se resume de la siguiente manera:

```text
feature/*
      │
      ▼
develop
      │
      ▼
release/vX.Y.Z
      │
      ▼
main
      │
      ▼
Deployment
      │
      ▼
Production
```

En caso de detectarse un error crítico en producción, el equipo utilizará ramas **hotfix**, las cuales serán creadas a partir de **main**. Una vez corregido y validado el problema, los cambios serán integrados tanto en **main** como en **develop**, manteniendo sincronizadas las versiones del código fuente.

---

#### Landing Page Deployment

La **Landing Page de CultivaTech** será desarrollada utilizando **HTML5, CSS3 y JavaScript** y será publicada mediante **GitHub Pages**, aprovechando su integración con los repositorios de GitHub para el alojamiento de sitios web estáticos.

El proceso de despliegue contempla las siguientes actividades:

1. El desarrollador implementa la funcionalidad correspondiente en una rama **feature**.
2. Se crea un Pull Request hacia la rama **develop**.
3. El equipo revisa los cambios y verifica el cumplimiento de las convenciones de código.
4. Se realizan las pruebas funcionales correspondientes.
5. Una vez que el producto alcanza un estado estable, se crea una rama **release**.
6. La rama **release** es validada y posteriormente fusionada con **main**.
7. GitHub Pages utiliza el contenido configurado del repositorio para publicar la Landing Page.
8. Se verifica que la página se encuentre disponible correctamente mediante HTTPS.

El flujo de despliegue de la Landing Page puede representarse de la siguiente manera:

```text
GitHub Repository
       │
       ▼
feature/*
       │
       ▼
develop
       │
       ▼
release/vX.Y.Z
       │
       ▼
main
       │
       ▼
GitHub Pages
       │
       ▼
Published Landing Page
```

Este procedimiento permitirá mantener una versión estable de la Landing Page y facilitar la publicación de nuevas versiones conforme avance el desarrollo de CultivaTech.

---

#### Frontend Web Application Deployment

La **Frontend Web Application de CultivaTech** será desarrollada utilizando **Angular, TypeScript y Angular Material**, siguiendo los principios de Material Design definidos para la solución.

El despliegue de la aplicación se realizará a partir del repositorio correspondiente en GitHub y contemplará la instalación de dependencias, ejecución de pruebas y generación de una versión optimizada para producción.

El proceso de despliegue seguirá las siguientes actividades:

1. El desarrollador implementa la funcionalidad correspondiente en una rama **feature**.
2. Se crea un Pull Request hacia **develop**.
3. El equipo realiza la revisión del código y valida los cambios.
4. Se ejecutan las pruebas correspondientes para verificar el funcionamiento de la aplicación.
5. Se crea una rama **release** cuando la versión se encuentra preparada para su publicación.
6. La rama **release** es validada y posteriormente fusionada con **main**.
7. Se instalan las dependencias del proyecto mediante **npm**.
8. Se genera la versión de producción de la aplicación Angular.
9. Los archivos generados son publicados en el servicio de alojamiento web o cloud seleccionado para el proyecto.
10. Finalmente, se verifica el acceso y funcionamiento de la aplicación en el entorno de producción.

El flujo general será:

```text
GitHub Repository
       │
       ▼
feature/*
       │
       ▼
develop
       │
       ▼
release/vX.Y.Z
       │
       ▼
main
       │
       ▼
npm install
       │
       ▼
Angular Production Build
       │
       ▼
Cloud Hosting
       │
       ▼
Published Frontend Application
```

Durante la validación del despliegue se verificará principalmente la carga correcta de las vistas, navegación entre funcionalidades, funcionamiento de los componentes de Angular Material y comunicación con los Web Services de CultivaTech.

---

#### RESTful Web Services Deployment

Los **RESTful Web Services de CultivaTech** serán desarrollados utilizando **Java, Spring Boot y Spring Data JPA**, proporcionando los servicios necesarios para la comunicación entre la Frontend Web Application y los datos de la solución.

El despliegue de los servicios será independiente del Frontend y partirá del repositorio correspondiente en GitHub.

El proceso contemplará las siguientes actividades:

1. El desarrollador implementa una nueva funcionalidad en una rama **feature**.
2. Se crea un Pull Request hacia **develop**.
3. El equipo realiza la revisión del código y verifica las convenciones establecidas.
4. Se ejecutan las pruebas unitarias y de integración correspondientes.
5. Una vez validada la versión, se crea una rama **release**.
6. La rama **release** es fusionada con **main** después de las validaciones finales.
7. Se configuran las variables y propiedades necesarias para el entorno de producción.
8. Se ejecuta el proceso de construcción del proyecto Spring Boot.
9. Se genera el artefacto correspondiente para su ejecución en el entorno de producción.
10. El servicio es publicado en el servidor o servicio cloud seleccionado para la solución.
11. Se verifica la disponibilidad de los endpoints REST y su correcta comunicación con la base de datos.
12. Finalmente, se valida la documentación de los servicios mediante **OpenAPI / Swagger**.

El flujo general será:

```text
GitHub Repository
       │
       ▼
feature/*
       │
       ▼
develop
       │
       ▼
Unit / Integration Tests
       │
       ▼
release/vX.Y.Z
       │
       ▼
main
       │
       ▼
Spring Boot Build
       │
       ▼
Cloud / Server Environment
       │
       ▼
RESTful Web Services
```

Durante la validación del despliegue se verificará:

- Correcta compilación del proyecto.
- Disponibilidad de los endpoints REST.
- Correcta conexión con la base de datos.
- Funcionamiento de las pruebas unitarias y de integración.
- Correcta comunicación entre el Frontend y los Web Services.
- Disponibilidad de la documentación OpenAPI mediante Swagger.
- Correcta configuración de las variables necesarias para el entorno de producción.

---

#### Seguridad y disponibilidad

El proceso de despliegue de CultivaTech considera diferentes medidas para mantener la estabilidad y seguridad de los productos publicados.

Entre las principales medidas se encuentran:

- Uso de la rama **main** únicamente para versiones estables.
- Revisión de cambios mediante Pull Requests.
- Aplicación de **GitFlow** para organizar el desarrollo y las liberaciones.
- Uso de **Semantic Versioning** para identificar las versiones publicadas.
- Ejecución de pruebas antes de realizar un despliegue.
- Uso de **HTTPS** en los productos publicados que lo soporten.
- Separación entre el código fuente y las configuraciones específicas del entorno de producción.
- No almacenar credenciales, contraseñas o claves de acceso directamente en el repositorio.
- Respaldo del código fuente mediante GitHub.

Estas medidas permitirán reducir los riesgos asociados a la publicación de nuevas versiones y facilitar la identificación y corrección de posibles problemas durante el ciclo de vida de CultivaTech.

---

#### Configuración del entorno de producción

La configuración del entorno de producción considera los principales productos tecnológicos que conforman la solución CultivaTech y las tecnologías utilizadas para su implementación.

| **Producto** | **Tecnología** | **Plataforma de despliegue** |
|---|---|---|
| Landing Page | HTML5, CSS3, JavaScript | GitHub Pages |
| Frontend Web Application | Angular + TypeScript + Angular Material | Servicio de alojamiento web / Cloud |
| RESTful Web Services | Java + Spring Boot + Spring Data JPA | Servidor / Servicio Cloud |
| Control de versiones | Git | GitHub |
| Documentación de API | OpenAPI / Swagger | Integrada con los Web Services |

La estrategia de despliegue definida permitirá mantener una publicación organizada y consistente de los componentes de CultivaTech. Además, la separación de los productos en diferentes repositorios permitirá desplegar y actualizar la Landing Page, la Frontend Web Application y los Web Services de manera independiente, facilitando el mantenimiento y evolución de la solución durante los siguientes Sprints.