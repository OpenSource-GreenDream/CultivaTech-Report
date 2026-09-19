## 4.6. Domain-Driven Software Architecture.

## 4.6.1. Design-Level Event Storming.
Para definir la arquitectura de CultivaTech orientada al dominio (DDD), se llevó a cabo un proceso iterativo de Design-Level Event Storming siguiendo la metodología de 10 pasos. Este análisis nos permitió alinear la lógica del negocio agrícola con la implementación tecnológica. A continuación, se detalla la evolución del modelo:

**Step 1: Unstructured Exploration**

Durante esta fase inicial, se identificaron y representaron cronológicamente todos los eventos que modifican el estado dentro del ecosistema de la plataforma. Estos eventos fueron redactados en tiempo pasado (representados simbólicamente en post-its naranjas), cubriendo el flujo completo desde la interacción del hardware hasta la analítica de datos. Entre los eventos más relevantes identificados se encuentran:

![event storming](assets/chapter-04/step1.png){width=500px}

**Step 2: Chronology**

Se ordenaron los eventos del dominio de forma cronológica de izquierda a derecha, estableciendo el flujo del ciclo de vida del monitoreo agrícola.

![event storming](assets/chapter-04/step2.png){width=500px}

**Step 3: Pain Points**

Se identificaron los puntos críticos y riesgos técnicos del negocio mediante rombos rosas, enfocándose en desafíos como la determinación exacta de dispositivos necesarios por zona de cultivo, la simplificación de procesos para evitar pasos innecesarios y la optimización de los reportes para que entreguen solo datos de alto valor. Asimismo, se cuestionó la fiabilidad del historial frente a irregularidades del terreno para asegurar que las proyecciones de cosecha sean precisas y útiles para el agricultor.

![event storming](assets/chapter-04/step3.png){width=500px}

**Step 4: Pivotal Points**

Se definieron los eventos pivote que marcan cambios significativos en el estado del sistema, dividiendo el flujo en fases claras: el Registro de cuenta y el Pago de suscripción como hitos iniciales, seguidos por la Activación de dispositivos IoT que da inicio al monitoreo, y finalmente la Generación de reportes y Proyección de cosechas, que consolidan la entrega de valor predictivo para el agricultor.

![event storming](assets/chapter-04/step4.png){width=500px}

**Step 5: Commands**

Se identificaron los comandos (post-its azules) que representan las intenciones de los usuarios para provocar cambios en el sistema, junto con los actores (post-its amarillos) responsables de ejecutarlos. Los actores principales definidos son el Agricultor, el Proveedor y el Cliente final, quienes interactúan mediante acciones clave como Registrar usuario, Seleccionar plan de suscripción, Registrar zona de cultivo y Exportar reporte.

![event storming](assets/chapter-04/step5.png){width=500px}


**Step 6: Policies**

Se incorporaron las reglas de negocio reactivas (post-its lilas) que automatizan la respuesta del sistema ante eventos específicos. Entre las políticas definidas destacan la Verificación de datos válidos tras el inicio de sesión, la validación del Seguro vigente al realizar el pago, y la automatización de alertas cuando se superan los umbrales de humedad o nutrientes en el historial de campo.

![event storming](assets/chapter-04/step6.png){width=500px}

**Step 7: Read Models**

Se mapearon los Read Models (post-its verdes), que representan las vistas e interfaces de datos necesarias para que los actores tomen decisiones informadas. Entre los modelos de lectura clave se encuentran la Lista de planes disponibles, la Búsqueda de usuarios, el Estado del sensor en tiempo real y el Dashboard de indicadores del campo, los cuales permiten al agricultor visualizar la información crítica antes de ejecutar cualquier comando de gestión o riego.

![event storming](assets/chapter-04/step7.png){width=500px}

**Step 8: External Systems**

Se identificaron los sistemas externos (post-its rosados rectangulares) que interactúan con CultivaTech para completar el flujo de procesos. Entre ellos destacan el Sistema de métodos de pago para procesar las suscripciones de los usuarios y el Sistema de mapas (como Google Maps o Mapbox), indispensable para la geolocalización de las zonas de cultivo y la visualización de los indicadores sobre el terreno.

![event storming](assets/chapter-04/step8.png){width=500px}

**Step 9: Aggregates**

Se incrementó el nivel de abstracción agrupando los comandos, eventos y reglas de negocio alrededor de las entidades principales del dominio (Aggregates, representados en post-its amarillos grandes). Para CultivaTech, se definieron agregados clave como Usuario, Plan de Suscripción, Notificaciones, Zona, IoT y Report, los cuales encapsulan la lógica y aseguran la consistencia del estado del sistema en cada etapa del monitoreo agrícola.

