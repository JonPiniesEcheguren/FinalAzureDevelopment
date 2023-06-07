### Tema 2: Implement secure Azure solutions	

- Preguntas:	

  - ¿Qué es Azure Key Vault y cómo se utiliza para proteger secretos y claves criptográficas?
  
    Es un servicio de administración de secretos y claves criptográficas ofrecido por Microsoft Azure. Proporciona un entorno seguro para almacenar y administrar secretos, como contraseñas, cadenas de conexión, claves de API y certificados, así como claves criptográficas, como claves de cifrado y claves de firma, utiliza técnicas de seguridad avanzadas. Todo esto  se almacenan en hardware de seguridad respaldado por Microsoft, lo que proporciona una mayor protección contra amenazas físicas y ataques basados en hardware. Además, se implementan controles de acceso y auditoría exhaustivos para garantizar que solo las personas autorizadas puedan acceder a los secretos y las claves.
  
  - ¿Cuál es el papel de las Identidades Administradas (Managed Identities) en la seguridad de Azure?
  
    Las Identidades Administradas (Managed Identities) desempeñan un papel fundamental en la seguridad de Azure al proporcionar una forma segura y conveniente de autenticar y autorizar recursos en la nube. Una Identidad Administrada es una entidad de seguridad dentro de Azure Active Directory (Azure AD) que se asigna a un recurso específico, como una máquina virtual o una función de Azure.
  
  - ¿Cómo se configuran y se utilizan Azure Key Vault y las Identidades Administradas?
  
    Configuración de Azure Key Vault:
  
    - En Azure Portal, crea un nuevo Azure Key Vault.
    - Define las políticas de acceso para especificar quién puede acceder a los secretos y las claves almacenadas.
    - Puedes configurar características adicionales, como la habilitación de auditoría y la configuración de reglas de acceso.
  
    Uso de Azure Key Vault:
  
    - Almacena tus secretos y claves criptográficas en Azure Key Vault. Esto puede incluir contraseñas, claves de API, cadenas de conexión, certificados y claves de cifrado.
    - Tus aplicaciones pueden acceder a los secretos y las claves almacenados en Key Vault de manera segura. Esto se hace autenticando y autorizando la aplicación para acceder a Azure Key Vault utilizando identidades administradas.
  
    Configuración de Identidades Administradas:
  
    - En Azure Portal, crea una identidad administrada y asígnala a un recurso específico, como una máquina virtual o una función de Azure.
    - Configura los permisos de la identidad administrada, asignándole roles apropiados para controlar su nivel de acceso.
  
    Uso de Identidades Administradas:
  
    - En la configuración de tus aplicaciones, puedes especificar que se autentiquen utilizando una identidad administrada en lugar de credenciales explícitas.
    - La identidad administrada se autenticará automáticamente ante los servicios de Azure en nombre de la aplicación, sin necesidad de proporcionar credenciales adicionales.
    - Puedes utilizar la identidad administrada para acceder a otros servicios de Azure, como Azure Key Vault, y obtener los secretos y las claves necesarias para que tu aplicación funcione.
  
- Identificar y explicar (comprobar si es posible) de la batería de Preguntas 3 preguntas por cada integrante relacionadas con Azure solutions:
  - Pregunta 2 pág 128:
  
    - Esta pregunta está relacionada con la corrección de un error en el sitio web de una empresa. La respuesta correcta es realizar cuatro acciones en secuencia:
  
      1. Generar un certificado.
      2. Subir el certificado al Azure Key Vault (un servicio de almacenamiento de claves en la nube de Azure).
      3. Importar el certificado al Azure App Service (un servicio de alojamiento web en la nube de Azure).
      4. Actualizar la línea SC05 del archivo security.cs para incluir la gestión de errores y luego volver a implementar el código.
  
      La respuesta es correcta porque aborda el problema de manera lógica y secuencial. Primero se genera el certificado necesario, luego se almacena de forma segura en Azure Key Vault, después se importa al Azure App Service y finalmente se actualiza el código para manejar el error específico que se está produciendo.
  
      Este enfoque asegura que el certificado esté disponible y protegido correctamente, y también aborda el problema de la excepción criptográfica que se muestra en el sitio web.
  - Pregunta 21 pág 161:
  
    - La pregunta plantea el escenario de tener una aplicación que incluye una aplicación web de Azure y varias aplicaciones de Azure Functions. Los secretos de la aplicación, como las cadenas de conexión y los certificados, se almacenan en Azure Key Vault. Se requiere diseñar un enfoque para cargar los secretos de la aplicación. La respuesta correcta es la opción C: Crear una identidad administrada asignada por el sistema en cada App Service con permiso para acceder a Key Vault, y es correcta porque permite utilizar las referencias de Azure Key Vault en las App Service y Azure Functions. Las referencias de Key Vault actualmente solo admiten identidades administradas asignadas por el sistema, no se pueden usar identidades asignadas por el usuario.
  - Pregunta 22 pág 161:
  
    - La pregunta plantea el escenario de desarrollar un sitio web de gestión de documentos de registros médicos. El sitio web se utiliza para almacenar copias escaneadas de formularios de admisión de pacientes. Si estas formas de admisión almacenadas son descargadas por un tercero, el contenido de los formularios no debe comprometerse.
  
      La respuesta correcta es la opción A: Sí, la solución cumple con el objetivo.
  
      La solución propuesta consiste en crear una clave de Azure Key Vault llamada "skey", encriptar los formularios de admisión utilizando la parte de clave pública de "skey" y almacenar los datos encriptados en Azure Blob storage.
  
      Esta solución cumple con el objetivo de no comprometer el contenido de los formularios si son descargados por un tercero. Al encriptar los formularios utilizando una clave almacenada en Azure Key Vault y luego almacenar los datos encriptados en Azure Blob storage, se asegura que solo aquellos que tengan acceso a la clave privada correspondiente puedan descifrar y acceder al contenido de los formularios. Esto proporciona una capa adicional de seguridad para proteger la información confidencial de los pacientes.
