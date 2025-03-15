**Lista de entidades**

**Usuarios:**

-   Firstname

-   Password

-   Lastname

-   createAt (Registra la fecha y hora del momento de la creación del
    usuario. "2025-14-03 00:00:00")

-   lastupdate

**roles:**

-   rolName (nombre del rol: "administrador", "usuario", etc)

-   description (detalles o descripcion de las funciones y
    responsabilidades del rol. "Administrar usuarios y configurar
    ajustes generales")

-   lastupdate (marca el último momento en el que se modificó el
    registro de rol."2025-14-03 12:00:00")

**users_roles:**

-   lastupdate (Registra la fecha y hora de la última modificación en la
    asignación de un rol a un usuario. "2025-15-03 00:00:00")

**permissions:**

-   permissionName (Es el nombre descriptivo del permiso para
    identificar cuál es la acción que se autoriza. "Crear usuario")

-   description (Explicación un poco más detallada del permiso. "Permite
    al usuario registrar nuevos usuarios en el sistema")

-   code (Identificador corto y único del permiso, puede ser utilizado
    en el código fuente. "USR_CREATE")

-   lastupdate (Registra la fecha y hora en la que se realizó la última
    modificación al registro de permiso. "2025-16-03 02:10:01")

**rolepermissions:**

-   lastupdate (Registra la fecha y hora de la última modificación en la
    asignación de un permiso a un rol. " 2025-16-03 02:11:00")

**ContactInfo:**

-   value

-   isPrincipal (Indica con un 1 si esta información del usuario es la
    principal que tiene registrada, con un 0 si no lo es. Puede tener
    registrado un número de teléfono, un email, etc)

-   lastupdate (Fecha y hora en la que se realizó la última modificación
    en este registro)

-   checksum (Almacena un valor hash para verificar la integridad de los
    datos. Detecta modificaciones no autorizadas o errores)

-   ownerTipo (Especifica el tipo de identidad a la que pertenece, un
    "Usuario" una "Empresa", etc)

-   ownerID (Almacena el identificador de la identidad a la que
    pertenece el contacto. Si la identidad es "Usuario", el ownerID
    corresponderá al userid del usuario)

**ContactInfoTypes:**

-   name

**Schedules:**

-   name

-   recurrence_type

-   recurrence_value (Almacena un valor númerico que, en conjunto con el
    recurrence_type, define el intervalo de ejecuciones. Por ejemplo
    para definir un intervalo de 3 días, en este campo se guarda el
    número 3, en recurrence_type se guarda "días"

-   repetitions

-   endDate

**Schedule**

-   baseDate

-   last_exec_datetime

-   next_exec_datetime

-   datePart

**Notificacion** (Registra y hace un seguimiento de las notificaciones
que se deben enviar a los usuarios)**:**

-   tipo (Define el tipo de notificación que se envía. "SMS, "email",
    etc)

-   mensaje (Contiene el texto o conetenido del mensaje que se envía en
    la notificación. "Su fecha de pago se acerca")

-   fechaEnvio (Registra la fecha y hora en la que está programada la
    notificación)

-   estado (Indica el estado actual de la notificación, ya sea
    "enviado", "fallido" o "pendiente")

-   lastupdate (Registra la fecha y hora de la última modificación al
    registro de la notificación)

**UserSettings** (Almacena preferencias o configuraciones específicas
para cada usuario)**:**

-   setting_key (Almacena la clave o el nombre del ajuste. "Idioma",
    "Tema", etc)

-   setting value (Guarda el valor correspondiente a la clave. Por
    ejemplo "ES" para idioma español, "Oscuro" para el tema, etc)

-   lastupdate (Registra la fecha y hora de la última modificación de la
    configuración)

**Moneda** (Registra las moendas que se emplean en las transacciones del
sistema)**:**

-   simbolo (Almacena el símbolo de la moneda. "$", "€", "₡", etc)

-   acronym (Guarda la abreviatura o el código corto de la moneda.
    "USD", "EUR", "CRC", etc)

**Countries:**

-   countryName (Almacena el nombre completo del país)

-   languajeID (Especifica el idioma principal u oficial del país)

**TranslationLanguaje:**

-   code (Almacena el código corto que representa el idioma. "ES", "EN",
    etc)

-   culture (Guarda información cultural relacionada con el idioma)

-   name (Almacena el nombre completo del idioma. "English", "Español",
    etc)

-   last_update (Registra la fecha y hora de la última modificación del
    registro del lenguaje de traducción)

**VoiceTranscription** (Almacena la transcripción generado a partir de
las grabaciones de voz de los usuarios)**:**

-   transcription_text (Almacena el texto resultante de convertir el
    audio del usuario en texto)

-   original_audio_reference (Guarda una referencia al audio original
    que se transcribió)}

-   lastupdate (Registra la fecha y hora de la última actualización del
    registro de transcripción)

**PlanPerPerson:**

-   enable

-   adquisition

**FeaturePerPlan:**

-   value

-   enabled

**PlanPrices:**

-   amount

-   recurrencyType

-   postTime

-   endDate

-   current

**MetodoPago:**

-   token (Almacena de forma segura el token que representa las
    credenciales o datos sensibles del método de pago, en formato
    binario)

-   expirationdate (Registra la fecha límite de validez del token)

-   checksum: (Guarda un valor hash para verificar la integridad del
    token)

-   lastupdate: (Registra la fehca y hora de cuándo se actualizó por
    última vez la información del método de pago)

-   iban (Contiene el número IBAN para identificar la cuenta bancaria
    asociada. "GB33BUKB20201555555555")

-   swift (Almacena el código SWIFT correspondiente al banco emisor.
    "BUKBGB22")

-   refreshToken (Guarda un token alternativo para renovar el acceso sin
    solicitar credenciales de nuevo)

-   detalles (Proporciona información adicional sobre el método, en
    formato JSON )

**Services:**

-   servicename: (Define el nombre del servicio que se gestiona. "Pago
    de Luz")

-   montofijo (Establece un monto fijo relacionado con el servicio, si
    aplica)

-   parametrosPago **(**Permite guardar parámetros adicionales en
    formato JSON, para configurar detalles específicos del servicio)

**Suscripcion:**

-   description

-   logoURL

**pagoProgramado:**

-   monto (Registra el monto que se debe pagar en la ejecución
    programada)

-   enabled (Indica si el pago programado está activo (1) o desactivado
    (0))

-   checksum (Almacena un valor hash para garantizar la integridad de
    los datos del pago)

-   description (Ofrece detalles adicionales sobre el pago programado.
    "Pago mensual de servicio de luz")

-   scheduleDetailID (Identifica el detalle de la programación que
    determina cuándo se ejecuta el pago)

**Proveedor:**
• proveedorname (Almacena el nombre del proveedor. "Banco Nacional")
• tipo (Especifica el tipo o categoría del proveedor. "banco")
• lastupdate (Registra la fecha y hora de la última modificación del
registro del proveedor)
• sitioWeb (Guarda la dirección URL del sitio web del proveedor.
"<http://banconacional.com>")
• config (Contiene configuraciones adicionales en formato JSON)
• datosFiscales (Almacena información fiscal o tributaria del proveedor.
"RUC 123456789")

**tasaCambio (Almacena las tasas de cambio entre dos monedas):**
• tasa (Indica el valor de la tasa de cambio entre dos monedas. 0.85)
• fechaActualizacion (Registra la fecha y hora en que se actualizó la tasa) 
• bit (Actúa como indicador de si se encuentra activo (1) o inactivo (0)) 
• tasaCambiocol (Puede almacenar información adicional o un comentario sobre la tasa. "EUR")
• monedaOrigen (Almacena el identificador de la moneda de origen para la tasa) 
• monedaDestino (Almacena el identificador de la moneda destino para la tasa)

**Transaccion:** 
• amount 
• description 
• trans_datetime 
• postTime 
• refNumber
• fechaProxReintento (Especifica cuándo se programará el próximo intento en caso de fallo) 
• lastupdate (Registra la última fecha en que se modificó la transacción) 
• exchangeRate 
• checksum 

**APIExterna (Guarda la información de integración con los servicios externos):** 
• tipo (Indica el tipo de API externa. "bancaria") 
• endpoint (Almacena la URL del endpoint de la API. "<https://api.banco.com>") 
• tokenAcceso (Guarda el token de acceso en formato binario para conectarse a la API) 
• checksum (Almacena un hash para verificar la integridad del token de acceso) 
• configuracion (Contiene parámetros de configuración adicionales en formato JSON) 
• config (Almacena configuraciones complementarias en formato JSON, si es necesario) 
• key (Guarda la llave de la API en formato binario) 
• secret (Almacena el secreto de la API en formato binario para mayor seguridad) 
• name (Proporciona un nombre descriptivo para la API. "API Banco Nacional")

**LogTypes:**
• name
• ref1Desc (Describe la primera referencia que se utiliza en los logs."Código de error")
• val1Desc (Proporciona un ejemplo o valor esperado para la primera
referencia. "500")
• val2Desc (Proporciona información adicional para una segunda
referencia. "Severidad alta")
• last_update (Indica cuándo se actualizó por última vez el registro)

**LogSources:**
• name (Indica el origen o módulo que genera los logs. "Payment
Module")
• last_update (Registra la última actualización de la información del
origen)

**LogSeverity:**
• name
• last_update (Registra la última actualización del registro de
severidad)

**Logs:**
• description
• postTime
• computer
• username
• trace
• referenceID1
• referenceID2
• value1
• value2
• checksum
• last_update (Indica la última fecha de actualización del registro)

**Pagos:**
• monto
• actualMonto
• result
• auth
• referencia
• changeToken
• description
• error
• fecha
• checksum

**Balances:**
• balance
• lastBalance
• freeze_amount
• last_update
• checksum

**TransSubTypes:**
• name
• last_update (Registra cuándo se actualizó por última vez la
información del subtipo)

**TransType:**
• name
• last_update (Registra la fecha de la última actualización de este
tipo)

**PlanFeatures:**
• description
• enabled
• datatype

**PersonPlanLimits:**
• limit

**AI_Interaction** (Almacena las interacciones con el sistema de
inteligencia artificial)**
• command_extracted (Almacena el comando textual extraído de la entrada
de voz. "Pagar factura")
• model_version (Indica la versión del modelo de IA utilizado para
interpretar el comando. "v1.2")
• response_generated (Guarda la respuesta generada por el sistema en
respuesta al comando. "Pago procesado")
• lastupdate (Registra la última actualización de la interacción)