![event storming](assets/chapter-04/step9.png){width=500px}

**Step 10: Bounded Contexts**

Finalmente, se delimitaron los límites semánticos y transaccionales del dominio mediante la definición de Bounded Contexts, agrupando los agregados y procesos relacionados en bloques independientes. Para CultivaTech, la arquitectura se consolidó en tres contextos principales: IAM (Identity and Access Management) para la gestión de usuarios y seguridad, Payment para el control de planes y facturación, y Monitoring para el núcleo del negocio que abarca el control de zonas, dispositivos IoT, historial de campo y proyecciones agrícolas.

![event storming](assets/chapter-04/step10.png){width=500px}

## 4.6.2. Software Architecture Context Diagram.

```plantuml
@startuml
!include <C4/C4_Context.puml>

' ==================== LIGHT THEME CONFIGURATION ====================
skinparam backgroundColor #FFFFFF
skinparam defaultFontColor #333333
skinparam classFontColor #1A1A1A
skinparam class {
    BackgroundColor #F8F9FA
    BorderColor #DEE2E6
    HeaderBackgroundColor #E9ECEF
    HeaderFontColor #0066CC
    FontColor #1A1A1A
}

title <color:#0066CC><size:18>AgroTech IoT - System Context Diagram</size></color>

' ==================== PERSONS ====================
Person(farmer, "Farmer", "Main user who monitors their crops and manages their farm")
Person(admin, "Administrator", "Manages products, orders, and oversees the system")

' ==================== MAIN SYSTEM ====================
System(agrotech, "AgroTech IoT Platform", "Smart crop monitoring and e-commerce platform")

' ==================== EXTERNAL SYSTEMS ====================
System_Ext(weatherApi, "Weather API", "Provides real-time weather data and forecasts")
System_Ext(satelliteApi, "Satellite API", "Provides satellite imagery for crop health analysis")
System_Ext(recommendationEngine, "Recommendation Engine", "Generates AI-based irrigation recommendations")
System_Ext(paymentGateway, "Payment Gateway", "Processes payments for orders and subscriptions")
System_Ext(emailService, "Email Service", "Sends email notifications and alerts")

' ==================== RELATIONSHIPS ====================
Rel(farmer, agrotech, "Monitors crops, receives alerts, purchases products", "HTTPS/REST API")
Rel(admin, agrotech, "Manages products, oversees orders and users", "HTTPS/REST API")

Rel(agrotech, weatherApi, "Fetches weather forecast data", "HTTPS/REST API")
Rel(agrotech, satelliteApi, "Fetches satellite images", "HTTPS/REST API")
Rel(agrotech, recommendationEngine, "Sends sensor data and receives recommendations", "Webhook/REST API")
Rel(agrotech, paymentGateway, "Processes payments for orders", "HTTPS/REST API")
Rel(agrotech, emailService, "Sends email notifications", "SMTP/HTTP")

@enduml
```

## 4.6.3. Software Architecture Container Diagrams.

