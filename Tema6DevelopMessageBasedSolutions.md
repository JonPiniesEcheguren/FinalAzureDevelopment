# Preguntas - Tema 6

1. **¿Cuál es la diferencia entre Azure Message Queue, Azure Service Bus y Azure Queue Storage en términos de funcionalidad y casos de uso?**	

Azure Message Queue, Azure Service Bus y Azure Queue Storage son servicios de mensajería y colas de Azure que se utilizan para diferentes casos de uso. A continuación, se describen sus diferencias en términos de funcionalidad y casos de uso:

Azure Message Queue (AMQ):

- AMQ es un servicio de cola de mensajes simple y ligero que ofrece una funcionalidad básica de encolado y desencolado de mensajes.
- Se centra en la entrega fiable de mensajes en el orden correcto.
- Es adecuado para escenarios simples de productor/consumidor en los que la prioridad es la entrega de mensajes de manera rápida y sencilla, sin necesidad de características más avanzadas.
- Es escalable y de bajo costo, lo que lo hace ideal para aplicaciones con cargas de trabajo más ligeras.

Azure Service Bus (ASB):

- ASB es un servicio de mensajería empresarial avanzado que ofrece capacidades de colas, temas y suscripciones.
- Proporciona características más avanzadas como filtrado de mensajes, entrega en lotes, transacciones y control de errores.
- Es adecuado para escenarios más complejos y empresariales, como el procesamiento distribuido, la integración de sistemas, la notificación de eventos y la implementación de patrones de mensajería avanzados.
- Ofrece una mayor flexibilidad y opciones de configuración en comparación con AMQ, pero también implica una mayor complejidad.

Azure Queue Storage:

- Azure Queue Storage es un servicio de almacenamiento de colas en la nube que permite almacenar y procesar mensajes en una cola de manera duradera.
- Está diseñado para ser una solución de cola simple y de bajo costo, sin las capacidades avanzadas de AMQ y ASB.
- Es adecuado para escenarios de colas básicas, donde se necesita persistencia y orden en la entrega de mensajes, pero no se requieren características más complejas.
- Puede integrarse con otros servicios de Azure, como Azure Functions y Azure WebJobs, para crear flujos de trabajo y procesos asincrónicos.

En resumen, Azure Message Queue es una opción simple y liviana para encolar y desencolar mensajes básicos. Azure Service Bus es un servicio de mensajería empresarial con capacidades avanzadas y flexibilidad para escenarios más complejos. Azure Queue Storage es una solución básica y de bajo costo para almacenar y procesar mensajes en una cola. La elección entre ellos dependerá de las necesidades específicas de tu aplicación o caso de uso.

2. **¿Cómo se utiliza Azure Message Queue para el envío y recepción de mensajes entre componentes de una aplicación distribuida?**	

Azure Message Queue se puede utilizar para el envío y recepción de mensajes entre componentes de una aplicación distribuida en Azure. Aquí hay una guía básica sobre cómo utilizar Azure Message Queue para este propósito:

1. Crear una cola de mensajes: En Azure Portal, crea una nueva instancia de Azure Message Queue. Define un nombre único y configura cualquier otra configuración necesaria, como el tamaño máximo de la cola y la retención de mensajes.
2. Configurar las credenciales de acceso: Obtén las credenciales de acceso necesarias para conectarte a la cola de mensajes. Puedes obtenerlas desde Azure Portal o utilizando la API de administración de Azure.
3. Productor de mensajes: En el componente de tu aplicación que actúa como productor de mensajes, establece una conexión con la cola de mensajes utilizando las credenciales de acceso. Luego, puedes enviar mensajes a la cola utilizando la API o el SDK adecuado para el lenguaje de programación que estés utilizando.
4. Consumidor de mensajes: En el componente de tu aplicación que actúa como consumidor de mensajes, también establece una conexión con la cola de mensajes utilizando las credenciales de acceso. Luego, puedes recibir mensajes de la cola y procesarlos en función de la lógica de tu aplicación.
5. Manejo de mensajes: Una vez que se recibe un mensaje, puedes realizar diferentes acciones según tus necesidades. Puedes procesar el mensaje, almacenar información en una base de datos, realizar operaciones adicionales o enviar una respuesta a otro componente.
6. Administración de la cola: Asegúrate de administrar la cola de mensajes según tus requisitos. Puedes establecer políticas de retención de mensajes, configurar tiempos de espera y manejar los casos de error o mensajes no procesados.

Recuerda que esto es solo un resumen básico. Azure Message Queue también ofrece otras características avanzadas, como el filtrado de mensajes, el control de errores y la entrega en lotes, que puedes explorar según tus necesidades específicas.

3. **¿Cuál es el propósito y la ventaja de utilizar Azure Service Bus en comparación con otros servicios de mensajería?**	

El propósito principal de Azure Service Bus es proporcionar una solución de mensajería empresarial avanzada en la nube. Algunas de las ventajas clave de utilizar Azure Service Bus en comparación con otros servicios de mensajería son:

