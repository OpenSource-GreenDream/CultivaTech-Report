# Conclusiones

## Conclusiones

- Resolución de la problemática del sector agrícola rural: Se validó 
que el principal problema de los pequeños y medianos agricultores 
andinos es la incertidumbre climática y el deterioro del suelo 
(hasta un 45% de degradación en la región). La propuesta de valor de 
CultivaTech aborda directamente esta brecha mediante sensores IoT de 
bajo costo (< S/300) y redes LoRaWAN, permitiendo el monitoreo técnico
en zonas con baja alfabetización digital y nula conectividad 4G.

- UX Adaptativa: El análisis de entrevistas confirmó un alto índice de 
analfabetismo digital y desconfianza inicial hacia la tecnología en el 
segmento de agricultores. La implementación de una interfaz basada en 
semáforos visuales (verde/amarillo/rojo), íconos simplificados y 
alertas sonoras logra mitigar esta barrera, garantizando que el usuario 
tome decisiones operativas inmediatas de riego y fertilización sin requerir 
una capacitación compleja.

- Integración del ecosistema del negocio: La plataforma no solo impacta 
al agricultor al reducir un 25% el gasto de agua y 20% en insumos, sino
que integra a los proveedores de insumos (al otorgarles evidencia técnica 
basada en datos para sus recomendaciones) y a los consumidores 
finales/compradores B2B.

- Avance en la implementación del producto: Durante el Sprint 2 se 
logró desarrollar una versión funcional del Front End de CultivaTech, 
permitiendo que los usuarios interactúen con las principales 
funcionalidades de la aplicación web. El desarrollo incorporó 
diseño responsivo, internacionalización (i18n), navegación y 
redirecciones funcionales, consolidando la transición desde los 
prototipos y diseños hacia una solución implementada.

- Integración del Front End con servicios simulados: Debido a que los 
servicios Back End aún se encuentran en desarrollo, se utilizaron Mocks
mediante JSON Server y datos simulados para representar las respuestas 
de los servicios. Esta estrategia permitió desacoplar temporalmente el 
desarrollo del Front End de la implementación del Back End y avanzar en 
la construcción y validación de las funcionalidades de la aplicación.

- Aplicación de buenas prácticas de arquitectura: El desarrollo del
Sprint 2 permitió aplicar principios de Clean Architecture y Domain-Driven Design (DDD) 
en la organización de los bounded contexts. Asimismo, se utilizaron patrones como Facade, 
Request, Response-Resource, Assembler y Store, buscando mantener una separación clara de 
responsabilidades y facilitar la futura integración con los servicios reales del Back End.

## Recomendaciones

- Completar la integración con el Back End real: En el siguiente 
sprint se recomienda reemplazar progresivamente los Mocks utilizados 
durante el desarrollo por los servicios Back End reales, verificando 
que los contratos de datos mantengan compatibilidad con las estructuras
utilizadas por el Front End.

- Mantener la separación de responsabilidades: Se recomienda conservar 
la estructura basada en Clean Architecture, DDD y los patrones 
implementados durante el Sprint 2. Esta decisión permitirá evitar 
que la lógica de negocio quede acoplada a componentes de 
infraestructura o presentación a medida que aumente la cantidad de 
funcionalidades.

- Reducir la deuda técnica identificada: Se recomienda priorizar
las tareas pendientes del Front End antes de incorporar nuevas
funcionalidades, con el objetivo de alcanzar una versión más estable
y consistente de la aplicación. El Sprint 2 deja explícitamente 
identificada esta deuda técnica para el Sprint 3.