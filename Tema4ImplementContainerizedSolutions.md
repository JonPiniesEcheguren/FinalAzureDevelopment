# Preguntas - Tema 4

**¿Cuál es la diferencia entre Azure Container Registry, Azure Container Instances y Azure Container Apps?**	

Azure Container Registry (ACR): Es un servicio de registro privado de contenedores que permite almacenar, administrar y desplegar imágenes de contenedores de forma segura. ACR es ideal para crear y mantener un repositorio centralizado de imágenes de contenedores que se pueden usar en múltiples entornos de Azure.

Azure Container Instances (ACI): Es un servicio de Azure que permite ejecutar contenedores de forma rápida y sencilla sin tener que administrar una infraestructura de máquinas virtuales. ACI es ideal para cargas de trabajo aisladas o con poco tráfico, ya que se encarga de aprovisionar y escalar automáticamente los recursos necesarios para ejecutar los contenedores.

Azure Container Apps: Es un servicio que permite implementar aplicaciones en contenedores en Azure de manera simplificada y sin la necesidad de administrar directamente la infraestructura subyacente. Con Container Apps, los desarrolladores pueden centrarse en el desarrollo de aplicaciones mientras Azure se encarga de los aspectos de implementación y administración del entorno de contenedores.

En resumen, Azure Container Registry es un repositorio de imágenes de contenedores, Azure Container Instances permite ejecutar contenedores sin administrar la infraestructura y Azure Container Apps simplifica la implementación de aplicaciones en contenedores en Azure.

**¿Cómo se utiliza Azure Container Registry para almacenar y gestionar imágenes de contenedores?**

Azure Container Registry (ACR) se utiliza para almacenar y gestionar imágenes de contenedores en Azure. A continuación, te mostraré los pasos básicos para utilizar ACR:

1. Crear un registro: En Azure Portal, crea un nuevo registro de contenedores en ACR. Define un nombre único y selecciona la suscripción, grupo de recursos y ubicación adecuados.
2. Iniciar sesión en el registro: Una vez creado el registro, utiliza las credenciales proporcionadas para iniciar sesión desde tu entorno de desarrollo o herramienta de línea de comandos. Esto permitirá la comunicación segura con el registro.
3. Preparar la imagen del contenedor: Prepara tu aplicación en contenedor y crea una imagen Docker. Puedes utilizar Docker CLI, Azure CLI o herramientas de construcción de imágenes como Dockerfile para este paso.
4. Etiquetar y subir la imagen: Etiqueta la imagen con la dirección del registro y la versión deseada. Luego, realiza la carga de la imagen al registro utilizando el comando `docker push`.
5. Gestionar las imágenes: Una vez que las imágenes están en el registro, puedes administrarlas, organizarlas y etiquetarlas según tus necesidades. Puedes usar Azure Portal, Azure CLI o la API de ACR para realizar estas tareas.
6. Implementar y usar las imágenes: Para utilizar las imágenes de contenedor almacenadas en ACR, puedes desplegarlas en diferentes servicios de Azure, como Azure Container Instances, Azure Kubernetes Service (AKS) u otros servicios de orquestación de contenedores.
7. Mantener y asegurar el registro: Asegúrate de mantener actualizado y asegurado el registro de ACR. Puedes configurar opciones de acceso seguro, habilitar la autenticación, habilitar la replicación geográfica, habilitar la eliminación de imágenes antiguas y configurar políticas de retención según tus requisitos.

Recuerda que estos son solo los pasos básicos para utilizar Azure Container Registry. Hay muchas otras características y funcionalidades avanzadas disponibles, como la administración de roles, la integración con Azure Active Directory, la administración del ciclo de vida de las imágenes, etc., que puedes explorar según tus necesidades específicas.

**¿Cuál es el propósito y la ventaja de utilizar Azure Container Instances para ejecutar contenedores sin necesidad de administrar una infraestructura subyacente?**	

El propósito principal de Azure Container Instances (ACI) es permitirte ejecutar contenedores de forma rápida y sencilla sin tener que preocuparte por administrar una infraestructura subyacente. Algunas de las ventajas clave de utilizar ACI son:

