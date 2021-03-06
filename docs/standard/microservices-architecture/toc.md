# [Microservicios de .NET: Arquitectura para aplicaciones .NET en contenedor](index.md)
## [Introducción a los contenedores y Docker](container-docker-introduction/index.md)
### [¿Qué es Docker?](container-docker-introduction/docker-defined.md)
### [Terminología de Docker](container-docker-introduction/docker-terminology.md)
### [Contenedores, imágenes y registros de Docker](container-docker-introduction/docker-containers-images-registries.md)
## [Selección entre .NET Core y .NET Framework para contenedores de Docker](net-core-net-framework-containers/index.md)
### [Orientación general](net-core-net-framework-containers/general-guidance.md)
### [Cuándo elegir .NET Core para contenedores de Docker](net-core-net-framework-containers/net-core-container-scenarios.md)
### [Cuándo elegir .NET Framework para contenedores de Docker](net-core-net-framework-containers/net-framework-container-scenarios.md)
### [Tabla de decisiones: versiones de .NET Framework para su uso con Docker](net-core-net-framework-containers/container-framework-choice-factors.md)
### [Selección del sistema operativo de destino con contenedores de .NET](net-core-net-framework-containers/net-container-os-targets.md)
### [Imágenes de Docker de .NET oficiales](net-core-net-framework-containers/official-net-docker-images.md)
## [Diseñar la arquitectura de aplicaciones basadas en contenedor y microservicio](architect-microservice-container-applications/index.md)
### [Incluir en un contenedor aplicaciones monolíticas](architect-microservice-container-applications/containerize-monolithic-applications.md)
### [Estado y datos en aplicaciones de Docker](architect-microservice-container-applications/docker-application-state-data.md)
### [Arquitectura orientada a servicios](architect-microservice-container-applications/service-oriented-architecture.md)
### [Arquitectura de microservicios](architect-microservice-container-applications/microservices-architecture.md)
### [Propiedad de los datos por microservicio](architect-microservice-container-applications/data-sovereignty-per-microservice.md)
### [Arquitectura lógica frente a arquitectura física](architect-microservice-container-applications/logical-versus-physical-architecture.md)
### [Desafíos y soluciones de la administración de datos distribuidos](architect-microservice-container-applications/distributed-data-management.md)
### [Identificar los límites del modelo de dominio para cada microservicio](architect-microservice-container-applications/identify-microservice-domain-model-boundaries.md)
### [Comunicación directa de cliente a microservicio frente al patrón de puerta de enlace de API](architect-microservice-container-applications/direct-client-to-microservice-communication-versus-the-api-gateway-pattern.md)
### [Comunicación en una arquitectura de microservicio](architect-microservice-container-applications/communication-in-microservice-architecture.md)
### [Comunicación asincrónica basada en mensajes](architect-microservice-container-applications/asynchronous-message-based-communication.md)
### [Crear, desarrollar y controlar las versiones de los contratos y las API de microservicio](architect-microservice-container-applications/maintain-microservice-apis.md)
### [Direccionabilidad de microservicios y el Registro de servicios](architect-microservice-container-applications/microservices-addressability-service-registry.md)
### [Crear una interfaz de usuario compuesta en función de los microservicios, incluidos la forma y el diseño visual de la interfaz de usuario generados por varios microservicios](architect-microservice-container-applications/microservice-based-composite-ui-shape-layout.md)
### [Resistencia y la alta disponibilidad en microservicios](architect-microservice-container-applications/resilient-high-availability-microservices.md)
### [Orquestar microservicios y aplicaciones de varios contenedores para una alta escalabilidad y disponibilidad](architect-microservice-container-applications/scalable-available-multi-container-microservice-applications.md)
### [Uso de Azure Service Fabric](architect-microservice-container-applications/using-azure-service-fabric.md)
## [Proceso de desarrollo de aplicaciones basadas en Docker](docker-application-development-process/index.md)
### [Flujo de trabajo de desarrollo para aplicaciones de Docker](docker-application-development-process/docker-app-development-workflow.md)
## [Diseñar y desarrollar aplicaciones .NET basadas en varios contenedores y microservicios](multi-container-microservice-net-applications/index.md)
### [Diseñar una aplicación orientada a microservicios](multi-container-microservice-net-applications/microservice-application-design.md)
### [Crear un microservicio CRUD sencillo controlado por datos](multi-container-microservice-net-applications/data-driven-crud-microservice.md)
### [Definir una aplicación de varios contenedores con docker-compose.yml](multi-container-microservice-net-applications/multi-container-applications-docker-compose.md)
### [Usar un servidor de bases de datos que se ejecuta como un contenedor](multi-container-microservice-net-applications/database-server-container.md)
### [Implementar la comunicación basada en eventos entre microservicios (eventos de integración)](multi-container-microservice-net-applications/integration-event-based-microservice-communications.md)
### [Implementar un bus de eventos con RabbitMQ para el entorno de desarrollo o de prueba](multi-container-microservice-net-applications/rabbitmq-event-bus-development-test-environment.md)
### [Suscribirse a eventos](multi-container-microservice-net-applications/subscribe-events.md)
### [Probar aplicaciones web y servicios ASP.NET Core](multi-container-microservice-net-applications/test-aspnet-core-services-web-apps.md)
### [Implementar tareas en segundo plano en microservicios con IHostedService](multi-container-microservice-net-applications/background-tasks-with-ihostedservice.md)
### [Implementación de puertas de enlace de API con Ocelot](multi-container-microservice-net-applications/implement-api-gateways-with-ocelot.md)
## [Abordar la complejidad empresarial en un microservicio con patrones DDD y CQRS](microservice-ddd-cqrs-patterns/index.md)
### [Aplicar los patrones CQRS y DDD simplificados en un microservicio](microservice-ddd-cqrs-patterns/apply-simplified-microservice-cqrs-ddd-patterns.md)
### [Aplicar enfoques CQRS y CQS en un microservicio DDD en eShopOnContainers](microservice-ddd-cqrs-patterns/eshoponcontainers-cqrs-ddd-microservice.md)
### [Implementar lecturas/consultas en un microservicio CQRS](microservice-ddd-cqrs-patterns/cqrs-microservice-reads.md)
### [Diseñar un microservicio orientado a DDD](microservice-ddd-cqrs-patterns/ddd-oriented-microservice.md)
### [Diseñar un modelo de dominio de microservicio](microservice-ddd-cqrs-patterns/microservice-domain-model.md)
### [Implementar un modelo de dominio de microservicio con .NET Core](microservice-ddd-cqrs-patterns/net-core-microservice-domain-model.md)
### [Seedwork (clases base e interfaces reutilizables para el modelo de dominio)](microservice-ddd-cqrs-patterns/seedwork-domain-model-base-classes-interfaces.md)
### [Implementar objetos de valor](microservice-ddd-cqrs-patterns/implement-value-objects.md)
### [Usar las clases de enumeración en lugar de tipos de enumeración](microservice-ddd-cqrs-patterns/enumeration-classes-over-enum-types.md)
### [Diseñar las validaciones en el nivel de modelo de dominio](microservice-ddd-cqrs-patterns/domain-model-layer-validations.md)
### [Validación del lado cliente (validación de los niveles de presentación)](microservice-ddd-cqrs-patterns/client-side-validation.md)
### [Eventos de dominio: diseño e implementación](microservice-ddd-cqrs-patterns/domain-events-design-implementation.md)
### [Diseñar el nivel de persistencia de infraestructura](microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design.md)
### [Implementar el nivel de persistencia de infraestructura con Entity Framework Core](microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-implemenation-entity-framework-core.md)
### [Usar bases de datos NoSQL como una infraestructura de persistencia](microservice-ddd-cqrs-patterns/nosql-database-persistence-infrastructure.md)
### [Diseñar el nivel de aplicación de microservicios y API web](microservice-ddd-cqrs-patterns/microservice-application-layer-web-api-design.md)
### [Implementar el nivel de aplicación de microservicios mediante la API web](microservice-ddd-cqrs-patterns/microservice-application-layer-implementation-web-api.md)
## [Implementar aplicaciones resistentes](implement-resilient-applications/index.md)
### [Controlar errores parciales](implement-resilient-applications/handle-partial-failure.md)
### [Estrategias para controlar errores parciales](implement-resilient-applications/partial-failure-strategies.md)
### [Implementar reintentos con retroceso exponencial](implement-resilient-applications/implement-retries-exponential-backoff.md)
### [Implementar conexiones SQL resistentes de Entity Framework Core](implement-resilient-applications/implement-resilient-entity-framework-core-sql-connections.md)
### [Exploración de reintentos de llamada HTTP personalizados con retroceso exponencial](implement-resilient-applications/explore-custom-http-call-retries-exponential-backoff.md)
### [Uso de HttpClientFactory para implementar solicitudes HTTP resistentes](implement-resilient-applications/use-httpclientfactory-to-implement-resilient-http-requests.md)
### [Implementación de reintentos de llamada HTTP con retroceso exponencial con Polly](implement-resilient-applications/implement-http-call-retries-exponential-backoff-polly.md)
### [Implementación del patrón de interruptor](implement-resilient-applications/implement-circuit-breaker-pattern.md)
### [Supervisión de matenimiento](implement-resilient-applications/monitor-app-health.md)
## [Proteger microservicios y aplicaciones web de .NET](secure-net-microservices-web-applications/index.md)
### [Acerca de la autorización en microservicios y aplicaciones web de .NET](secure-net-microservices-web-applications/authorization-net-microservices-web-applications.md)
### [Almacenar secretos de aplicación de forma segura durante el desarrollo](secure-net-microservices-web-applications/developer-app-secrets-storage.md)
### [Usar Azure Key Vault para proteger secretos en tiempo de producción](secure-net-microservices-web-applications/azure-key-vault-protects-secrets.md)
## [Puntos clave](key-takeaways.md)
