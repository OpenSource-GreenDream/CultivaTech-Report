# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competitor Analysis

Para la solución CultivaTech desarrollada por GreenDream, se ha realizado un análisis comparativo frente a los principales competidores en el sector de la Agricultura 4.0 a nivel nacional e internacional.

### 2.1.1. Análisis competitivo

A continuación, se presenta la matriz de análisis comparativo de CultivaTech frente a las alternativas existentes en el mercado:

| Criterio / Característica | CultivaTech (Nuestra Solución) | Libelium (Smart Agriculture) | CropX | Kilimo |
| :--- | :--- | :--- | :--- | :--- |
| **Tipo de Competidor** | — | Directo (Internacional) | Directo (Internacional) | Indirecto (Regional) |
| **Público Objetivo** | Pequeños y medianos agricultores andinos (1-20 ha). | Agroindustria de gran escala e investigación. | Medianos y grandes productores agrícolas. | Medianos/Grandes agricultores con sistemas de riego. |
| **Tecnología IoT** | Sensores de suelo de bajo costo (< S/ 300) con LoRaWAN. | Sensores modulares de grado industrial (Plug & Sense). | Nodos integrados con transmisión satelital/celular. | Sin hardware propio (usa datos satelitales/clima). |
| **Experiencia de Usuario (UX)** | Basada en íconos, interfaz tipo semáforo y alertas sonoras. | Dashboards técnicos para ingenieros agrónomos. | Aplicación móvil gráfica enfocada en riego. | Plataforma web y móvil de gestión de riego. |
| **Costo Aprox. de Implementación** | Accesible (< S/ 500 inicial por hectárea). | Muy alto (> S/ 5,000 por hectárea). | Alto (> S/ 3,500 por hectárea). | Suscripción de software (S/ 1,200/año aprox). |
| **Dependencia de Conectividad** | Red LoRaWAN (Funciona sin cobertura celular 4G). | Celular 4G / Wi-Fi / LoRa. | Celular 4G / Satelital. | Requiere internet móvil constante. |
| **Análisis Predictivo** | Predicción de siembra y rendimiento por cosechas previas. | Telemetría en tiempo real sin enfoque predictivo directo. | Recomendaciones automáticas de riego. | Recomendaciones de balance hídrico. |

### 2.1.2. Estrategias y tácticas frente a competidores

Con el fin de posicionar a CultivaTech de manera competitiva y lograr la adopción en el sector agrícola peruano, se establecen las siguientes estrategias y tácticas:

* **Estrategia de Liderazgo en Costos e Inclusión Digital:**
    * **Táctica:** Desarrollo de nodos IoT propios utilizando componentes de bajo costo con certificación IP67 y autonomía solar, reduciendo el precio de entrada a menos de S/ 300 por sensor frente a los S/ 3,500+ de competidores internacionales.
* **Estrategia de Accesibilidad en Conectividad Rural:**
    * **Táctica:** Implementación de arquitectura de red basada en **LoRaWAN**, permitiendo la transmisión de datos a larga distancia en zonas sin cobertura celular 4G (superando la barrera del 90% de desconexión en campos andinos).
* **Estrategia de Diseño Inclusivo (UX Adaptativa):**
    * **Táctica:** Sustitución de dashboards complejos cargados de gráficos densos por una interfaz móvil simplificada basada en íconos visuales, códigos de colores tipo semáforo (verde/amarillo/rojo) y alertas sonoras adaptadas a usuarios con baja alfabetización digital.
* **Estrategia de Diferenciación por Valor Agregado:**
    * **Táctica:** Integración de algoritmos de análisis predictivo basados en el historial de cosechas para estimar rendimientos futuros, transformando la simple telemetría de suelo en decisiones operativas directas de siembra, riego y fertilización.