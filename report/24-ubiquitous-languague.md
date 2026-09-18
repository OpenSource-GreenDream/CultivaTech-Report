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

| Term (English)           | Term (Spanish)       | Definition (in Spanish)                                                                                |
|:-------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| **Subscription**         | Suscripción          | Relación activa entre el agricultor y el plan de monitoreo IoT contratado.                             |
| **Subscription started** | Suscripción iniciada | Evento que indica el inicio de un plan de servicio.                                                    |
| **Payment**              | Pago                 | Transacción financiera para habilitar el servicio o renovar la suscripción.                            |
| **Payment processed**    | Pago procesado       | Evento que confirma que un pago fue realizado exitosamente.                                            |
| **Plan**                 | Plan                 | Conjunto de servicios (cantidad de sensores monitoreados, alertas predictivas) con un precio definido. |