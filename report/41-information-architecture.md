## 4.2. Information Architecture.

La arquitectura de información de TerraTech se ha definido con el propósito de organizar los contenidos y funcionalidades de la plataforma de manera clara, accesible y comprensible para los usuarios. La estructura propuesta busca facilitar la navegación y permitir que agricultores y administradores de cooperativas encuentren rápidamente la información necesaria para monitorear cultivos, consultar indicadores y gestionar los recursos disponibles en la plataforma.

### 4.2.1. Organization Systems.

TerraTech organizará visualmente la información de acuerdo con su importancia y el contexto en el que se encuentre el usuario. Para ello, se aplicarán diferentes criterios de jerarquización y distribución de contenido dentro de la plataforma:

- En el Dashboard de Monitoreo, los datos que requieren mayor atención tendrán prioridad visual. Las alertas críticas relacionadas con el riego, así como los indicadores de humedad y nutrientes N-P-K, serán mostrados en posiciones destacadas mediante tamaños, colores y elementos visuales que permitan reconocer rápidamente el estado del cultivo. En la Landing Page se seguirá un criterio similar, comenzando por la propuesta de valor de TerraTech y continuando progresivamente con sus características y beneficios.

- En aquellos procesos que requieren el ingreso de información, como el registro de usuarios, la incorporación de un nuevo sensor IoT o la solicitud de una demostración, los formularios se organizarán de manera secuencial. De esta forma, el usuario podrá completar cada proceso mediante pasos claramente diferenciados, reduciendo errores y evitando presentar demasiada información al mismo tiempo.

- Para la interpretación de información geográfica y comparativa, TerraTech empleará estructuras visuales que permitan relacionar diferentes variables. En el Mapa de Calor de Fertilidad, por ejemplo, se representarán las diferentes zonas del terreno utilizando colores asociados al estado del suelo. Asimismo, en los módulos destinados a cooperativas se podrá organizar información de diferentes socios o lotes mediante tablas que permitan comparar indicadores de rendimiento, humedad y alertas.

### 4.2.2. Labeling Systems.

TerraTech utilizará un sistema de etiquetas consistente que permita identificar fácilmente las funcionalidades, métricas y acciones disponibles. El lenguaje empleado buscará mantener un equilibrio entre los términos propios de la agricultura de precisión y expresiones comprensibles para los diferentes tipos de usuario.

- ***Visitantes y nuevos usuarios:*** La Landing Page utilizará llamados a la acción fácilmente reconocibles, como "Solicitar Demo", acompañados de etiquetas claras en los formularios para solicitar únicamente la información necesaria, como nombre, datos de contacto y características generales del terreno.

- ***Agricultores:*** Los indicadores relacionados con el monitoreo utilizarán nombres y unidades que permitan interpretar rápidamente los datos, como "Humedad (%)", "Nutrientes (N-P-K ppm)" y "Temperatura (°C)". Las acciones principales se identificarán mediante etiquetas como "Agregar Sensor", "Ver historial" o "Ver recomendaciones". Las alertas mostrarán mensajes breves y orientados a una acción específica.

- ***Administradores de Cooperativa:*** Los módulos orientados a la gestión utilizarán etiquetas relacionadas con el análisis consolidado de información, como "Reportes", "Dashboard Agregado", "Rendimiento promedio" y "Hectáreas totales". Asimismo, se utilizarán acciones como "Exportar PDF" para facilitar la generación y consulta de reportes.

### 4.2.3. SEO Tags and Meta Tags
Los SEO tags son etiquetas HTML que ayudan a los motores de búsqueda a entender y posicionar en los resultados. Los meta tags son etiquetas que proporcionan información sobre la página, como su descripción, palabras clave y autor, lo cual ayuda al ser buscado en el navegador. A continuación se presentan los SEO tags y meta tags que se utilizarán en la plataforma TerraTech:

***Title Tag:*** Este tag define el título de la página y es uno de los factores más importantes para el SEO. Debe ser único y contener palabras clave relevantes.

