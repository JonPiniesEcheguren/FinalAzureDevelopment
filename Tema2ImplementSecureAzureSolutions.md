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
  - Pregunta 21 pág 159:
  - Pregunta 22 pág 161:
