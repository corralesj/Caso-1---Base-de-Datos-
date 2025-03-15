# **Lista de Entidades**  

## **Usuarios**  
- **Firstname**  
- **Password**  
- **Lastname**  
- **createAt** (Registra la fecha y hora del momento de la creación del usuario. `"2025-14-03 00:00:00"`)  
- **lastupdate**  

## **Roles**  
- **rolName** (nombre del rol: `"administrador"`, `"usuario"`, etc)  
- **description** (Detalles o descripción de las funciones y responsabilidades del rol. `"Administrar usuarios y configurar ajustes generales"`)  
- **lastupdate** (Marca el último momento en el que se modificó el registro de rol. `"2025-14-03 12:00:00"`)  

## **Users_roles**  
- **lastupdate** (Registra la fecha y hora de la última modificación en la asignación de un rol a un usuario. `"2025-15-03 00:00:00"`)  

## **Permissions**  
- **permissionName** (Es el nombre descriptivo del permiso para identificar cuál es la acción que se autoriza. `"Crear usuario"`)  
- **description** (Explicación más detallada del permiso. `"Permite al usuario registrar nuevos usuarios en el sistema"`)  
- **code** (Identificador corto y único del permiso, puede ser utilizado en el código fuente. `"USR_CREATE"`)  
- **lastupdate** (Registra la fecha y hora de la última modificación al registro de permiso. `"2025-16-03 02:10:01"`)  

## **RolePermissions**  
- **lastupdate** (Registra la fecha y hora de la última modificación en la asignación de un permiso a un rol. `"2025-16-03 02:11:00"`)  

## **ContactInfo**  
- **value**  
- **isPrincipal** (Indica con un `1` si esta información del usuario es la principal que tiene registrada, con un `0` si no lo es. Puede ser un número de teléfono, un email, etc.)  
- **lastupdate** (Fecha y hora en la que se realizó la última modificación en este registro)  
- **checksum** (Almacena un valor hash para verificar la integridad de los datos y detectar modificaciones no autorizadas)  
- **ownerTipo** (Especifica el tipo de identidad a la que pertenece: `"Usuario"`, `"Empresa"`, etc.)  
- **ownerID** (Almacena el identificador de la identidad a la que pertenece el contacto)  

## **ContactInfoTypes**  
- **name**  

## **Schedules**  
- **name**  
- **recurrence_type**  
- **recurrence_value** (Define el intervalo de ejecuciones en conjunto con `recurrence_type`. Por ejemplo, para definir un intervalo de `3 días`, este campo guarda el número `3` y `recurrence_type` almacena `"días"`)  
- **repetitions**  
- **endDate**  

## **Schedule**  
- **baseDate**  
- **last_exec_datetime**  
- **next_exec_datetime**  
- **datePart**  

## **Notificacion** *(Registra y hace un seguimiento de las notificaciones que se deben enviar a los usuarios)*  
- **tipo** (Define el tipo de notificación que se envía: `"SMS"`, `"email"`, etc.)  
- **mensaje** (Contiene el contenido del mensaje enviado en la notificación. `"Su fecha de pago se acerca"`)  
- **fechaEnvio** (Registra la fecha y hora en la que está programada la notificación)  
- **estado** (Indica el estado actual de la notificación: `"enviado"`, `"fallido"`, `"pendiente"`)  
- **lastupdate** (Registra la fecha y hora de la última modificación al registro de la notificación)  

## **UserSettings** *(Almacena preferencias o configuraciones específicas para cada usuario)*  
- **setting_key** (`"Idioma"`, `"Tema"`, etc.)  
- **setting_value** (Valor correspondiente a la clave. Ejemplo: `"ES"` para idioma español, `"Oscuro"` para el tema)  
- **lastupdate**  

## **Moneda** *(Registra las monedas utilizadas en el sistema)*  
- **simbolo** (`"$"`, `"€"`, `"₡"`, etc.)  
- **acronym** (`"USD"`, `"EUR"`, `"CRC"`, etc.)  

## **Countries**  
- **countryName** (Nombre completo del país)  
- **languajeID** (Idioma principal u oficial del país)  

## **TranslationLanguaje**  
- **code** (`"ES"`, `"EN"`, etc.)  
- **culture** (Información cultural relacionada con el idioma)  
- **name** (Nombre completo del idioma: `"English"`, `"Español"`)  
- **last_update**  

## **VoiceTranscription** *(Almacena la transcripción generada a partir de grabaciones de voz de los usuarios)*  
- **transcription_text** (Texto resultante de la conversión de audio a texto)  
- **original_audio_reference** (Referencia al audio original transcrito)  
- **lastupdate**  

## **PlanPerPerson**  
- **enable**  
- **adquisition**  

## **FeaturePerPlan**  
- **value**  
- **enabled**  

## **PlanPrices**  
- **amount**  
- **recurrencyType**  
- **postTime**  
- **endDate**  
- **current**  

## **MetodoPago**  
- **token** (Token seguro que representa credenciales del método de pago en formato binario)  
- **expirationdate**  
- **checksum**  
- **lastupdate**  
- **iban** (Número IBAN de la cuenta bancaria asociada)  
- **swift** (Código SWIFT del banco emisor)  
- **refreshToken**  
- **detalles** (Información adicional en formato JSON)  

## **Services**  
- **servicename** (`"Pago de Luz"`)  
- **montofijo**  
- **parametrosPago** (JSON con detalles del servicio)  

## **Suscripcion**  
- **description**  
- **logoURL**  

## **PagoProgramado**  
- **monto**  
- **enabled**  
- **checksum**  
- **description**  
- **scheduleDetailID**  

## **Proveedor**  
- **proveedorname** (`"Banco Nacional"`)  
- **tipo** (`"banco"`)  
- **lastupdate**  
- **sitioWeb** (`"http://banconacional.com"`)  
- **config** (Configuraciones en formato JSON)  
- **datosFiscales** (`"RUC 123456789"`)  

## **TasaCambio** *(Registra tasas de cambio entre monedas)*  
- **tasa** (Valor de la tasa de cambio, ejemplo: `0.85`)  
- **fechaActualizacion**  
- **bit** (Indica si está activa (`1`) o inactiva (`0`))  
- **monedaOrigen**  
- **monedaDestino**  

## **Transaccion**  
- **amount**  
- **description**  
- **trans_datetime**  
- **postTime**  
- **refNumber**  
- **fechaProxReintento**  
- **lastupdate**  
- **exchangeRate**  
- **checksum**  

## **APIExterna** *(Guarda información de integración con servicios externos)*  
- **tipo** (`"bancaria"`)  
- **endpoint**  
- **tokenAcceso**  
- **checksum**  
- **configuracion**  
- **config**  
- **key**  
- **secret**  
- **name** (`"API Banco Nacional"`)  

---

Con esta estructura, tu documentación en Markdown se verá mucho más clara y organizada en GitHub. 🚀