```plantuml
@startuml
!include <C4/C4_Container.puml>

' ==================== LIGHT THEME CONFIGURATION ====================
skinparam backgroundColor #FFFFFF
skinparam defaultFontColor #333333
skinparam classFontColor #1A1A1A
skinparam class {
    BackgroundColor #F8F9FA
    BorderColor #DEE2E6
    HeaderBackgroundColor #E9ECEF
    HeaderFontColor #0066CC
    FontColor #1A1A1A
}

title <color:#0066CC><size:18>AgroTech IoT - Container Diagram</size></color>

' ==================== PERSONS ====================
Person(farmer, "Farmer", "Main user who monitors their crops")
Person(admin, "Administrator", "Manages products and oversees the system")

' ==================== CONTAINERS ====================
Container(webApp, "Web Application", "Vue 3 / Vite", "Web interface for farmers and administrators")
Container(mobileApp, "Mobile Application", "Flutter / Dart", "Mobile app for field monitoring")
Container(apiGateway, "API Gateway", ".NET 10 / YARP", "Single entry point, authentication and routing")

Container_Boundary(backend, "Backend Services (Microservices)") {
    Container(iamService, "IAM Service", ".NET 10", "Authentication, authorization and user management")
    Container(profileService, "Profile Service", ".NET 10", "Farmer profile management")
    Container(commercialService, "Commercial Service", ".NET 10", "Product and order management")
    Container(monitoringService, "Monitoring Service", ".NET 10", "Field and monitoring data management")
    Container(stockService, "Stock Service", ".NET 10", "Inventory control")
    Container(notificationService, "Notification Service", ".NET 10", "Notification delivery")
    Container(communityService, "Community Service", ".NET 10", "Community profiles and comments management")
    Container(analyticsService, "Analytics Service", ".NET 10", "Report generation and data analysis")
}

ContainerDb(mysqlDb, "MySQL Database", "MySQL 8.0", "Main system database")

' ==================== EXTERNAL SYSTEMS ====================
System_Ext(weatherApi, "Weather API", "Provides weather data")
System_Ext(satelliteApi, "Satellite API", "Provides satellite imagery")
System_Ext(paymentGateway, "Payment Gateway", "Processes payments")

' ==================== RELATIONSHIPS ====================
Rel(farmer, webApp, "Uses", "HTTPS")
Rel(farmer, mobileApp, "Uses", "HTTPS")
Rel(admin, webApp, "Uses", "HTTPS")

Rel(webApp, apiGateway, "Consumes API", "HTTPS/REST")
Rel(mobileApp, apiGateway, "Consumes API", "HTTPS/REST")

Rel(apiGateway, iamService, "Routes to", "HTTP")
Rel(apiGateway, profileService, "Routes to", "HTTP")
Rel(apiGateway, commercialService, "Routes to", "HTTP")
Rel(apiGateway, monitoringService, "Routes to", "HTTP")
Rel(apiGateway, stockService, "Routes to", "HTTP")
Rel(apiGateway, notificationService, "Routes to", "HTTP")
Rel(apiGateway, communityService, "Routes to", "HTTP")
Rel(apiGateway, analyticsService, "Routes to", "HTTP")

Rel(iamService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(profileService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(commercialService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(monitoringService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(stockService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(notificationService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(communityService, mysqlDb, "Reads/Writes", "EF Core/MySQL")
Rel(analyticsService, mysqlDb, "Reads/Writes", "EF Core/MySQL")

Rel(monitoringService, weatherApi, "Queries", "REST API")
Rel(monitoringService, satelliteApi, "Queries", "REST API")
Rel(commercialService, paymentGateway, "Processes payment", "REST API")

@enduml
```

## 4.6.4. Software Architecture Components Diagrams.

