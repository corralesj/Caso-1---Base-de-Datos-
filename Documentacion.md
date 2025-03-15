**PAYMENT ASSISTANT**





Es importante recalcar que nuestro diseño de base de datos, en las tablas de usuarios, roles, permisos, transacciones y todas las demás, está inspirado en las explicaciones del profesor durante las clases, bajo el principio de siempre insertar y no actualizar. Esto reduce el riesgo de errores, además de mejorar el rendimiento del sistema.
![Imagen 1](users.png)
![Imagen 2](countries.png)
![Imagen 3](contacts.png)
![Imagen 4](metodospagos.png)
![Imagen 5](pagos.png)
![Imagen 6](transacciones.png)
![Imagen 7](suscriptions.png)

Esto reduce el riesgo de errores, además de mejorar el rendimiento del sistema. 

Ahora bien, a continuación, están los requerimientos funcionales explicados, las tablas correspondientes necesarias, el por qué son importantes, y además algunos ejemplos de aplicaciones o sitios web que utilizan estos métodos:

![Imagen](audio.png)

**Interacción por Voz y Registro de Pagos**

La aplicación permite a los usuarios registrar pagos recurrentes mediante comandos de voz. Se utiliza procesamiento de lenguaje natural para identificar detalles como el servicio, monto, fecha y frecuencia. Cada interacción se confirma con el usuario antes de ser almacenada.

Tablas involucradas:
- Usuarios: Almacena la información personal y de autenticación (ID, nombre, contraseña, etc.).
- VoiceTranscription: Guarda las transcripciones de los comandos de voz.
- AI_Interaction: Registra cada interacción, incluyendo los comandos extraídos y las respuestas generadas.

Esta combinación permite que el sistema capture con precisión las órdenes emitidas por voz y las vincule a la identidad del usuario, facilitando el seguimiento y la mejora continua de la experiencia. Esta funcionalidad la utilizan aplicaciones como Google Assistant y Amazon Alexa para permitir a los usuarios interactuar de manera natural y sin fricciones. Los usuarios se benefician de la rapidez y facilidad de uso, reduciendo errores de entrada manual y haciendo el proceso mucho más intuitivo.

![Imagen](gestion.png)

**Gestión de Cuentas Bancarias y Métodos de Pago**

Los usuarios pueden configurar sus cuentas bancarias, registrando datos como el número de cuenta, nombre del banco y saldo. La aplicación permite vincular métodos de pago (como tarjetas o transferencias) para autorizar transacciones automáticas. Se pueden editar o eliminar cuentas y métodos de pago cuando sea necesario.

Tablas involucradas:
- cuentaBancaria: Almacena información detallada de las cuentas bancarias.
- MetodoPago: Detalla los métodos de pago, incluyendo token, fecha de expiración y otros parámetros.
- companies: Gestiona información de empresas relacionadas o clientes corporativos.
- ContactInfoTypes y ContactInfo: Permiten almacenar datos de contacto y otros detalles asociados a cuentas y métodos.

Estas tablas aseguran que toda la información financiera y de contacto esté correctamente vinculada a cada usuario, permitiendo transacciones seguras y verificables. Esta funcionalidad la utilizan aplicaciones como Mint para la gestión de cuentas y la monitorización de saldos. Los usuarios se benefician al tener toda su información financiera consolidada y actualizada, lo que permite transacciones seguras y verificables.

![Imagen](ejecucion.png)

**Ejecución de Pagos y Registro de Transacciones**

Una vez que se confirma un pago (mediante notificaciones SMS o email), la aplicación ejecuta la transacción de forma automática. Se registra cada transacción, capturando datos como el monto, la fecha, el método de pago utilizado y el estado (éxito o fallo). Se mantiene un historial completo para análisis y consulta futura.

Tablas involucradas:
- Pagos: Registra cada pago realizado.
- Transaccion: Almacena detalles ampliados de cada transacción, incluyendo referencias y estado.
- Balances: Controla el saldo y registra los movimientos financieros asociados.
- Notificacion: Gestiona el envío de recordatorios y confirmaciones de pago.

