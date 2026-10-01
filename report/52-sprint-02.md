## 5.2.2. Sprint 2

### 5.2.2.1. Sprint Planning 2.
A través de una reunión en la plataforma Google Meet, se llevó a cabo la planificación del Sprint 2. Durante la sesión se definieron los objetivos orientados al desarrollo de las principales funcionalidades de la aplicación web CultivaTech, considerando la implementación de los bounded contexts asignados al equipo. , la integración de los servicios backend necesarios para el funcionamiento de las funcionalidades implementadas y el avance de la documentación técnica del proyecto.

| **Campo** | **Descripción** |
| :--- | :--- |
| **Número** | Sprint 2 |
| **Sprint Planning Background** | Continuación del desarrollo del proyecto GreenDream, avanzando en la implementación de la aplicación web CultivaTech mediante el desarrollo de sus principales bounded contexts, la integración de servicios backend y la documentación técnica del proyecto. |
| **Date** | 2026-09-21 |
| **Time** | 10:00 a.m. - 12:00 p.m. |
| **Location** | Plataforma Google Meet |
| **Prepared by** | Jorge Manuel Retuerto Rodriguez |
| **Attendees** | Jean Pierre Condor Sandoval, Maria Luisa Munayco Apolaya, Renzo Piero Santos Minaya, Jorge Manuel Retuerto Rodriguez, Rosangela Karen Silva Hualpa |
| **Sprint n-1 Review Summary** | Durante el Sprint 1 se desarrolló la primera versión de la Landing Page de CultivaTech y se avanzó en la documentación inicial del proyecto, estableciendo las bases necesarias para continuar con el desarrollo de la aplicación web. |
| **Sprint n-1 Retrospective Summary** | Durante la retrospectiva del Sprint 1 se identificó la necesidad de mejorar la organización y trazabilidad del trabajo mediante una distribución más clara de las tareas y el uso de buenas prácticas de desarrollo para la integración de las funcionalidades del proyecto. |
| **Sprint Goal & User Stories** | Desarrollar las principales funcionalidades de la aplicación web CultivaTech mediante la implementación de los bounded contexts definidos para el proyecto, considerando la integración de servicios backend y el avance de la documentación técnica correspondiente. |
| **Sprint 2 Goal** | **Implementar las principales funcionalidades de la aplicación web CultivaTech:**<br>Nuestro enfoque es desarrollar e integrar las funcionalidades correspondientes a los bounded contexts priorizados durante el Sprint 2: Monitoring Management, Analytics Management, Identity & Access Management (IAM), Commercial Management, Stock Management y Notification Management, junto con los componentes compartidos necesarios para su funcionamiento. El desarrollo contempla funcionalidades relacionadas con la autenticación de usuarios, monitoreo y registro de sensores, visualización de indicadores, gestión de inventario, procesos comerciales y gestión de notificaciones. Creemos que esto permitirá consolidar el núcleo funcional de CultivaTech y avanzar desde la propuesta inicial hacia una aplicación web integrada. El éxito se confirmará cuando las User Stories planificadas para el Sprint 2 se encuentren implementadas, integradas y disponibles para su revisión en el entorno de desarrollo.<br><br>**Avance del Backend y Arquitectura:**<br>Se avanzará en la integración de los servicios necesarios para consumir y gestionar la información utilizada por los diferentes bounded contexts, manteniendo la separación de responsabilidades definida en la arquitectura de CultivaTech y la organización modular de la aplicación. |
| **Sprint 2 velocity** | 51 Story Points (SP) |
| **Sum of Story Points** | 51 |

Durante el Sprint 2 se priorizó la implementación del núcleo funcional de la aplicación web CultivaTech. Las actividades fueron organizadas considerando el desarrollo de las funcionalidades correspondientes a los bounded contexts de Identity & Access Management (IAM), Monitoring Management, Notification Management, Stock Management y Commercial Management, además de los componentes compartidos necesarios para su integración. El trabajo se orientó a implementar las User Stories seleccionadas para el sprint y avanzar en la construcción de una aplicación funcional e integrada.

### 5.2.2.2. Aspect Leaders and Collaborators

En este sprint, se definieron roles de liderazgo y colaboración para las diferentes áreas del proyecto.

| Team member | Github username | IAM / Commercial / Shared | Analytics | Monitoring | Stock | Notifications | Documentation |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| Jean Pierre Condor Sandoval | `jeanpcs` | C | L | C | C | C | C |
| Jorge Manuel Retuerto Rodriguez | `Calin1407` | L | C | C | C | C | C |
| Maria Luisa Munayco Apolaya | `malumunayco` | C | C | C | C | L | C |
| Renzo Piero Santos Minaya | `RSSint` | C | C | C | L | C | C |
| Rosangela Karen Silva Hualpa | `amazcoffee2` | C | C | L | C | C | L |

### 5.2.2.3. Sprint Backlog 2
Tabla con el detalle de las tareas asignadas para cumplir con las historias de usuario del Sprint 2.

