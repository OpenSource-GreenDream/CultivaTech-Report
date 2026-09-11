## 4.2. Information Architecture.

La arquitectura de información de CultivaTech se ha definido con el propósito de organizar los contenidos y funcionalidades de la plataforma de manera clara, accesible y comprensible para los usuarios. La estructura contempla tanto la Landing Page, orientada a presentar la solución y facilitar el acceso a la plataforma, como la Web Application, destinada al monitoreo y gestión de los cultivos. De esta manera, los visitantes podrán conocer la propuesta de CultivaTech, solicitar una demostración o iniciar sesión, mientras que los usuarios registrados podrán acceder a las funcionalidades de monitoreo y análisis disponibles en la aplicación.

### 4.2.1. Organization Systems.

CultivaTech organizará visualmente la información de acuerdo con su importancia y el contexto en el que se encuentre el usuario. Para ello, se aplicarán diferentes criterios de jerarquización y distribución de contenido tanto en la Landing Page como en la Web Application:

- En la Landing Page, la información seguirá una organización jerárquica y secuencial. Se iniciará con el Hero Section, donde se presentará el nombre de CultivaTech, su propuesta de valor, una descripción breve y el botón "Solicitar Demo". Posteriormente, se mostrarán las características principales de la solución, información sobre el proyecto y el equipo de desarrollo. Asimismo, se dispondrá de la opción "Iniciar Sesión" para permitir el acceso a la Web Application.

- En el Dashboard de Monitoreo de la Web Application, los datos que requieren mayor atención tendrán prioridad visual. Los indicadores relacionados con las condiciones del cultivo y las alertas generadas por el sistema serán mostrados en posiciones destacadas mediante tamaños, colores y elementos visuales que permitan reconocer rápidamente el estado del cultivo.

- En aquellos procesos que requieren el ingreso de información, como el registro de usuarios, el inicio de sesión, la incorporación de un nuevo sensor IoT o la solicitud de una demostración, los formularios se organizarán de manera clara y secuencial. De esta forma, el usuario podrá completar cada proceso reduciendo errores y evitando presentar demasiada información al mismo tiempo.

- Para la interpretación de información histórica y geográfica, CultivaTech empleará estructuras visuales que permitan relacionar diferentes variables. Los datos recopilados podrán presentarse mediante gráficos, indicadores y representaciones del terreno que faciliten la identificación de cambios y tendencias en las condiciones del cultivo.

### 4.2.2. Labeling Systems.

CultivaTech utilizará un sistema de etiquetas consistente que permita identificar fácilmente las secciones, funcionalidades, métricas y acciones disponibles. El lenguaje empleado buscará mantener un equilibrio entre los términos relacionados con la agricultura y expresiones comprensibles para los diferentes tipos de usuario.

- ***Visitantes y nuevos usuarios:*** La Landing Page utilizará etiquetas de navegación como "Inicio", "Características", "Sobre el Proyecto", "Equipo", "Solicitar Demo" e "Iniciar Sesión". El botón "Solicitar Demo" permitirá acceder al formulario correspondiente, mientras que "Iniciar Sesión" permitirá a los usuarios registrados acceder a la Web Application.

- ***Formulario de solicitud de demo:*** Los campos utilizarán etiquetas claras para identificar la información requerida. En caso de que un campo obligatorio no sea completado, se mostrará un mensaje de validación. Cuando el formulario sea enviado correctamente, se mostrará un mensaje de confirmación.

- ***Agricultores:*** Los indicadores relacionados con el monitoreo utilizarán nombres y unidades que permitan interpretar rápidamente los datos, como "Humedad (%)", "Nutrientes (N-P-K ppm)" y "Temperatura (°C)". Las acciones principales se identificarán mediante etiquetas como "Agregar Sensor", "Ver historial" o "Ver recomendaciones".

- ***Administradores de Cooperativa:*** Los módulos orientados a la gestión utilizarán etiquetas relacionadas con el análisis consolidado de información, como "Reportes", "Dashboard Agregado", "Rendimiento promedio" y "Hectáreas totales".

- ***Información legal:*** Se utilizará la etiqueta "Términos y Condiciones" para permitir que el visitante pueda acceder fácilmente a las condiciones de uso de CultivaTech.

### 4.2.3. SEO Tags and Meta Tags

Los SEO tags son etiquetas HTML que ayudan a los motores de búsqueda a comprender e identificar el contenido de una página. Por otro lado, los meta tags proporcionan información como la descripción, idioma y autor. En CultivaTech, estos elementos estarán orientados principalmente a la Landing Page, debido a que corresponde al contenido público de la plataforma.

***Title Tag:*** Este tag define el título de la página y permite identificar el contenido principal de CultivaTech en los motores de búsqueda.

```html
<title>CultivaTech - Monitoreo Inteligente de Cultivos con IoT</title>
```

***Meta Description:*** Proporciona una descripción breve del contenido y propuesta de valor de CultivaTech.

