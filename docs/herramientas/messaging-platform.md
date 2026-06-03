# Cimiento de Comunicación: Messaging Platform

Enlace al proyecto: https://github.com/DamianGonzalez27/MessagingCluster

Messaging Platform es una solución de infraestructura y topología de red distribuida, empaquetada como Infraestructura como Código (IaC), desarrollada para proveer un entorno híbrido de mensajería y transmisión de eventos de alta disponibilidad. El proyecto surge como respuesta a un desafío crítico en plataformas modernas: el acoplamiento directo y síncrono entre microservicios, lo que genera sistemas rígidos frente a fallos de red, cuellos de botella en bases de datos y una alta complejidad operativa para escalar componentes de manera independiente.

En lugar de permitir que cada servicio web implemente configuraciones locales de mensajería o adopte de forma ciega una única herramienta para resolver problemas de distinta naturaleza, concebí este proyecto como un cimiento perimetral de comunicación de autoservicio. Su objetivo principal es abstraer el aprovisionamiento de los esquemas de red y persistencia distribuidos, aislando el tráfico de eventos dentro de una cuenta satélite dedicada (Spoke Account) para minimizar radicalmente el radio de impacto (blast radius) de la organización.

## El Problema de Negocio y Operación
Cuando los servicios de una organización dependen de llamadas síncronas HTTP mutuas para completar una transacción, la caída de un solo componente secundario provoca un colapso en cadena de toda la plataforma (Efecto Dominó). Asimismo, intentar forzar una sola tecnología de mensajería para resolver tanto la entrega de tareas transaccionales exactas como la ingesta masiva de telemetría a alta velocidad eleva los costos operativos, genera pérdida de mensajes y satura la capacidad de cómputo del sistema.

## La Solución de Ingeniería
Messaging Platform resuelve esta fricción mediante el aprovisionamiento orquestado de un ecosistema híbrido y sinérgico que combina las ventajas de un Message Broker tradicional con un Distributed Commit Log. Al empaquetar esta topología mediante arquitecturas de contenedores y volúmenes aislados, la plataforma habilita de forma nativa el desacoplamiento temporal, sistemas de comunicación coreográficos y pipelines de datos resilientes, listos para ser consumidos por las APIs síncronas y los componentes del Async Framework.

## Capacidades Principales del Componente
Diseñada bajo principios de segregación estricta de casos de uso, alta persistencia y seguridad perimetral, la plataforma provee de forma nativa:

Coexistencia Híbrida Inteligente: Integración dirigida de RabbitMQ para mensajería transaccional de alta fidelidad (enrutamientos complejos y garantías de entrega mediante AMQP) junto con Apache Kafka para streaming masivo de eventos e ingesta inmutable a ultra-baja latencia.

Modernización Operativa mediante Kafka KRaft: Configuración avanzada que elimina por completo la dependencia externa de Zookeeper para la gestión de metadatos de Kafka, consolidando el gobierno del clúster de forma nativa en los brokers para acelerar los tiempos de recuperación ante fallos de nodos.

Garantía de Persistencia e Inmutabilidad de Datos: Implementación de políticas de almacenamiento mediante volúmenes nombrados independientes (Named Volumes), asegurando la continuidad de los estados del clúster y las colas de mensajes ante reinicios o actualizaciones de la infraestructura.

Seguridad Perimetral y Principio de Mínimo Privilegio: Mitigación automatizada de riesgos de acceso mediante la parametrización dinámica de credenciales administrativas y el aislamiento estricto de redes virtuales (Docker Networks), impidiendo la exposición innecesaria de los puertos de datos hacia zonas públicas de la red.

## Filosofía de Diseño y "Golden Paths"
Concibo Messaging Platform como la infraestructura neurálgica que transforma un conjunto de microservicios aislados en un verdadero ecosistema distribuido y resiliente. Su diseño materializa mi filosofía de ingeniería: la infraestructura debe ser tratada como un producto consumible que reduzca la fricción técnica de los equipos de desarrollo. Al proveer este "Camino Seguro" (Golden Path) empaquetado y listo para producción, las células de software pueden implementar patrones asíncronos complejos o arquitecturas orientadas a eventos (EDA) de forma inmediata, sabiendo que la red subyacente ya cuenta con los estándares corporativos de alta disponibilidad, persistencia de datos y seguridad exigidos por el negocio.

## Roadmap y Evolución Técnica
El proyecto ha sido estructurado para transicionar hacia una plataforma de mensajería distribuida totalmente elástica y automatizada en la nube a través de los siguientes hitos técnicos:

Migración Hacia Declaraciones Terraform / CloudFormation: Evolución del empaquetamiento actual basado en Docker Compose hacia manifiestos de Infraestructura como Código (IaC) empresariales para el aprovisionamiento automatizado del clúster sobre servicios nativos de AWS (como Amazon MSK y Amazon MQ).

Monitoreo y Observabilidad de Clúster Integrada: Incorporación de agentes de telemetría dedicados (como Prometheus Exporters) para capturar en tiempo real métricas críticas de infraestructura, incluyendo tasas de entrada/salida de mensajes, lag de los consumidores y saturación de disco.

Automatización de Tópicos y Esquemas mediante GitOps: Desarrollo de pipelines que permitan a los desarrolladores declarar nuevos tópicos de Kafka o colas de RabbitMQ directamente mediante archivos de configuración en sus repositorios de código, automatizando su creación y gobernanza en el clúster sin intervención manual del equipo de operaciones.