1. Escalabilidad y rendimiento: Azure Service Bus está diseñado para manejar cargas de trabajo empresariales y escalar automáticamente según la demanda. Puede manejar grandes volúmenes de mensajes y ofrecer un rendimiento confiable y predecible incluso en situaciones de alta carga.
2. Mensajería avanzada y patrones de comunicación: Service Bus ofrece características avanzadas como colas, temas y suscripciones, que permiten implementar patrones de mensajería complejos y escenarios de integración de sistemas. Puedes utilizar filtros y reglas para enrutar mensajes de manera selectiva, realizar transformaciones de mensajes y habilitar la comunicación pub/sub (publicador/suscriptor).
3. Fiabilidad y durabilidad: Service Bus garantiza la entrega confiable de mensajes y proporciona almacenamiento persistente de mensajes en caso de fallas temporales o desconexiones. Los mensajes se mantienen de manera duradera en la cola o el tema hasta que se procesen correctamente.
4. Transacciones y control de errores: Service Bus admite transacciones de mensajes, lo que permite la atomicidad y consistencia en el procesamiento de múltiples mensajes. Además, ofrece mecanismos para el control de errores y la gestión de dead-letter (mensajes no procesados o con errores) para facilitar la resolución de problemas y el manejo de errores en el flujo de mensajes.
5. Integración con otros servicios de Azure: Service Bus se integra estrechamente con otros servicios de Azure, como Azure Functions, Azure Logic Apps y Azure Event Grid, lo que te permite construir soluciones más completas y escalables utilizando un enfoque de arquitectura de eventos.
6. Seguridad y cumplimiento: Service Bus proporciona opciones de seguridad avanzadas, como la autenticación y autorización basada en tokens y la integración con Azure Active Directory. Además, cumple con los estándares y certificaciones de cumplimiento, lo que garantiza la seguridad y confidencialidad de los mensajes.

En resumen, Azure Service Bus ofrece una solución de mensajería empresarial con características avanzadas, escalabilidad, rendimiento confiable y una variedad de opciones de comunicación. Su objetivo es proporcionar una plataforma sólida y flexible para la integración de sistemas, la comunicación distribuida y el procesamiento de mensajes en escenarios empresariales complejos.

# Preguntas relacionadas con Azure Service Bus

Pregunta 1:

QUESTION 20 - Pagina 245

You are developing an Azure messaging solution. 

You need to ensure that the solution meets the following requirements: 

- Provide transactional support. 
- Provide duplicate detection. 
- Store the messages for an unlimited period of time. 

Which two technologies will meet the requirements? Each correct answer presents a complete solution. 

NOTE: Each correct selection is worth one point. 

A. Azure Service Bus Topic 

B. Azure Service Bus Queue 

C. Azure Storage Queue 

D. Azure Event Hub 

Correct Answer: AB 

Explanation/Reference: 

Explanation: The Azure Service Bus Queue and Topic has duplicate detection. Enabling duplicate detection helps keep track of the application-controlled MessageId of all messages sent into a queue or topic during a specified time window. 

Incorrect Answers: 

C: There is just no mechanism that can query a Storage queue and find out if a message with the same contents is already there or was there before. 

D: Azure Event Hub does not have duplicate detection

Pregunta 2:

QUESTION 18 - Pagina 243

DRAG DROP 

You develop software solutions for a mobile delivery service. You are developing a mobile app that users can use to order from a restaurant in their area. The app uses the following workflow: 

1. A driver selects the restaurants from which they will deliver orders. 
2. Orders are sent to all available drivers in an area. 
3. Only orders for the selected restaurants will appear for the driver. 
4. The first driver to accept an order removes it from the list of available orders. 

You need to implement an Azure Service Bus solution. 

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

![image-20230602131916898](C:\Users\marin\AppData\Roaming\Typora\typora-user-images\image-20230602131916898.png)

Correct Answer: Box 1:Create a single Service Bus Namespace
						   Box 2:Create a Service Bus Topic for each restaurant for which a driver can receive messages 
						   Box 3:Create a Service Bus subscription for each restaurant for which a driver can receive orders

Explanation/Reference: 

Explanation: Box 1: Create a single Service Bus Namespace To begin using Service Bus messaging entities in Azure, you must first create a namespace with a name that is unique across Azure. A namespace provides a scoping container for addressing Service Bus resources within your application. 

Box 2: Create a Service Bus Topic for each restaurant for which a driver can receive messages. Create topics. 

Box 3: Create a Service Bus subscription for each restaurant for which a driver can receive orders. Topics can have multiple, independent subscriptions.

Pregunta 3:

QUESTION 16 - Pagina 241

A company is developing a solution that allows smart refrigerators to send temperature information to a central location. 

The solution must receive and store messages until they can be processed. You create an Azure Service Bus instance by providing a name, pricing tier, subscription, resource group, and location. 

You need to complete the configuration. 

Which Azure CLI or PowerShell command should you run?

A. Az group create
			--name fridge-rg
			--location fridge-loc

B. New-AzureRmServiceBusNamespace
		-ResourceGroupName fridge-rg
		-NamespaceName fridge-ns
		-Location fridge-loc

C. New-AzureRmSericeName fridge-rg
		-ResourceGroupName fridge-rg
		-NamespaceName fridge-ns
		-Name fridge-q
		-EnablePartitioning $False

D. Get-AzureRmServiceBusKey
		-ResourceGroupName fridge-rg
		-Namespace fridge-ns
		-Name RootManageSharedAccessKey

Correct Answer: C 

Explanation/Reference: 

Explanation: A service bus instance has already been created (Step 2 below). Next is step 3, Create a Service Bus queue. 

Note: 

Steps: 

Step 1: # Create a resource group 

resourceGroupName="myResourceGroup" 

az group create --name $resourceGroupName --location eastus 

Step 2: # Create a Service Bus messaging namespace with a unique name 

namespaceName=myNameSpace$RANDOM 

az servicebus namespace create --resource-group $resourceGroupName --name $namespaceName -- location eastus 

Step 3: # Create a Service Bus queue 

az servicebus queue create --resource-group $resourceGroupName --namespace-name 

$namespaceName --name BasicQueue 

Step 4: # Get the connection string for the namespace connectionString=$(az servicebus namespace authorization-rule keys list --resource-group 

$resourceGroupName --namespace-name $namespaceName --name RootManageSharedAccessKey -- query primaryConnectionString --output tsv)
