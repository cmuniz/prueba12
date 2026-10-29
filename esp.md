## Componentes principales de la infraestructura

La infraestructura de la aplicación se compone de diversos servicios de AWS y herramientas de integración, observabilidad y análisis de datos, que trabajan conjuntamente para permitir la generación de dashboards mediante una interfaz conversacional. A continuación, se describen los principales componentes y su función dentro de la arquitectura.

\- Amazon EKS (Elastic Kubernetes Service): Plataforma de ejecución y orquestación de contenedores sobre la que se despliegan los componentes principales de la aplicación.

- Frontend: Proporciona la interfaz de usuario, gestiona la interacción con el chatbot y presenta los resultados generados, incluidos los dashboards y sus visualizaciones.
- Backend: Gestiona la lógica de negocio y la orquestación de las peticiones, coordina las llamadas a los modelos de lenguaje y a los servicios externos, y procesa las consultas necesarias para generar los dashboards.

\- Amazon Bedrock: Proporciona acceso a los modelos de lenguaje (LLM) utilizados para interpretar las peticiones de los usuarios y generar las consultas DAX necesarias para obtener y analizar los datos.

\- PostgreSQL: Base de datos relacional destinada al almacenamiento persistente de la información estructurada de la aplicación.

\- Amazon DynamoDB: Base de datos NoSQL utilizada para almacenar y gestionar las sesiones de usuario y la información asociada al estado de las conversaciones.

\- Amazon ElastiCache for Redis: Servicio de caché en memoria que permite almacenar temporalmente información de acceso frecuente, reducir la latencia y disminuir la necesidad de repetir determinadas operaciones o consultas.

\- Amazon S3 (Simple Storage Service): Servicio de almacenamiento de objetos utilizado para guardar los archivos de configuración de los modelos semánticos, necesarios para definir la estructura de los datos y facilitar la generación de consultas coherentes con el modelo analítico.

\- Microsoft Power BI: Plataforma de inteligencia de negocio que actúa como fuente de datos para la aplicación, proporcionando acceso a los modelos semánticos y a los datos sobre los que se ejecutan las consultas DAX y se construyen las visualizaciones.

\- Langfuse: Herramienta de observabilidad y trazabilidad de las aplicaciones basadas en LLM. Permite registrar y analizar las interacciones con los modelos, las trazas de ejecución, las llamadas realizadas y los resultados obtenidos, facilitando la evaluación y la depuración del comportamiento del sistema.

\- Datadog: Plataforma de monitorización y observabilidad de la infraestructura y de la aplicación. Permite supervisar métricas, logs y trazas distribuidas para detectar errores, analizar el rendimiento y facilitar el diagnóstico de incidencias.

\- Microsoft Fabric Data Agent: Componente de integración complementario que permite explorar y analizar los datos mediante agentes de inteligencia artificial conectados a los recursos de Microsoft Fabric. Esta integración constituye una vía de análisis paralela al flujo principal de generación de consultas DAX, ofreciendo una alternativa para responder a las preguntas de los usuarios a partir de los datos disponibles.