Este conjunto de tablas permite un seguimiento detallado de todas las transacciones, garantizando que cada pago se ejecute y se registre correctamente para futuros análisis y auditorías. Esta funcionalidad la utilizan aplicaciones como Braintree Payments, que ofrecen un sistema robusto para procesar pagos y mantener un historial detallado de transacciones. Los usuarios se benefician al contar con un registro transparente de sus operaciones, lo que facilita el seguimiento y la resolución de cualquier inconveniente.

![Imagen](monetizacion.jpeg)

**Planes y Monetización**

La aplicación debe ofrecer una opción gratuita que permita un pago único al mes. Además, se deben ofrecer planes de suscripción escalables basados en la cantidad de pagos y transferencias mensuales que el usuario requiera. El sistema gestionará de forma automática la facturación y la renovación de estas suscripciones.

Tablas involucradas:
- Suscripcion: Define los planes disponibles en la aplicación, incluyendo descripciones y otros detalles relevantes.
- FeaturePerPlan: Especifica las características adicionales que se incluyen en cada plan, permitiendo diferenciar la oferta en función del nivel de servicio.
- PlanPrices: Detalla el precio, la periodicidad (mensual, anual, etc.) y la vigencia de cada plan de suscripción.
- PlanPerPerson: Relaciona el plan de suscripción con cada usuario, permitiendo saber qué plan ha seleccionado cada cliente.
- PersonPlanLimits: Establece restricciones específicas, como la cantidad máxima de pagos o transferencias mensuales que se permiten en cada plan.

![Imagen](recordatorios.png)

**Programación y Recordatorios**

La aplicación programa la ejecución de pagos según la recurrencia definida (diaria, semanal, mensual, etc.) y envía recordatorios para confirmar los pagos. Los recordatorios se gestionan mediante notificaciones que se envían al usuario, garantizando que no se omitan transacciones importantes.

Tablas involucradas:
- Schedules: Configura la recurrencia y el número de repeticiones.
- Schedule: Registra los detalles de cada ejecución programada, como la fecha base y la próxima ejecución.
- pagoProgramado: Vincula la programación con la ejecución de pagos, relacionando montos y métodos de pago.
- Notificacion: Gestiona el envío y registro de notificaciones y recordatorios.

![Imagen](api.png)

**Integración con APIs Externas y Gestión de Logs**

La aplicación se integra con APIs externas para procesar pagos y enviar SMS, lo que permite automatizar la ejecución de transacciones. Además, se registra cada evento y error en un sistema de logs que facilita la auditoría y el monitoreo del sistema.

Tablas involucradas:
- APIExterna: Configura y gestiona la conexión con APIs de terceros (definiendo endpoints, tokens, etc.).
- Services: Lista y detalla los servicios de pago y sus parámetros.
- LogTypes: Clasifica los tipos de logs generados.
- LogSources: Registra la fuente de cada evento o error.
- LogSeverity: Define la gravedad de los logs.
- Logs: Almacena el registro completo de eventos y errores para auditoría.

![Imagen](internacional.png)

**Soporte Internacional y Datos Complementarios**

Para adaptarse a un mercado global, Payment Assistant incorpora soporte para diferentes monedas, tasas de cambio, idiomas y países. Esto permite que la aplicación ajuste los formatos, precios y la experiencia de usuario de acuerdo con la región.

Tablas involucradas:
- Moneda: Define las monedas utilizadas en el sistema.
- tasaCambio: Registra las tasas de cambio entre las diferentes monedas.
- TranslationLanguage: Almacena información sobre idiomas para la localización.
- Countries: Relaciona países con la moneda y el idioma correspondiente.
- companies: Gestiona información de empresas relacionadas, ya sean clientes o entidades colaboradoras.

![Imagen](transcription.png)

**Otros Datos Complementarios**

Algunas tablas adicionales aseguran una clasificación más fina de las transacciones y facilitan el análisis de datos.

Tablas involucradas:
- TransSubTypes: Clasifica subtipos de transacciones para un análisis más detallado.
- TransType: Registra los tipos generales de transacciones que se pueden realizar.
- VoiceTranscription: Además de lo mencionado, refuerza el análisis de los comandos de voz para futuras mejoras.

