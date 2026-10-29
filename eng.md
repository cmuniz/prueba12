## Main Infrastructure Components

The application's infrastructure consists of several AWS services and tools for integration, observability, and data analysis, which work together to enable dashboard generation through a conversational interface. The following sections describe the main components and their roles within the architecture.

- **Amazon EKS (Elastic Kubernetes Service):** Provides the container orchestration and execution platform on which the application's main components are deployed.
  - **Frontend:** Provides the user interface, manages user interactions with the chatbot, and displays the generated results, including dashboards and visualizations.
  - **Backend:** Handles the business logic and request orchestration, coordinates calls to language models and external services, and processes the queries required to generate dashboards.

- **Amazon Bedrock:** Provides access to large language models (LLMs) used to interpret user requests and generate the DAX queries required to retrieve and analyze data.

- **PostgreSQL:** Relational database used for the persistent storage of structured application data.

- **Amazon DynamoDB:** NoSQL database used to store and manage user sessions and the information associated with conversation state.

- **Amazon ElastiCache for Redis:** In-memory caching service used to store frequently accessed information temporarily, reduce latency, and minimize the need to repeat certain operations or queries.

- **Amazon S3 (Simple Storage Service):** Object storage service used to store semantic model configuration files, which are required to define the data structure and facilitate the generation of queries consistent with the analytical model.

- **Microsoft Power BI:** Business intelligence platform that acts as the application's data source, providing access to semantic models and the data against which DAX queries are executed and visualizations are built.

- **Langfuse:** Observability and tracing tool for LLM-powered applications. It enables the recording and analysis of model interactions, execution traces, API calls, and generated outputs, facilitating the evaluation and debugging of system behavior.

- **Datadog:** Infrastructure and application monitoring and observability platform. It enables the monitoring of metrics, logs, and distributed traces to detect errors, analyze performance, and facilitate incident diagnosis.

- **Microsoft Fabric Data Agent:** Complementary integration component that enables data exploration and analysis through AI agents connected to Microsoft Fabric resources. This integration provides an alternative analytical workflow alongside the primary DAX query generation process, offering an additional way to answer user questions based on the available data.

