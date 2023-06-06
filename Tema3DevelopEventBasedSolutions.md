### Tema 3: Develop event-based solutions

- Preguntas:	

  - ¿Qué son las soluciones basadas en eventos y cómo se diferencian de las arquitecturas tradicionales basadas en solicitudes y respuestas?

    Las soluciones basadas en eventos se basan en la comunicación a través de eventos significativos, donde los componentes del sistema generan y consumen eventos importantes sin una interacción directa y sincrónica. Esto permite una mayor flexibilidad y escalabilidad en comparación con las arquitecturas tradicionales basadas en solicitudes y respuestas, ya que los componentes pueden responder de manera independiente y en tiempo real a los cambios en el sistema.

  - ¿Cuál es el papel de Azure Event Grid en la implementación de soluciones basadas en eventos y cómo se integra con otros servicios de Azure?

    Azure Event Grid ayuda a que los diferentes componentes de un sistema se comuniquen entre sí al enviar y recibir mensajes sobre eventos importantes. Puede detectar eventos de una variedad de servicios de Azure, como Azure Blob Storage, Azure Functions y Azure Logic Apps, así como eventos personalizados generados por tus propias aplicaciones.

    La integración con otros servicios de Azure es una de las fortalezas de Azure Event Grid. Puedes configurar Event Grid para que envíe eventos a otros servicios de Azure, como Azure Functions, Azure Logic Apps y Azure Event Hubs, en función de los eventos que se generen. Esto permite que esos servicios respondan y realicen acciones específicas en tiempo real según los eventos recibidos.

  - ¿Cuáles son los beneficios y casos de uso comunes de Azure Event Hub en el procesamiento y análisis de flujos masivos de eventos en tiempo real?

    Azure Event Hub ofrece una solución escalable y confiable para procesar y analizar flujos masivos de eventos en tiempo real. Algunos de los beneficios y casos de uso comunes de Azure Event Hub son:

    1. Escalabilidad: Event Hub puede manejar grandes volúmenes de eventos entrantes en tiempo real. Puedes enviar millones de eventos por segundo y asegurarte de que se procesen de manera eficiente.
    2. Retención de eventos: Event Hub almacena eventos durante un período configurable, lo que permite que los datos se mantengan disponibles para su posterior procesamiento y análisis, incluso si los consumidores no están disponibles en ese momento.
    3. Distribución de eventos: Event Hub permite distribuir eventos a varios consumidores de forma paralela. Esto facilita el procesamiento en paralelo y la escala horizontal de los consumidores para manejar cargas de trabajo masivas.
    4. Procesamiento en tiempo real: Event Hub es ideal para el procesamiento y análisis en tiempo real de flujos de eventos. Puedes conectarlo a servicios de procesamiento en tiempo real, como Azure Stream Analytics o Azure Databricks, para realizar análisis, agregaciones y tomar acciones en tiempo real.
    5. Integración con Azure ecosystem: Event Hub se integra con otros servicios de Azure, lo que facilita la construcción de soluciones completas. Puedes utilizarlo junto con servicios de almacenamiento, análisis y visualización de datos, como Azure Blob Storage, Azure Data Lake Analytics y Power BI.
    6. Casos de uso comunes: Event Hub se utiliza en una amplia variedad de casos de uso, como telemetría y registro de aplicaciones, seguimiento de dispositivos de IoT, transmisión de datos en tiempo real, análisis de datos en tiempo real, detección de anomalías y mucho más.

- 
  Identificar y explicar (comprobar si es posible) de la batería de Preguntas 3 preguntas por cada integrante relacionadas con Develop event-base solutions:

  - Pregunta 2 pág 64:

  - Pregunta 6 pág 135:

  - Pregunta 6 pág 147:
