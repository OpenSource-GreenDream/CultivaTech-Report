## 4.4. Web Applications UX/UI Design.

El diseño de experiencia de usuario (UX) y de interfaz de usuario (UI) de CultivaTech busca ofrecer una plataforma intuitiva, accesible y funcional para agricultores. La UX se enfoca en facilitar tareas como el monitoreo de las condiciones del suelo, la gestión de sensores, la consulta de alertas y notificaciones, y el control de productos e inventario mediante flujos de navegación simples y organizados. Por su parte, la UI mantiene una identidad visual coherente con CultivaTech, utilizando una estructura clara que facilita la visualización de información como humedad, nutrientes y estado de los sensores. En conjunto, el diseño UX/UI busca transformar los datos obtenidos mediante dispositivos IoT en información comprensible que permita al agricultor supervisar sus cultivos y tomar decisiones de manera rápida y eficiente.

## 4.4.1. Web Applications Wireframes.

Los siguientes wireframes presentan el flujo inicial de acceso a CultivaTech. La primera pantalla funciona como punto de entrada a la plataforma, permitiendo al usuario seleccionar entre iniciar sesión o crear una nueva cuenta. A partir de esta vista, el usuario puede acceder al formulario de registro (US06), donde ingresa sus datos personales y credenciales, o dirigirse al inicio de sesión (US07) para acceder a las funcionalidades de la aplicación.

![wireframe](assets/chapter-04/inicio-sesion.png){width=500px}

Estos wireframes representan el proceso de recuperación de contraseña (US08). Desde la pantalla de inicio de sesión, el usuario puede seleccionar la opción “¿Olvidaste tu contraseña?” e ingresar el correo electrónico asociado a su cuenta. El sistema inicia el proceso de recuperación e informa al usuario que la solicitud ha sido enviada correctamente.

![wireframe](assets/chapter-04/recuperacion-contraseña.png){width=500px}

Los siguientes wireframes representan la gestión del perfil y el cierre de sesión en CultivaTech. La visualización y edición del perfil (US09) permite al agricultor consultar su información personal registrada, modificar sus datos y guardar los cambios realizados. Por otro lado, el cierre de sesión (US10) permite al usuario finalizar su sesión de manera segura; al seleccionar la opción “Cerrar sesión”, el sistema muestra una ventana de confirmación y, al confirmar la acción, finaliza la sesión y redirige al usuario a la pantalla de acceso.

![wireframe](assets/chapter-04/cuenta-perfil.png){width=500px}

Los siguientes wireframes corresponden al módulo de monitoreo de CultivaTech. La vista de resumen (US11) permite consultar los datos registrados por los sensores, mostrando información como zona, humedad y estado de nutrientes. La vista por zona (US12) permite seleccionar una zona de cultivo específica y consultar los sensores asociados. Finalmente, el historial de humedad (US13) permite analizar la evolución de esta variable durante un periodo determinado.

![wireframe](assets/chapter-04/monitoreo.png){width=500px}

Estos wireframes representan la gestión de sensores de CultivaTech. El registro de un nuevo sensor (US14) permite ingresar el código del dispositivo y asociarlo con una zona de cultivo. Por otro lado, la consulta de sensores registrados (US15) presenta una lista organizada con información relevante de cada dispositivo y su estado dentro del sistema.

![wireframe](assets/chapter-04/sensor.png){width=500px}

Los siguientes wireframes representan las alertas automáticas generadas por CultivaTech. La alerta por baja humedad (US16) aparece cuando un sensor registra un valor inferior al rango establecido, identificando la zona y el sensor afectado. De manera similar, la alerta por nutrientes fuera de rango (US17) informa al agricultor cuando los valores registrados presentan condiciones que requieren atención.

![wireframe](assets/chapter-04/alerta-automatica.png){width=500px}

