# Ingeniería de Requerimientos Sistémicos

Entiendo el levantamiento de requerimientos como la fase más crítica del ciclo de vida del software. La mayoría de los problemas tecnológicos no nacen del código, sino de una comprensión incompleta del contexto operativo, organizacional y de negocio donde el sistema debe funcionar.

Por ello, no me limito a recopilar necesidades técnicas aisladas. Ejecuto un proceso de descubrimiento estructurado y sistémico orientado a reducir la incertidumbre, identificar riesgos tempranos y alinear la arquitectura tecnológica con las restricciones operativas, financieras, regulatorias y humanas de la organización. Mi objetivo es construir el contexto necesario para tomar decisiones arquitectónicas sostenibles.

Para garantizar predictibilidad, trazabilidad y repetibilidad, utilizo un conjunto de formatos, plantillas y diagramas estándar que he desarrollado y perfeccionado a lo largo de mi trayectoria. Este framework de análisis se compone de diez fases estratégicas:

## 1. Mapeo de Involucrados y Matriz de Interés
Identifico y clasifico a todos los actores clave del ecosistema: negocio, operaciones, seguridad, infraestructura, cumplimiento, soporte y usuarios finales. A través de artefactos estandarizados defino:

- Niveles de influencia y expectativas del negocio.
- Dependencias interdepartamentales y canales de comunicación.
- Responsabilidades operativas futuras.

Este análisis alinea la toma de decisiones técnicas con las necesidades reales de la organización y reduce fricciones entre áreas.

## 2. Modelado y Delimitación de Dominios
Aplico principios de diseño guiado por el dominio (Domain-Driven Design) para descomponer problemas complejos en subdominios claramente acotados. Defino bounded contexts y responsabilidades funcionales con el objetivo de:

- Evitar el acoplamiento innecesario entre componentes.
- Facilitar la escalabilidad organizacional y la mantenibilidad del código.
- Permitir la evolución e iteración independiente de los equipos.

Busco que la arquitectura de software refleje fielmente la operación real del negocio.

## 3. Taxonomía y Clasificación de la Información
Analizo la naturaleza de los datos que el sistema procesará, almacenará e intercambiará. Clasifico la información considerando variables críticas:

- Atributos del dato: Criticidad, sensibilidad, volumen, frecuencia, persistencia y trazabilidad.
- Impacto arquitectónico: Requisitos regulatorios de gobierno de datos, estrategias de almacenamiento, políticas de retención, seguridad, integración y observabilidad.

## 4. Auditoría del Ecosistema Tecnológico Existente
Evalúo las plataformas, infraestructura, integraciones, capacidades cloud y herramientas actuales de la organización para:

- Identificar capacidades reutilizables y evitar la duplicidad tecnológica.
- Detectar y mapear la deuda técnica preexistente.
- Comprender las restricciones operativas y asegurar la compatibilidad evolutiva.

Una arquitectura madura no ignora el legado de la organización; evoluciona sobre él de forma controlada y pragmática.

## 5. Modelado de Procesos y Dependencias Críticas
Diagramo los flujos operativos y de información de extremo a extremo (end-to-end), localizando con precisión:

- Dependencias críticas y puntos únicos de falla (SPOFs). 
- Cuellos de botella y flujos síncronos altamente sensibles.
- Riesgos de propagación de fallos en cascada.

Este análisis permite diseñar arquitecturas desacopladas, resilientes y observables desde la fase de concepción.

## 6. Evaluación de Riesgos y Brechas de Control
Realizo un análisis preventivo de riesgos técnicos, operativos y de seguridad asociados a la solución propuesta, identificando:

- Vulnerabilidades, brechas de control y riesgos de disponibilidad o escalabilidad.
- Estrategias nativas de mitigación, resiliencia, recuperación ante desastres y seguridad operativa.

La gestión del riesgo es un componente fundamental del diseño arquitectónico, nunca una actividad posterior.

# 7. Contexto Normativo y de Cumplimiento (Compliance)
Evalúo las regulaciones sectoriales, políticas internas y restricciones legales que impactan la solución. Traduzco los requerimientos normativos en capacidades técnicas concretas:

- Mecanismos de auditoría, trazabilidad y protección de datos.
- Segregación de responsabilidades (SoD) y retención segura de la información.

Este enfoque asegura la viabilidad de la solución en entornos corporativos altamente regulados.

## 8. Viabilidad Operativa y Madurez Técnica
Analizo la capacidad operativa real de los equipos que heredarán el sistema, evaluando su experiencia técnica, esquemas de ownership, madurez DevOps y flujos de respuesta ante incidentes.

Evito diseñar soluciones cuya complejidad técnica exceda la capacidad sostenible de operación del equipo. Una arquitectura técnicamente avanzada pero imposible de operar en el día a día sigue siendo una mala arquitectura.

## 9. Detección de Áreas de Oportunidad Estratégicas
El proceso de descubrimiento no solo busca resolver la necesidad inicial, sino optimizar el entorno. Analizo el ecosistema completo para proponer mejoras en:

- Automatización de procesos y optimización de costos de infraestructura.
- Modernización tecnológica, incremento de la observabilidad y simplificación organizacional.

## 10. Priorización Estratégica y Roadmap Evolutivo
Transformo los hallazgos obtenidos en iniciativas priorizadas con base en su impacto, riesgo, complejidad técnica, costo operativo y retorno esperado.

Defino hojas de ruta (roadmaps) evolutivas que permitan entregar valor de forma incremental y predecible, asumiendo la arquitectura como un proceso guiado por trade-offs conscientes y transparentes.

Filosofía Operativa: Este proceso existe para reducir la incertidumbre antes de construir. Las mejores decisiones técnicas no nacen únicamente del conocimiento tecnológico puro, sino de la comprensión profunda del contexto humano, operativo y organizacional donde el sistema debe evolucionar. Priorizo soluciones sostenibles diseñadas para resolver los desafíos actuales, preservando siempre la capacidad futura de adaptación de la organización.