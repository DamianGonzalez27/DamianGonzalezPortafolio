# Ecosistema Core: Develop Toolkit
El Develop Toolkit constituye la base de software reutilizable de nuestra Plataforma Interna de Desarrollo (IDP). En lugar de permitir que cada microservicio o célula de ingeniería resuelva de forma aislada e inconsistente la telemetría o la gestión de fallos, este conjunto de librerías nativas automatiza y estandariza las políticas de gobernanza técnica directamente en el código de la aplicación.

Su integración inyecta capacidades avanzadas de grado empresarial con cero fricción, reduciendo drásticamente la carga cognitiva de los equipos de desarrollo.

---

## Proyecto de Plataforma: Logger Tracker (Librería PyPI)

- [Enlace a Github](https://github.com/DamianGonzalez27/FrameworkObservabilidad)
- [Enlace a PyPi](https://pypi.org/project/logger-tracker/)

Logger Tracker es una librería de infraestructura desarrollada en Python para estandarizar la observabilidad operacional de servicios backend dentro de ecosistemas distribuidos y entornos altamente concurrentes o asíncronos. El proyecto surge como respuesta a un desafío crítico en plataformas modernas: la inconsistencia en la generación de telemetría y la alta complejidad para correlacionar eventos durante la operación diaria de sistemas distribuidos.

En lugar de abordar la observabilidad como una configuración aislada por proyecto, concebí esta herramienta como una capa reutilizable de gobernanza técnica. Su objetivo principal es permitir a múltiples células de desarrollo incorporar capacidades de rastreo homogéneas, predecibles y sin fricción operativa, reduciendo drásticamente el boilerplate code asociado a la instrumentación manual.

### El Problema de Negocio y Operación
En sistemas distribuidos o aplicaciones concurrentes, un único flujo transaccional puede fragmentarse en múltiples hilos o corrutinas, dispersando los registros de ejecución. Ante un incidente en producción, reconstruir la línea de tiempo de una petición se vuelve una tarea compleja que incrementa el Tiempo Medio de Recuperación (MTTR) debido a la falta de un contexto unificado.

### La Solución de Ingeniería
Logger Tracker resuelve esta fricción mediante la implementación de mecanismos de correlación contextual automática. A través de identificadores únicos inyectados en el contexto de ejecución, la librería permite enlazar cada log generado con una transacción específica, facilitando de forma inmediata el diagnóstico de incidentes, el debugging distribuido y el análisis del comportamiento del sistema bajo carga.

### Capacidades Principales del Componente
Diseñada bajo principios de simplicidad operativa, adopción incremental y alta eficiencia, la librería provee de forma nativa:

Gobernanza de Logs Centralizada: Estandarización de formatos de salida para múltiples tipos de cargas de trabajo (APIs, Workers, procesos batch), asegurando homogeneidad en todo el ecosistema Python.

Rastreo Contextual Concurrente: Correlación de eventos mediante identificadores únicos inyectados de forma segura en el flujo de ejecución (hilos y contextos asíncronos), aislando el comportamiento de cada petición en entornos saturados.

Configuración Agnóstica y Dinámica: Inicialización simplificada e instrumentación transparente basada en variables de entorno, facilitando su integración en arquitecturas nativas de la nube (Cloud-Native).

Optimización de la Experiencia de Desarrollo (DevEx): Abstracción completa de patrones repetitivos de observabilidad, permitiendo a los desarrolladores contar con telemetría avanzada desde el primer día sin necesidad de reescribir manejadores o formateadores manuales.

### Filosofía de Diseño y "Golden Paths"
Concibo Logger Tracker como un activo estratégico de Ingeniería de Plataforma orientado a disminuir la carga cognitiva de los equipos. Su diseño materializa mi filosofía de ingeniería: anteponer plataformas habilitadoras sobre soluciones aisladas y tratar la observabilidad como una capacidad nativa del ciclo de vida del software. Al proveer un "Camino Seguro" (Golden Path), los equipos de desarrollo pueden concentrarse enteramente en la lógica de negocio, sabiendo que la infraestructura de código hereda de forma automática los estándares de seguridad, trazabilidad y resiliencia de la organización.

### Roadmap y Evolución Técnica
El proyecto ha sido estructurado para evolucionar hacia un estándar de observabilidad moderna y distribuida de manera progresiva a través de los siguientes hitos técnicos:

Structured Logging Dinámico: Transición completa hacia formatos estructurados nativos (JSON logs) optimizados para su ingesta y análisis en tiempo real por procesadores de logs (Log Forwarders).

Alineación con OpenTelemetry (OTel): Incorporación de soporte nativo para la propagación distribuida de contextos mediante Trace y Span IDs bajo estándares del W3C.

Instrumentación Automatizada para Microservicios: Desarrollo de middlewares integrados para frameworks populares de Python (FastAPI, Flask) y consumidores de eventos asíncronos para capturar e inyectar telemetría de forma transparente en las fronteras de la red.

## Proyecto de Plataforma: Global Handler (Librería PyPI)

- [Enlace a GitHub](https://github.com/DamianGonzalez27/GlobalHandler)
- [Enlace a PyPi](https://pypi.org/project/global-handler/)

Global Handler es una librería de infraestructura desarrollada en Python para centralizar, unificar y gobernar la gestión de fallos en la frontera más externa de servicios y APIs distribuidas. El proyecto surge como respuesta a un desafío crítico en plataformas modernas: la dispersión y heterogeneidad en el manejo de excepciones de software, lo que genera respuestas inconsistentes hacia los clientes y eleva el riesgo de seguridad operativa en entornos de producción.

En lugar de abordar el manejo de errores mediante bloques repetitivos y manuales en cada controlador o caso de uso, concebí esta herramienta como una barrera perimetral de resiliencia reutilizable. Su objetivo principal es actuar como un interceptor agnóstico capaz de estandarizar los contratos de salida, mitigar riesgos de seguridad y clasificar fallos de forma automática, reduciendo drásticamente el boilerplate code asociado a la contención manual de excepciones.

### El Problema de Negocio y Operación
En arquitecturas distribuidas, la falta de una estrategia unificada para la gestión de errores provoca que fallos inesperados del sistema expongan stack traces crudos, variables internas o credenciales hacia clientes externos (Information Leakage). Este comportamiento no solo viola normativas de seguridad (OWASP), sino que rompe los contratos de interfaz de las APIs y fragmenta el flujo de diagnóstico, forzando a los ingenieros de soporte a descifrar errores heterogéneos bajo escenarios de alta presión.

### La Solución de Ingeniería
Global Handler resuelve esta fricción mediante la implementación de un mecanismo centralizado de intercepción perimetral y traducción dinámica de excepciones. A través de un desacoplamiento estricto, la librería captura cualquier fallo del sistema en las fronteras de la red, sanitiza el payload de salida hacia el exterior con mensajes seguros y estandarizados, y resguarda de forma íntegra el contexto técnico real para el consumo exclusivo de las herramientas de telemetría y auditoría interna.

### Capacidades Principales del Componente
Diseñada bajo principios de robustez defensiva, tipificación estricta y alta interoperabilidad, la librería provee de forma nativa:

Mapeo Dinámico de Excepciones de Dominio: Capacidad de registrar correspondencias directas entre excepciones semánticas de negocio (DDD) y códigos de estado del protocolo de entrega, manteniendo la lógica core limpia de conceptos de transporte (HTTP).

Gobernanza de Seguridad (OWASP Sanitize): Mitigación automatizada del riesgo de fuga de información en entornos de producción, reemplazando logs técnicos crudos por tokens de error y respuestas predecibles para el cliente externo.

Estandarización de Contratos de Interfaz: Garantía absoluta de que toda anomalía del sistema (errores de validación, recursos no encontrados o colapsos de servidor) responda bajo una estructura JSON idéntica y tipificada para los consumidores del ecosistema.

Optimización de la Experiencia de Desarrollo (DevEx): Abstracción completa de patrones repetitivos de captura de errores (try/except), permitiendo a los desarrolladores programar enfocados exclusivamente en el "camino feliz" de la lógica de negocio.

### Filosofía de Diseño y "Golden Paths"
Concibo Global Handler como un activo estratégico de Ingeniería de Plataforma orientado a disminuir la carga cognitiva de los equipos de desarrollo al momento de diseñar software tolerante a fallos. Su diseño materializa mi filosofía de ingeniería: anteponer componentes de infraestructura reutilizables que blinden el comportamiento perimetral del ecosistema de manera transparente. Al proveer un "Camino Seguro" (Golden Path), las células de desarrollo delegan la responsabilidad de la resiliencia y la seguridad del contrato al framework, asegurando que cada nuevo servicio web o asíncrono herede por defecto las políticas de cumplimiento corporativo.

### Roadmap y Evolución Técnica
El proyecto ha sido estructurado para evolucionar hacia un estándar de resiliencia moderno y distribuido de manera progresiva a través de los siguientes hitos técnicos:

Evolución a Middlewares Nativos Asíncronos: Transición del modelo de decoradores funcionales hacia middlewares oficiales y asíncronos con soporte nativo para los ciclos de eventos de FastAPI y Flask Asíncrono.

Sinergia Automatizada de Telemetría: Integración profunda con el ecosistema logger-tracker para correlacionar e inyectar de forma automática el Correlation ID activo dentro del log estructurado de la excepción interceptada.

Políticas de Reintentos y DLQ para Arquitecturas EDA: Expansión de las capacidades del handler hacia entornos orientados a eventos, actuando sobre consumidores del Async Framework para gestionar estrategias de Exponential Backoff y enrutamiento automatizado a colas de descarte (Dead Letter Queues).