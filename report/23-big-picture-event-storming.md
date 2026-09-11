## 2.4. Big Picture Event Storming

El equipo llevó a cabo una sesión colaborativa de Big Picture Event Storming utilizando la herramienta Miro, con el objetivo de explorar el dominio del negocio agrícola de CultivaTech a alto nivel. A diferencia de un flujo técnico o de registro de usuarios, el Big Picture Event Storming se enfoca en capturar el flujo de negocio completo que ocurre en el mundo real del agricultor, desde la preparación de la tierra hasta la comercialización de los productos.

Durante la sesión, se identificaron los eventos significativos que ocurren en el ciclo de vida del cultivo y la interacción con los actores del ecosistema. El proceso permitió visualizar el flujo completo del negocio agrícola, exponiendo las relaciones entre los eventos clave, los actores involucrados (agricultor, tierra, clima, proveedores, clientes finales) y las políticas de negocio que rigen el comportamiento del sistema.

A continuación, se presentan los principales elementos identificados en el Big Picture Event Storming:

### Domain Events (Eventos de Dominio)
Eventos en tiempo pasado que ocurren en el proceso de negocio:
* **Soil Prepared** (Tierra preparada)
* **Crop Planted** (Cultivo sembrado)
* **Soil Moisture Changed** (Humedad del suelo cambió)
* **Nutrient Level Changed** (Nivel de nutrientes cambió)
* **Irrigation Applied** (Riego aplicado)
* **Fertilizer Applied** (Fertilizante aplicado)
* **Weather Alert Received** (Alerta climática recibida)
* **Crop Growth Stage Updated** (Etapa de crecimiento actualizada)
* **Pest Detected** (Plaga detectada)
* **Crop Harvested** (Cultivo cosechado)
* **Yield Recorded** (Rendimiento registrado)
* **Product Listed for Sale** (Producto listado para venta)
* **Product Sold** (Producto vendido)
* **Traceability QR Generated** (Código QR de trazabilidad generado)
* **Sustainability Report Generated** (Reporte de sostenibilidad generado)

### Actors (Actores)
Personas o sistemas que ejecutan comandos o generan eventos:
* **Farmer (Agricultor):** Actor principal que prepara, siembra, riega, fertiliza y cosecha.
* **Soil (Tierra/Suelo):** Actor pasivo que genera eventos de cambio de humedad y nutrientes mediante la red de sensores IoT.
* **Weather (Clima):** Actor externo que genera alertas climáticas.
* **Advisor / Supplier (Asesor / Proveedor):** Actor que recomienda insumos basados en los datos de suelo recolectados.
* **End Customer (Cliente Final / B2B):** Actor que compra productos y verifica la trazabilidad.

### External Systems (Sistemas Externos)
* **IoT Sensor Network (LoRaWAN):** Red de sensores físicos de suelo y puerta de enlace.
* **Weather API Service:** Servicio meteorológico para alertas preventivas.
* **E-commerce Platform / Payment Gateway:** Plataformas para gestión de ventas.

### Policies (Políticas)
Reglas de negocio que se disparan ante eventos específicos:
* **When Soil Moisture drops below 30%, trigger Irrigation Recommendation:** Cuando la humedad del suelo baja del 30%, se dispara la recomendación de riego (alerta sonora y semáforo).
* **When Nutrient N drops below 20 ppm, trigger Fertilizer Recommendation:** Cuando el nitrógeno baja de 20 ppm, se dispara la recomendación de fertilización.
* **When Pest is Detected, trigger Pest Control Alert:** Cuando se detecta una plaga, se dispara la alerta de control de plagas al agricultor y asesor.
* **When Crop is Harvested, update Inventory and Yield Records:** Cuando se cosecha, se actualiza el inventario y los registros de rendimiento proyectado.
* **When Product is Listed, generate Traceability QR Code:** Cuando se lista un producto, se genera el código QR de trazabilidad para el cliente final.


## 2.5. Ubiquitous Language

El siguiente glosario define los términos y conceptos clave del dominio de negocio de CultivaTech, asegurando una comunicación clara y sin ambigüedades entre todos los miembros del equipo y stakeholders. Los términos están presentados en inglés (con el equivalente en español entre paréntesis) y sus definiciones están redactadas en español.

### Identity & Access Management

| Term (English) | Term (Spanish) | Definition (in Spanish) |
| :--- | :--- | :--- |
| **User** | Usuario | Persona que interactúa con la aplicación. Puede ser agricultor, proveedor de insumos o administrador. |
| **Register User** | Registrar usuario | Acción de crear una cuenta nueva en el sistema. |
| **Login** | Iniciar sesión | Proceso de autenticación para acceder a la plataforma. |
| **Credentials** | Credenciales | Conjunto de datos (correo/teléfono, contraseña) para la autenticación. |
| **User registered** | Usuario registrado | Evento que indica que una nueva cuenta ha sido creada exitosamente. |

---

### Profiles & Preferences Management

| Term (English) | Term (Spanish) | Definition (in Spanish) |
| :--- | :--- | :--- |
| **Profile** | Perfil | Información personal y agrícola del usuario (nombre, ubicación, tipo de cultivo). |
| **Preferences** | Preferencias | Configuración personalizada definida por el usuario (frecuencia de alertas, tipo de notificación). |
| **Profile created** | Perfil creado | Evento que indica que se creó un perfil asociado a un usuario. |
| **Preferences updated** | Preferencias actualizadas | Evento que indica que el usuario cambió su configuración de alertas o idioma. |

---

### IoT Monitoring & Crop Management

| Term (English) | Term (Spanish) | Definition (in Spanish) |
| :--- | :--- | :--- |
| **IoT Sensor Node** | Nodo Sensor IoT | Dispositivo físico instalado en campo que mide variables del suelo (humedad, pH, NPK). |
| **LoRaWAN Gateway** | Antena LoRaWAN | Estación base que recibe la telemetría de los sensores en zonas con baja conectividad. |
| **Soil Telemetry** | Telemetría del suelo | Datos periódicos transmitidos por los sensores con lecturas de la tierra. |
| **Traffic Light Indicator** | Semáforo de estado | Interfaz visual simplificada (Verde/Amarillo/Rojo) para mostrar la condición del suelo. |
| **Irrigation Alert** | Alerta de riego | Notificación emitida cuando la humedad del suelo cae por debajo del umbral óptimo. |

---

### Payments & Subscriptions

| Term (English) | Term (Spanish) | Definition (in Spanish) |
| :--- | :--- | :--- |
| **Subscription** | Suscripción | Relación activa entre el agricultor y el plan de monitoreo IoT contratado. |
| **Subscription started** | Suscripción iniciada | Evento que indica el inicio de un plan de servicio. |
| **Payment** | Pago | Transacción financiera para habilitar el servicio o renovar la suscripción. |
| **Payment processed** | Pago procesado | Evento que confirma que un pago fue realizado exitosamente. |
| **Plan** | Plan | Conjunto de servicios (cantidad de sensores monitoreados, alertas predictivas) con un precio definido. |