#### 5.2.2.3. Sprint Backlog 2

El Sprint Backlog 2 contiene las User Stories y tareas priorizadas para el desarrollo de las principales funcionalidades de CultivaTech. Las actividades fueron distribuidas entre los bounded contexts trabajados durante el sprint, incluyendo Identity & Access Management, Analytics Management, Monitoring Management, Stock Management y Notification Management.

| **User Story ID** | **User Story Title** | **Work-item / Task ID** | **Task Title** | **Description** | **Estimation (Hours)** | **Assigned to** | **Status** |
| :--- | :--- | :--- | :--- | :--- | :---: | :--- | :--- |
| US06 | Registro de Nuevo Usuario | Task 6.1 | Diseñar componente de registro | Diseñar e implementar la interfaz necesaria para el registro de nuevos usuarios en CultivaTech. | 3 | Jorge Manuel Retuerto Rodriguez | Done |
| US06 | Registro de Nuevo Usuario | Task 6.2 | Implementar validaciones visuales del registro | Incorporar las validaciones visuales necesarias en los campos del formulario de registro de usuario. | 2 | Jorge Manuel Retuerto Rodriguez | Done |
| US07 | Inicio de Sesión | Task 7.1 | Diseñar componente de inicio de sesión | Diseñar e implementar la interfaz que permita a los usuarios registrados iniciar sesión en CultivaTech. | 3 | Jorge Manuel Retuerto Rodriguez | Done |
| US07 | Inicio de Sesión | Task 7.2 | Implementar validaciones visuales de inicio de sesión | Incorporar validaciones visuales en los campos requeridos para el inicio de sesión. | 2 | Jorge Manuel Retuerto Rodriguez | Done |
| US10 | Visualización de Indicadores Clave | Task 10.1 | Definir modelos y entidades para datos de analítica (Analytics Management) | Definir los modelos y entidades necesarios para representar los datos utilizados en Analytics Management. | 2 | Jean Pierre Condor Sandoval | ToProgress |
| US10 | Visualización de Indicadores Clave | Task 10.2 | Implementar servicios de API y endpoints para indicadores clave | Implementar los servicios necesarios para obtener los datos utilizados en los indicadores clave. | 3 | Jean Pierre Condor Sandoval | ToProgress |
| US10 | Visualización de Indicadores Clave | Task 10.3 | Diseñar e integrar componentes visuales y gráficos del Dashboard | Diseñar e integrar los componentes visuales y gráficos necesarios para presentar los indicadores en el Dashboard. | 3 | Jean Pierre Condor Sandoval | ToProgress |
| US11 | Visualización de Datos de Sensores | Task 11.1 | Implementar obtención de datos de sensores | Implementar la obtención de la información registrada por los sensores para su posterior visualización. | 3 | Rosangela Karen Silva Hualpa | Done |
| US11 | Visualización de Datos de Sensores | Task 11.2 | Diseñar e implementar vista de monitoreo de sensores | Diseñar e implementar la interfaz para consultar los sensores y los valores registrados en las zonas de cultivo. | 3 | Rosangela Karen Silva Hualpa | Done |
| US12 | Selección de Zona | Task 12.1 | Implementar filtrado de sensores por zona de cultivo | Implementar un filtro que permita visualizar los sensores correspondientes a una zona de cultivo seleccionada. | 2 | Rosangela Karen Silva Hualpa | Done |
| US13 | Visualización del Historial de Humedad | - | Visualización del historial de humedad | Implementar la visualización del historial de humedad registrado por los sensores para consultar su comportamiento a lo largo del tiempo. | 3 | Rosangela Karen Silva Hualpa | Done |
| US14 | Registro de Nuevo Sensor | Task 14.1 | Implementar lógica de registro de nuevo sensor | Implementar la lógica necesaria para incorporar un nuevo sensor y asociarlo a una zona de cultivo. | 3 | Rosangela Karen Silva Hualpa | Done |
| US14 | Registro de Nuevo Sensor | Task 14.2 | Diseñar e implementar formulario de registro de sensor | Diseñar e implementar el formulario utilizado para ingresar la información correspondiente a un nuevo sensor. | 3 | Rosangela Karen Silva Hualpa | Done |
| US15 | Consulta de Sensores Registrados | - | Consulta de sensores registrados | Implementar la visualización de los sensores previamente registrados y asociados al usuario. | 2 | Rosangela Karen Silva Hualpa | Done |

### 5.2.2.4. Development Evidence for Sprint Review
Registro de commits representativos del trabajo realizado durante el Sprint 2 en los repositorios de la organización.


### 5.2.2.5. Execution Evidence for Sprint Review

### 5.2.2.6. Services Documentation Evidence for Sprint Review
### 5.2.2.7. Software Deployment Evidence for Sprint Review
### 5.2.2.8. Team Collaboration Insights during Sprint