```html
<title>TerraTech - Monitoreo Inteligente y Agricultura de Precisión IoT</title>
```

***Meta Description:*** Este tag proporciona una breve descripción del contenido de la página. Permite a los usuarios entender de qué trata la página antes de hacer clic en el enlace. Debe ser conciso y atractivo.

```html
<meta name="description" content="TerraTech es una plataforma de agricultura inteligente que optimiza el riego y la fertilización mediante sensores IoT en tiempo real, mapas de fertilidad y análisis predictivo para agricultores.">
```

***Language tag:*** Este tag indica el idioma principal del contenido de la página. Es importante para la accesibilidad y el SEO.

```html
<meta http-equiv="Content-Language" content="es-PE">
```

***Robots tag:*** Este tag indica a los motores de búsqueda cómo deben indexar la página. Puede ser utilizado para evitar que ciertas páginas sean indexadas (por ejemplo, el dashboard interno).

```html
 <meta name="robots" content="index, follow">
```

***Author tag:*** Este tag indica el autor del contenido de la página. Es útil para dar crédito a los creadores de contenido.

```html
<meta name="author" content="NovaTech Agro Team">
```

***Meta Viewport:*** Este tag es esencial para que la página sea responsiva en dispositivos móviles (vital para agricultores en el campo). Mejora la experiencia del usuario y es un factor importante para el SEO técnico.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

***Canonical Tag:*** Este tag especifica la URL canónica de la página para evitar problemas de contenido duplicado en motores de búsqueda. Ayuda a consolidar el posicionamiento de una sola versión de la página.***

```html
<link rel="canonical" href="https://www.terratech-agro.com/">
```

### 4.2.4. Searching Systems

Para encontrar ciertas funcionalidades de nuestra aplicación, usamos varios botones y empleamos varios indicadores visuales para que el usuario sepa dónde encontrar lo que necesita. A continuación se muestran los ejemplos de los tipos de búsqueda que usaremos:

- ***Búsqueda de zonas y sensores:*** Para facilitar el monitoreo en fincas grandes, usamos una serie de filtros y un selector desplegable para que el agricultor pueda hallar exactamente la zona de cultivo o el sensor individual (ID) del cual desea ver los datos en tiempo real.

- ***Búsqueda en histórico de datos:*** Usamos filtros por rango de fechas y tipo de métrica (Humedad, Nitrógeno, Fósforo, Potasio o Temperatura) para que el agricultor pueda graficar las tendencias de los últimos días y detectar patrones en su suelo.

- ***Búsqueda de socios y reportes:*** Para los administradores de la cooperativa, se les da una forma de buscar rápidamente el rendimiento por socio o por lote específico, permitiéndoles acceder ágilmente al dashboard consolidado y a la exportación de reportes en PDF.

### 4.2.5. Navigation Systems

- ***Registro e Inicio de Sesión:*** Para poder entrar, el usuario ingresará sus credenciales y el sistema registrará qué tipo de usuario es: Agricultor, que busca monitorear sus sembríos y recibir recomendaciones de riego/fertilización, o Administrador de Cooperativa, que requiere visualizar métricas globales y reportes de todos los socios.

- ***Dashboard de Monitoreo:*** Permite a los usuarios visualizar los indicadores clave del suelo en tiempo real, ver el pronóstico del clima integrado y acceder rápidamente a las notificaciones y recomendaciones predictivas del sistema.

- ***Mapas y Análisis:*** Permite a los agricultores navegar de forma interactiva (zoom y desplazamiento) sobre el mapa de calor de fertilidad de su terreno y visualizar imágenes satelitales recientes para identificar áreas críticas.

- ***Gestión de Dispositivos:*** Una sección dedicada donde el agricultor puede registrar nuevos sensores físicos a su cuenta y configurar los umbrales personalizados de alerta para cada métrica.

- ***Mi perfil:***  Permite a los usuarios configurar sus preferencias personales, actualizar la información técnica de su finca o cooperativa, y cambiar su contraseña.