1. Facilidad de uso: ACI simplifica enormemente el proceso de ejecución de contenedores al eliminar la necesidad de aprovisionar y administrar máquinas virtuales o clústeres. Puedes crear y ejecutar contenedores con solo unos pocos clics o mediante comandos de la línea de comandos.
2. Escalado automático: ACI escala automáticamente los recursos necesarios para ejecutar tus contenedores en función de la carga de trabajo. Puedes configurar límites de recursos para controlar el uso de CPU y memoria, y ACI ajustará automáticamente la capacidad según sea necesario.
3. Pago por uso: ACI utiliza un modelo de pago por uso, lo que significa que solo pagas por el tiempo que tus contenedores están en ejecución y por los recursos que consumen. No hay costos adicionales asociados con la administración de máquinas virtuales o clústeres subyacentes.
4. Aislamiento y seguridad: Cada contenedor se ejecuta en un entorno aislado, lo que garantiza la seguridad y evita la interferencia entre contenedores. ACI también proporciona opciones de red y seguridad avanzadas, como la integración con redes virtuales y grupos de seguridad de red.
5. Integración con otros servicios de Azure: ACI se integra de manera nativa con otros servicios de Azure, como Azure Virtual Network, Azure Monitor y Azure Logic Apps, lo que te permite construir soluciones más completas y escalables.
6. Alta disponibilidad: ACI garantiza la alta disponibilidad de tus contenedores mediante la redundancia automática en diferentes hosts y zonas de disponibilidad de Azure.

En resumen, Azure Container Instances simplifica la ejecución de contenedores al eliminar la necesidad de administrar la infraestructura subyacente. Proporciona facilidad de uso, escalado automático, pago por uso, aislamiento y seguridad, integración con servicios de Azure y alta disponibilidad, lo que permite un enfoque ágil y eficiente para la ejecución de contenedores en Azure.

# Preguntas relacionadas con Azure container registry y Azure Event Instance y Azure Container Apps

**Pregunta 1:**

QUESTION 2- Pagina 64

You need to store the user agreements. 

Where should you store the agreement after it is completed? 

A. Azure Storage queue 

B. Azure Event Hub 

C. Azure Service Bus topic 

D. Azure Event Grid topic 

Correct Answer: B  

Explanation/Reference: 

Explanation: Azure Event Hub is used for telemetry and distributed data streaming. 

This service provides a single solution that enables rapid data retrieval for real-time processing as well as repeated replay of stored raw data. It can capture the streaming data into a file for processing and analysis. 

It has the following characteristics: 

- low latency 
- capable of receiving and processing millions of events per second 
- at least once delivery

**Pregunta 2:**

QUESTION 1 - Pagina 218

You need to configure the integration for Azure Service Bus and Azure Event Grid. How should you complete the CLI statement? To answer, select the appropriate options in the answer area.

![image-20230602131647152](C:\Users\marin\AppData\Roaming\Typora\typora-user-images\image-20230602131647152.png)

Correct Answer: Box 1:eventgrid
						   Box 2:event-subscription 
						   Box 3:servicebusqueue

Explanation/Reference: 

Explanation: Box 1: eventgrid To create event subscription use: az eventgrid event-subscription create 

Box 2: event-subscription 

Box 3: servicebusqueue 

Scenario: Azure Service Bus and Azure Event Grid 

Azure Event Grid must use Azure Service Bus for queue-based load leveling. Events in Azure Event Grid must be routed directly to Service Bus queues for use in buffering. Events from Azure Service Bus and other Azure services must continue to be routed to Azure Event Grid for processing.

**Pregunta 3:**

QUESTION 6 - Pagina 28

You develop a software as a service (SaaS) offering to manage photographs. Users upload photos to a web service which then stores the photos in Azure Storage Blob storage. The storage account type is Generalpurpose V2. 

When photos are uploaded, they must be processed to produce and save a mobile-friendly version of the image. The process to produce a mobile-friendly version of the image must start in less than one minute. 

You need to design the process that starts the photo processing. 

Solution: Trigger the photo processing from Blob storage events. 

Does the solution meet the goal? 

A. Yes 

B. No 

Correct Answer: B  

Explanation/Reference: 

Explanation: You need to catch the triggered event, so move the photo processing to an Azure Function triggered from the blob upload 

Note: Azure Storage events allow applications to react to events. Common Blob storage event scenarios include image or video processing, search indexing, or any file-oriented workflow. 

Events are pushed using Azure Event Grid to subscribers such as Azure Functions, Azure Logic Apps, or even to your own http listener. 

Note: Only storage accounts of kind StorageV2 (general purpose v2) and BlobStorage support event integration. Storage (general purpose v1) does not support integration with Event Grid.
