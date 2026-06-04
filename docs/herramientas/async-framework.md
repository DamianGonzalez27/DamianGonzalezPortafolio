# Proyecto de Plataforma: Async Framework (Scaffolding Asíncrono)

[Enlace al proyecto](https://github.com/DamianGonzalez27/AsyncFramework)

Async Framework es una arquitectura de referencia y plantilla de andamiaje (scaffolding) desarrollada en Python para estandarizar la creación de Workers, demonios de fondo y consumidores de eventos de alto rendimiento dentro de ecosistemas distribuidos. El proyecto surge como respuesta a un desafío crítico en plataformas modernas: el acoplamiento y la degradación de rendimiento que sufren las APIs síncronas al procesar tareas pesadas o ejecuciones por lotes dentro del ciclo de vida tradicional de una solicitud HTTP.

En lugar de obligar a los equipos de desarrollo a configurar manualmente bucles de eventos complejos o conectores de red para cada demonio secundario, concebí esta herramienta como una base sólida de gobernanza operativa. Su objetivo principal es abstraer la complejidad de la concurrencia no bloqueante y la integración con brokers de mensajería, asegurando que el plano de ejecución en segundo plano de la organización sea predecible, resiliente y nativamente compatible con nuestro Develop Toolkit.

## El Problema de Negocio y Operación
Cuando una organización procesa tareas intensivas en cómputo o integraciones con servicios externos lentos de forma síncrona, se bloquean los hilos de ejecución de las APIs principales, incrementando los tiempos de respuesta y provocando caídas en cascada bajo escenarios de alta demanda. Al intentar mover estos flujos a procesos en segundo plano sin un estándar formal, se pierde la trazabilidad de las transacciones (puntos ciegos de observabilidad) y se eleva el riesgo de pérdida o duplicidad de mensajes ante fallos de infraestructura.

## La Solución de Ingeniería
Async Framework resuelve esta fricción proveyendo un entorno de ejecución desacoplado temporalmente y basado en bucles de eventos eficientes. Al actuar como el motor que procesa las colas y tópicos del ecosistema de forma independiente, el framework encapsula las políticas de reintentos distribuidos, la gestión de la concurrencia y la persistencia asíncrona, permitiendo que las APIs web deleguen el trabajo pesado instantáneamente y permanezcan ligeras, reactivas y altamente disponibles.

## Capacidades Principales del Componente
Diseñada bajo principios de alta eficiencia de recursos, tolerancia a fallos autónoma y optimización de la experiencia de desarrollo, la plantilla provee de forma nativa:

Concurrencia No Bloqueante Avanzada (asyncio): Núcleo estructurado en torno al ciclo de eventos nativo de Python, permitiendo una gestión masiva de operaciones de Entrada/Salida (E/S) con una huella de memoria mínima por contenedor.

Trazabilidad Distribuida Context-Aware: Middleware interceptor encargado de extraer el Correlation ID desde las cabeceras de los mensajes entrantes del clúster de mensajería, sincronizándolo automáticamente con logger-tracker para erradicar los puntos ciegos operacionales.

Mecanismo de Resiliencia y Manejo de DLQ: Integración nativa con global-handler para capturar fallos de ejecución, aplicando reintentos exponenciales aleatorizados (Exponential Backoff with Jitter) y enrutando los mensajes corruptos hacia colas de descarte (Dead Letter Queues) para evitar bloqueos del clúster.

Ciclo de Vida Sensible a la Infraestructura (Graceful Shutdown): Capacidad de interceptar señales del sistema operativo (SIGTERM/SIGINT), permitiendo al Worker detener la ingesta, finalizar el procesamiento del mensaje en curso y cerrar de forma segura las conexiones a bases de datos antes de apagarse, garantizando la consistencia transaccional absoluta.

## Filosofía de Diseño y "Golden Paths"
Concibo Async Framework como un componente de infraestructura indispensable para habilitar Arquitecturas Orientadas a Eventos (EDA) de grado empresarial de forma simplificada. Su diseño materializa mi filosofía de ingeniería: tratar el desacoplamiento temporal no como una configuración artesanal, sino como una capacidad arquitectónica gobernada y transparente para el desarrollador. Al proveer este "Camino Seguro" (Golden Path), los ingenieros de software pueden orquestar coreografías complejas y procesamiento asíncrono masivo con la certeza de que la infraestructura subyacente autosana sus conexiones, protege los datos ante caídas de red y mantiene los estándares de auditoría de la organización de extremo a extremo.

## Roadmap y Evolución Técnica
El proyecto ha sido diseñado para evolucionar hacia un framework híbrido y elástico de procesamiento asíncrono a través de los siguientes hitos técnicos:

Abstracción Agnóstica de Drivers de Mensajería: Desarrollo de una capa de transporte genérica que permita alternar de forma transparente entre colas de RabbitMQ (AMQP) y tópicos de Apache Kafka a nivel de configuración, reutilizando la misma lógica de negocio del Worker.

Métricas de Consumo Nativas (Prometheus Integration): Incorporación de exportadores automatizados de telemetría para reportar en tiempo real métricas críticas de los Workers, tales como latencia de procesamiento, tasa de errores por mensaje y tiempos de ciclo.

Escalado Autosuficiente basado en Carga (KEDA Alignment): Optimización de los ciclos de vida de los contenedores del framework para interactuar de forma nativa con escaladores automáticos controlados por eventos en la nube, permitiendo instanciar o destruir nodos de ejecución de acuerdo al volumen de mensajes represados en el clúster.