```html
<meta name="description" content="CultivaTech es una solución tecnológica de GreenDream que utiliza dispositivos IoT y análisis de datos para apoyar el monitoreo y gestión de tierras de cultivo.">
```

***Language Tag:*** Indica el idioma principal utilizado en la página.

```html
<meta http-equiv="Content-Language" content="es-PE">
```

***Robots Tag:*** Indica a los motores de búsqueda que la Landing Page puede ser indexada.

```html
<meta name="robots" content="index, follow">
```

***Author Tag:*** Identifica al equipo responsable del contenido y desarrollo de la plataforma.

```html
<meta name="author" content="GreenDream Team">
```

***Meta Viewport:*** Permite que la interfaz se adapte correctamente a diferentes tamaños de pantalla y dispositivos.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

***Canonical Tag:*** Especifica la URL principal de la Landing Page para evitar problemas relacionados con contenido duplicado.

```html
<link rel="canonical" href="https://www.cultivatech.com/">
```

### 4.2.4. Searching Systems

CultivaTech utilizará diferentes mecanismos de navegación, búsqueda y filtrado para facilitar que los usuarios encuentren la información que necesitan tanto en la Landing Page como en la Web Application.

- ***Navegación en la Landing Page:*** Debido a que la información estará distribuida en secciones claramente identificadas, el visitante podrá utilizar el menú principal para acceder rápidamente a "Inicio", "Características", "Sobre el Proyecto" y "Equipo".

- ***Acceso a Solicitar Demo:*** El botón "Solicitar Demo" permitirá dirigir al visitante hacia el formulario correspondiente para realizar una solicitud de demostración.

- ***Acceso a la Web Application:*** La opción "Iniciar Sesión" permitirá que los usuarios registrados accedan desde la Landing Page a la pantalla de autenticación de la Web Application.

- ***Búsqueda de zonas y sensores:*** Dentro de la Web Application se utilizarán filtros y selectores para que el agricultor pueda identificar una zona de cultivo o un sensor específico y consultar la información correspondiente.

- ***Búsqueda en el historial de datos:*** Se utilizarán filtros por rango de fechas y tipo de métrica, como humedad, nutrientes o temperatura, para consultar la evolución de los datos recopilados.

- ***Búsqueda de socios y reportes:*** Los administradores de cooperativas podrán localizar información correspondiente a socios o lotes específicos y acceder a los datos consolidados disponibles en la plataforma.

### 4.2.5. Navigation Systems

El sistema de navegación de CultivaTech permitirá que los usuarios se desplacen fácilmente entre los contenidos de la Landing Page y las funcionalidades disponibles en la Web Application.

***Landing Page***

- ***Hero Section:*** Presentará el nombre de CultivaTech, un título principal, una descripción breve de la solución y el botón "Solicitar Demo".

- ***Características:*** Permitirá al visitante conocer las principales funcionalidades de CultivaTech mediante títulos y descripciones breves.

- ***Sobre el Proyecto:*** Presentará información relacionada con el propósito y objetivo de CultivaTech.

- ***Equipo:*** Permitirá conocer los nombres y roles de los integrantes responsables del desarrollo del proyecto.

- ***Solicitar Demo:*** Permitirá acceder al formulario de solicitud de demostración. El sistema validará los campos obligatorios y mostrará un mensaje de confirmación cuando la solicitud sea enviada correctamente.

- ***Iniciar Sesión:*** Permitirá a los usuarios registrados dirigirse desde la Landing Page hacia la pantalla de autenticación de la Web Application.

- ***Términos y Condiciones:*** Permitirá al visitante acceder y visualizar las condiciones de uso de CultivaTech.

***Web Application***

- ***Registro e Inicio de Sesión:*** Permitirá al usuario registrarse o ingresar mediante sus credenciales para acceder a las funcionalidades disponibles en CultivaTech.

- ***Dashboard de Monitoreo:*** Permitirá visualizar los principales indicadores obtenidos mediante los dispositivos IoT y conocer el estado general de los cultivos.

- ***Monitoreo de Cultivos:*** Permitirá consultar los indicadores relacionados con las condiciones de las tierras de cultivo y visualizar los datos recopilados por los dispositivos IoT.

- ***Historial y Análisis:*** Permitirá consultar la evolución de los indicadores mediante gráficos, filtros y rangos de fechas para facilitar el análisis de la información.

- ***Mapas y Análisis:*** Permitirá visualizar gráficamente las diferentes zonas del terreno y consultar información relacionada con sus condiciones.

- ***Gestión de Dispositivos:*** Permitirá registrar y administrar los dispositivos IoT asociados a las tierras de cultivo.

- ***Recomendaciones:*** Permitirá consultar información generada a partir del análisis de los datos recopilados y del historial de los cultivos.

- ***Mi Perfil:*** Permitirá al usuario consultar y actualizar la información relacionada con su cuenta y sus preferencias.