```plantuml
@startuml
!include <C4/C4_Component.puml>

' ==================== CONFIGURACIÓN ====================
skinparam backgroundColor #FFFFFF
skinparam defaultFontColor #333333
skinparam classFontColor #1A1A1A
skinparam class {
    BackgroundColor #F8F9FA
    BorderColor #DEE2E6
    HeaderBackgroundColor #E9ECEF
    HeaderFontColor #0066CC
    FontColor #1A1A1A
}

skinparam componentStyle rectangle
skinparam rectangle {
    BackgroundColor #F8F9FA
    BorderColor #DEE2E6
    FontColor #0066CC
}

title <color:#0066CC><size:18>AgroTech IoT - Components Diagram (Part 1: Business Services)</size></color>

' ==================== SERVICIOS DE NEGOCIO ====================
Container_Boundary(backend, "Backend Services") {
    
    Container_Boundary(iam, "IAM Service") {
        Component(iamApi, "REST API", "ASP.NET Core", "AuthenticationController, UsersController")
        Component(userCommand, "UserCommandService", ".NET Service", "Handles SignIn and SignUp commands")
        Component(userQuery, "UserQueryService", ".NET Service", "Handles user queries")
        Component(facade, "IamContextFacade", ".NET Service", "ACL Facade for other contexts")
        Component(tokenService, "TokenService", "JWT Service", "Generates and validates JWT tokens")
        Component(hashingService, "HashingService", "BCrypt Service", "Hashes and verifies passwords")
        Component(userRepository, "UserRepository", "EF Core", "User data access")
    }
    
    Container_Boundary(profile, "Profile Service") {
        Component(profileApi, "REST API", "ASP.NET Core", "ProfilesController")
        Component(profileCommand, "ProfileCommandService", ".NET Service", "Handles profile commands")
        Component(profileQuery, "ProfileQueryService", ".NET Service", "Handles profile queries")
        Component(profileRepository, "ProfileRepository", "EF Core", "Profile data access")
    }
    
    Container_Boundary(commercial, "Commercial Service") {
        Component(commercialApi, "REST API", "ASP.NET Core", "OrdersController, ProductsController")
        Component(orderService, "OrderService", ".NET Service", "Order management")
        Component(productService, "ProductService", ".NET Service", "Product management")
        Component(orderRepository, "OrderRepository", "EF Core", "Order data access")
        Component(productRepository, "ProductRepository", "EF Core", "Product data access")
    }
    
    Container_Boundary(monitoring, "Monitoring Service") {
        Component(monitoringApi, "REST API", "ASP.NET Core", "FieldsController, DevicesController")
        Component(fieldCommand, "FieldCommandService", ".NET Service", "Handles field commands")
        Component(fieldQuery, "FieldQueryService", ".NET Service", "Handles field queries")
        Component(deviceCommand, "DeviceCommandService", ".NET Service", "Handles device commands")
        Component(deviceQuery, "DeviceQueryService", ".NET Service", "Handles device queries")
        Component(fieldRepository, "FieldRepository", "EF Core", "Field data access")
        Component(deviceRepository, "DeviceRepository", "EF Core", "Device data access")
    }
}

' ==================== BASE DE DATOS ====================
ContainerDb(mysqlDb, "MySQL Database", "MySQL 8.0", "Main system database")

' ==================== EXTERNOS ====================
System_Ext(client, "Client", "Web/Mobile Frontend")
System_Ext(weatherApi, "Weather API", "External service")
System_Ext(satelliteApi, "Satellite API", "External service")
System_Ext(paymentGateway, "Payment Gateway", "External service")

' ==================== RELACIONES - CLIENTES ====================
Rel(client, iamApi, "Authenticates", "HTTPS/REST")
Rel(client, profileApi, "Manages profile", "HTTPS/REST")
Rel(client, commercialApi, "Manages orders and products", "HTTPS/REST")
Rel(client, monitoringApi, "Manages fields and devices", "HTTPS/REST")

' ==================== RELACIONES - IAM ====================
Rel(iamApi, userCommand, "Delegates to", "Internal")
Rel(iamApi, userQuery, "Delegates to", "Internal")
Rel(facade, userCommand, "Uses", "Internal")
Rel(facade, userQuery, "Uses", "Internal")
Rel(userCommand, hashingService, "Uses", "Internal")
Rel(userCommand, tokenService, "Uses", "Internal")
Rel(userCommand, userRepository, "Uses", "Internal")
Rel(userQuery, userRepository, "Uses", "Internal")

' ==================== RELACIONES - PROFILE ====================
Rel(profileApi, profileCommand, "Delegates to", "Internal")
Rel(profileApi, profileQuery, "Delegates to", "Internal")
Rel(profileCommand, profileRepository, "Uses", "Internal")
Rel(profileQuery, profileRepository, "Uses", "Internal")

' ==================== RELACIONES - COMMERCIAL ====================
Rel(commercialApi, orderService, "Delegates to", "Internal")
Rel(commercialApi, productService, "Delegates to", "Internal")
Rel(orderService, orderRepository, "Uses", "Internal")
Rel(orderService, productRepository, "Uses", "Internal")
Rel(productService, productRepository, "Uses", "Internal")
Rel(orderService, paymentGateway, "Processes payment", "REST API")

' ==================== RELACIONES - MONITORING ====================
Rel(monitoringApi, fieldCommand, "Delegates to", "Internal")
Rel(monitoringApi, fieldQuery, "Delegates to", "Internal")
Rel(monitoringApi, deviceCommand, "Delegates to", "Internal")
Rel(monitoringApi, deviceQuery, "Delegates to", "Internal")
Rel(fieldCommand, fieldRepository, "Uses", "Internal")
Rel(fieldQuery, fieldRepository, "Uses", "Internal")
Rel(deviceCommand, deviceRepository, "Uses", "Internal")
Rel(deviceQuery, deviceRepository, "Uses", "Internal")
Rel(fieldCommand, weatherApi, "Gets weather data", "REST API")
Rel(fieldCommand, satelliteApi, "Gets satellite images", "REST API")

' ==================== RELACIONES - BASE DE DATOS ====================
Rel(userRepository, mysqlDb, "Reads/Writes", "EF Core")
Rel(profileRepository, mysqlDb, "Reads/Writes", "EF Core")
Rel(orderRepository, mysqlDb, "Reads/Writes", "EF Core")
Rel(productRepository, mysqlDb, "Reads/Writes", "EF Core")
Rel(fieldRepository, mysqlDb, "Reads/Writes", "EF Core")
Rel(deviceRepository, mysqlDb, "Reads/Writes", "EF Core")

@enduml
```