Estos wireframes corresponden al módulo de notificaciones. La consulta de notificaciones (US18) permite visualizar las alertas actualmente generadas por el sistema. Las preferencias de notificaciones (US19) permiten seleccionar qué tipos de alertas desea recibir el agricultor. Finalmente, el historial de notificaciones (US20) presenta los registros anteriores, incorporando filtros por tipo de alerta, zona, estado y rango de fechas.

![wireframe](assets/chapter-04/notificacion.png){width=500px}

Los siguientes wireframes representan el módulo de Productos e Inventario. El registro de insumos (US21) permite incorporar nuevos recursos utilizados en la actividad agrícola indicando información como nombre, cantidad y unidad. La consulta del inventario (US22) organiza los insumos registrados y muestra su disponibilidad actual.

![wireframe](assets/chapter-04/producto.png){width=500px}

Finalmente, estos wireframes complementan la gestión de Productos e Inventario. La actualización de stock (US23) permite modificar la cantidad disponible de un insumo previamente registrado. El catálogo (US24) presenta los productos agrícolas disponibles mediante tarjetas visuales, mientras que el detalle de producto (US25) permite consultar información específica del elemento seleccionado.

![wireframe](assets/chapter-04/inventario.png){width=500px}

## 4.4.2. Web Applications Wireflow Diagrams.
Los Wireflow Diagrams de CultivaTech representan visualmente los principales flujos de navegación e interacción del usuario dentro de la aplicación web. Estos diagramas muestran el recorrido entre las diferentes interfaces y funcionalidades del sistema, permitiendo comprender la navegación e identificar posibles problemas de usabilidad. El Wireflow Diagram de CultivaTech representa el recorrido del usuario desde el acceso o registro en la aplicación hasta la navegación por sus principales funcionalidades. El flujo muestra la interacción con el panel principal y el acceso a diferentes módulos para consultar información, realizar registros de productos, gestionar datos de sensores y configurar notificaciones, evidenciando cómo se conectan las distintas interfaces del sistema.

![wireflow](assets/chapter-04/wireflow.png){width=500px}

## 4.4.2. Web Applications Mock-ups.
Los Mock-ups de CultivaTech representan visualmente las principales interfaces de la aplicación web y permiten observar cómo el usuario interactuará con sus funcionalidades. Incluyen pantallas para la gestión de usuarios, monitoreo de sensores y zonas, alertas y notificaciones, así como la gestión de inventario y productos.

![wireframe](assets/chapter-04/mockup.png){width=500px}

## 4.4.3. Web Applications User Flow Diagrams.
El diagrama de flujo de usuario es una representación visual de las acciones secuenciales que realiza un usuario al interactuar con la plataforma web CultivaTech. Estos diagramas permiten representar los diferentes recorridos dentro del sistema para acceder al monitoreo de las tierras de cultivo, consultar la información obtenida mediante dispositivos IoT y visualizar las proyecciones generadas a partir de los datos históricos.
**User Flow 1: Registro y Activación de Cuenta**

**User Stories relacionadas:** US06, US08

**Flujos incluidos:** Happy Path, email inválido, contraseña débil, email ya registrado, contraseñas no coinciden, cancelación, enlace expirado.

![flow](assets/chapter-04/userflow-1.png){width=500px}

---

**User Flow 2: Configuración de un Nuevo Sensor IoT**

**User Stories relacionadas:** US14

**Flujos incluidos:** Happy Path, código de sensor inválido, código ya registrado, sensor sin batería o sin conexión, cancelación, campos incompletos.

![flow](assets/chapter-04/userflow-2.png){width=500px}

---

**User Flow 3: Consulta de Recomendación de Riego**

**User Stories relacionadas:** US13

**Flujos incluidos:** Happy Path, no hay datos del sensor (sensor sin conexión), humedad óptima, humedad excesiva, usuario descarta recomendación, usuario modifica umbrales, usuario consulta historial.

![flow](assets/chapter-04/userflow-3.png){width=500px}