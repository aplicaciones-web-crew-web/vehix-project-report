# Capítulo III: Requirements Specification
## 3.1. To-Be Scenario Mapping
En esta sección se abordará el To-Be Scenario Mapping para cada uno de las User Persona, en el cual describiremos en filas Phases, Doing, Thinking y Feeling.

**Segmento 1: Propietarios de vehículos urbanos que desean prolongar la vida útil de su auto personal.**

En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Uso diaria del auto, notan un comportamiento extraño, problema evidente y post-reparación. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, se recata el análisis en tiempo real del vehículo, como actividad principal.
![to-be-scenario-mapping-segment-1](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-1.jpg)

**Segmento 2: Conductores independientes que generan ingresos con su vehículo.**

En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Inicio de jornada laboral, Durante el trabajo, Falla crítica o emergencia y Evaluación del gasto. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, se recata la ayuda activa de la aplicación para poder derivar a mecánicos cercanos y a la vez el diagnóstico rápido para manejar sin preocupación.
![to-be-scenario-mapping-segment-2](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-2.jpg)

**Segmento 3: Mecánicos o técnicos automotrices que desean mejorar sus diagnósticos y comunicación con los clientes.**

En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Cliente llega con una falla, Diagnóstico, Datos útiles y Registro del caso. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, el diagnóstico rápido, ahorro de tiempo y lenguage técnico.
![to-be-scenario-mapping-segment-3](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-3.jpg)

## 3.2. User Stories
En esta sección el equipo redacta la definición y la elaboración de los User Stories (Como, Quiero y Para). Las historias de usuario son un recurso clave para construir software y diseñar proyectos con enfoque en las necesidades y experiencias de las personas. De manera que se a usado la sintaxis Gherkin para los tests de aceptación.

| Epic /Story ID | Título | Descripción | Criterios de aceptación | Relacionado con (Epic ID) |
| :---- | :---- | ----- | ----- | ----- |
| EP01 | Gestión de usuarios |**Como** conductor independiente **quiero** crear una cuenta en la aplicación **para** asegurar mis datos y registros| \- | \- |
| EP02 | Información de la plataforma (Landing Page) |**Como** visitante del segmento de propietarios de vehículos urbanos **quiero** información detallada y precisa de lo que ofrece el sitio web **para** poder encontrar información necesaria. | \- | \- |
| EP03 | Diagnóstico y mantenimiento vehicular | **Como** conductor independiente **quiero** realizar un estudio de mi vehículo en tiempo real y rápido **para** prevenir mantener mi carro en buen estado. | \- | \- |
| EP04 | Conectividad del vehículo | **Como** propietario de vehículos urbanos **quiero** conectar mi vehículo por medio de la aplicación **para** enterarme de los datos de este | \- | \- |
| EP05 | Gestión de mecánicos | **Como** mecánico automotriz **quiero** quiero examinar vehículos por la aplicación **para** obtener un diagnóstico rápido y eficiente| \- | \- |
| EP05 | Suscripciones y pagos | **Como** conductor independiente **quiero** suscribirme a su aplicación **para** obtener acceso completo a todas las funciones disponibles | \- | \- |
| EP07 | Funcionalidades API RESTFUL (Developer) | **Como** desarrollador **quiero** manejar la aplicación mediante APIrest **para** controlar los datos y el flujo de este por toda la solución.  | \- | \- |
| EP08 | Biblioteca automotriz | **Como** mecánico automotriz **quiero** tener un centro de conocmiento integral dentro de la aplicación **para** mantenerme continuamente informado sobre la tecnología y práctica automotrices.  | \- | \- |
| US01 | Registro de cuenta | **Como** propietario de vehículo urbano, **quiero** registrarme **para** acceder a las funcionalidades de la aplicación | **Escenario 1: Registro exitoso Dado** que el propietario de vehículo urbano ingresa información válida, como: nombre, apellidos, dni, correo personal, contraseña, número de celular y género,**Cuando** solicita el registro, **Entonces** su cuenta se crea correctamente y puede acceder a la plataforma. **Escenario 2: Error en el registro Dado** que el propietario de vehículo urbano ingresa información incompleta o incorrecta en los campos de nombre, apellidos, dni, correo personal, contraseña, número de celular, dni y/o género, **Cuando** solicita el registro, **Entonces** el sistema le notifica sobre el error y le permite corregirlo.| EP01 |
| US02 | Búsqueda de Contenido | **Como** visitante del segmento de mecánicos automotrices **quiero** ver contenido específico en el sistema **para** mayor claridad y rapidez al acceder a la información. | **Escenario 1: Acceso a las secciones Dado** que el visitante del segmento de mecánicos automotrices busca una sección en específico **Cuando** elige la sección, **Entonces** el sistema muestra la información correspondiente. **Escenario 2: Búsqueda sin resultados Dado que** que el visitante del segmento de mecánicos automotrices se encuentra en la página, **Cuando** busca una sección específica **Y** no se encuentra **Entonces** el sistema informa la falta de información.  | EP02 |
| US03 | Lista de beneficios | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** ver una lista de todos los beneficios **para** poder conocer las ventajas que se ofrecen. | **Escenario 1: Visualización exitosa de beneficios Dado** que el visitante del segmento de propietarios de vehículos urbanos ingresa a la landing page **Cuando** solicita los beneficios **Entonces** la landing page muestra una lista de todos los beneficios activos  **Escenario 2: No hay beneficios activos para mostrar Dado que** que el visitante del segmento de propietarios de vehículos urbanos ingresa a la landing page **Cuando** no existen beneficios activos **Entonces** la landing page informa que no hay beneficios disponibles en este momento  | EP02 |
| US04 | Inicio de sesión | **Como** propietario de vehículo urbano **quiero** iniciar sesión en la aplicación **para** usar todas las funcionalidades de esta. | **Escenario 1: Inicio de sesión exitoso Dado** que el propietario de vehículo urbano ingresa credenciales válidas de DNI y contraseña **Cuando** solicita acceder a la aplicación, **Entonces** ingresa a la aplicacón sin errores. **Escenario 2: Credenciales inválidas Dado** que el propietario de vehículo urbano ingresa datos incorrectos de DNI y/o contraseña, **Cuando** intenta ingresar a la aplicación, **Entonces** recibe un aviso y puede volver a intentarlo. **Escenario 3: Falta de credeneciales Dato que** el propietario de vehículo urbano ingresa uno o ningún DNI o contraseña , **Cuando** solicita acceder a la aplicación, **Entonces** el sistema informe la falta de credencial.| EP01 |
| US05 | Notificaciones de alerta del vehículo en tiempo real | **Como** propietario de vehículo urbano, **quiero** recibir alerta inmediatas sobre el estado o fallos de mi vehículo **para** evitar daños mayores o situaciones de riesgo. | **Escenario 1: Generación de alerta por evento crístico del vehículo Dado que** el propietario de vehículo urbano está conectado correctamente al vehículo, **Cuando** el sistema procesa la información de una anomalía crítica **Entonces** el sistema genera una notificación de alerta **E** indica la magnitud del defecto. **Escenario 2: Alerta por acción inadedcuada del usuario que afecta al vehículo Dado** que el propietario realiza una acción que afecta el estado del vehículo,  **Cuando** el sistema registra el estado del vehículo **Entonces** el sistema genera una notificacion de alerta si el estado actual es crítico. **Escenario 3: Historial de alertas Dado** que el propietario de vehiculos urbanos visualiza las alertas,  **Cuando** solicita revisar todas las alerta **Entonces** el sistema muestra la lista completa de alertas del vehículo. | EP03 |
| US06 | Previsión de problemas |  **Como** conductor independiente **quiero** acceder a la informacion relevante sobre los problemas a futuro de mi vehículo **para** cuidar de mejor manera mi vehículo. | **Escenario 1:  Diagnóstico previo para la previsión de problemas del vehículo Dado** que el conductor independiente ingresa a la aplicación **Y** realiza un diagnóstico **Cuando** solicita ver los problemas o fallas a futuro de su vehículo **Entonces** el sistema muestra indicacores relevantes del pronóstico considerando los 7 sistemas principales del vehiuclo **Y** las probabilidades de falla en cada uno **Escenario 2: No se realiza diagnóstico previo para la previsión de problemas del vehículo Dado** que el conductor independiente ingresa a la aplicacion **Y** no realiza un diagnóstico **Cuando** solicita ver los problemas o fallas a futuro de su vehículo **Entonces** el sistema informa que no hay datos disponibles **Y** le permite escanear el vehículo. | EP03 |
| US07 | Diagnóstico vehicular | **Como** mecánico automotriz **quiero** obtener un diagnóstico veraz del estado de mi vehículo **para** atender cualquier problema y considerar reparaciones o mantenimientos menos costosos. | **Escenario 1: Ejecución Exitosa de un Diagnóstico General Dado que** el mecánico automotriz está conectado a un vehículo **Cuando** el mecánico automotriz solicita el escaneo del vehículo, **Entonces** el sistema muestra los errores del vehículo en lenguage simple y técnico, malas prácticas de manejo, nivel de urgencia **Y** consejos para solucionarlo. **Escenario 2: Ejecución Fallida de un Diagnóstico General Dado que** el mecánico automotriz no está conectado con un vehículo **Cuando** el mecánico automotriz solicita el escaneo del vehículo, **Entonces** el sistema muestra el error de conexión con el vehículo **Y** le permite buscar vehículos por bluetooth.  | EP03 |
| US08 | Cierre de sesión | **Como** propietario de vehículo urbano, **quiero** cerrar mi sesión activa **para** poder proteger mi cuenta y finalizar mi interacción con el sistema de forma segura | **Escenario 1: Cierre exitoso Dado** que el propietario del vehículo urbano está con una sesión activa, **Cuando** solicita cerrar su sesión, **Entonces** el sistema finaliza su sesión actual **Y** lo redirige al estado de inicio de sesión. **Escenario 2: Intento de acceso Posterior a cerrar sesión Dado que** el propietario del vehículo urbano cierra su sesión **Cuando** intenta acceder a una función **Entonces** el sistema impide el acceso a esa funcionalidad **Y** solicita que inicie sesión nuevamente.  | EP01 |
| US09 | Historial de vehículos | **Como** mecánico automotriz **quiero** ver un historial de vehículos previamente registrados **para** consultar información sobre ellos y gestionar mis datos de forma efectiva. | **Escenario 1: Visualización del Historial de Vehículos con plan PRO Dado** que el mecánico automotriz registra uno o más vehículos con el plan PRO **Cuando** solicita ver el historial de vehiculos registrados, **Entonces** el sistema muestra una lista de todos los vehículos registrados con el nombre del vehículo **Escenario 2: Visualización del Historial de Vehículos con plan STANDARD Dado Dado** que el mecánico automotriz tiene el plan standard **Y** registra un vehículo, **Cuando** solicita la lista de vehículos, **Entonces** la aplicación muestra el único vehículo **Y** no se le permite añadir más vehículos. **Escenario 3: Historial de vehículos vacío Dado** que el mecánico automotriz tiene el plan PRO o STANDARD, **Cuando** solicite la lista de vehículos, **Entonces** se le informa que debe registrar vehículos **Y** se le permite registrar.  | EP03 |
| US10 | Conexión bluetooth | **Como** mecánico automotriz **quiero** conectarme a mi vehículo de manera rápida y precisa con bluetooth **para** tener información de mi vehículo en todo lugar y momento. | **Escenario 1: Transmisión de datos correctos Dado** que el mecánico automotriz instala en el puerto OBD2 del vehiculo, el adaptador de diagnóstico VEHIX, **E** incia sesión correctamente en la aplicación **Cuando** el sistema detecta el vehículo y se intenta la conexión, **Entonces** el sistema establece una conexión **Y** muestra la opción de registrar el vehículo. **Escenario 2: Transmisión de datos incorrecto Dado** que el mecánico automotriz instala de manera errónea el adaptador diagnóstico VEHIX **E** intenta conectar a este por la aplicación por medio de la aplicación **Cuando** el mecanico automotriz activa el bluetooh **Y** no se visualize ningún adaptador en pantalla **Entonces** la aplicación muestra el video de instalación y la guía rapida de instalación. | EP04 |
| US11 | Ingresar nuevo vehículo | **Como** propietario de vehículo urbano **quiero** registrar mi vehículo **para** poder tener una lista ordenada de mis vehículos. | **Escenario 1: Registro exitoso de vehículo Dado** que el propietario de vehículo urbano conecta de manera exitosa su vehículo con la aplicación **Cuando** el propietario de vehiculo urbano ingresa información válida y completa del vehículo, como: nombre del vehículo, modelo, kilometraje y año de producción **Entonces** el sistema guarda el vehículo en la lista de vehículos. **Escenario 2: Registro fallido de vehículo Dado** que el propietario de vehículo urbano conecta de manera exitosa su vehículo con la aplicación **Cuando** el propietario de vehiculo urbano ingresa información inválida o imcompleta del vehículo, como: nombre del vehículo, modelo, kilometraje y año de producción **Entonces** el sistema guarda informa que debe ingresar correctamente los datos.  **Escenario 3: Bloqueo de registro Dado** que el propietario de vehículo urbano registra un vehiculo y tiene el plan STANDARD **Cuando** intente registrar otro vehículo. **Entonces** la aplicación mostrará que debe de adquirir el plan PRO. | EP01 |
| US12 | Localizar un taller automotriz cercano | **Como** conductor independiente, **quiero** localizar un taller mecánico cercano y confiable, **para** realizar arreglar o revisar mi vehículo | **Escenario 1: Mecánicos disponibles en la zona Dado** el conductor independiente ingresa a la aplicación **Y** realiza un diagnóstico, **Cuando** este solicita ayuda **Y** active el gps **Entonces** se le muestran opciones de mecánicos cercanos, certificados y expertos en su falla. **Escenario 2: No hay mecánicos cercanos Dado** el conductor independiente ingresa a la aplicación **Y** realiza un diagnóstico, **Cuando** solicita ayuda **Y** activa el gps **Entonces** se le informa que no hay resultados de mecánicos cercanos, certificados y expertos en su falla. **Escenario 3: No activa el GPS Dado** que el conductor independiente ingresa a la aplicación **Y** realiza un diagnóstico **Cuando** solicita ayuda **Y** no activa el GPS **Entonces** no se visualizan mecánicos cercanos, certificados y expertos en su falla.  | EP05 |
| US13 | Auditoría de fallas | **Como** conductor independiente, **quiero** ver la descripción y controlar el estado de la falla que tiene mi vehículo, **para** tomar medidas de mantenimiento y guardarlas en la aplicación. | **Escenario 1: Falla identificada Dado** que el sistema ha detectado un error o se registra un escaneo diagnóstico, **Cuando** el conductor independiente accede a la auditoría de fallas, **Entonces** se muestran las fallas con título referencial, motivo **Y** permite cambiar el estado de la falla entre "solucionado" y "pendiente". **Escenario 2: Vehículo en buen estado Dado** que la aplicación no detecta ninguna falla a través del diagnóstico, **Cuando** el conductor independiente ingresa a la auditoría de fallas **Entonces** se le informa que su vehículo está en buen estado | EP03 |
| US14 | Estado de suscripción | **Como** conductor independiente, **quiero** saber que suscripción poseo, **para** verificar mi estado de suscripción. | **Escenario 1: Suscripción activa Dado** que el conductor independiente tiene una suscripción, **Cuando** accede al perfil, **Entonces** se le muestra la fecha de renovación. **Escenario 2: Cambio de suscripción Dado** que la suscripción se encuentra activa **Cuando** el conductor independiente quiere cambiar de plan **Entonces** el sistema le pedirá ingresar número de tarjetas, mes y año de expiracion y codigo de seguridad de la tarjeta. **Escenario 3: Suscripción expirada Dado** que la suscripción se encuentra expirada **Cuando** el conductor independiente ingresa a la aplicación **Entonces** el sistema pide renovar su suscripción solicitandole número, mes y año de expiracion y codigo de seguridad de la tarjeta.| EP06 |
| US15 | Diagnóstico rápido | **Como** conductor independiente **quiero** acceder al diagnóstico rápido de mi vehículo **para** obtener el estado de mi vehiculo de manera rápida y sencilla. | **Escenario 1: Diagnóstico rápido exitoso Dado** que el conductor independiente ingresa a la aplicación **Y** se conecta a un vehículo **Cuando** solicita ver el diagnóstico rápido de su vehículo **Entonces** el sistema muestra indicacores relevantes del pronóstico considerando los 4 sistemas principales del vehiculo, como motor, bateria, frenos y sensores **Y** el estado en cada uno **Escenario 2: Bloqueo de diagnóstico rápido Dado** que el conductor independiente tiene el plan STANDARD **Cuando** solicita ver el diagnóstico rápido de su vehículo **Entonces** el sistema informa que debe de cambiar al plan PRO. | EP03 |
| US16| Fallas y reparaciones | **Como** conductor independiente **quiero** acceder a la informacion de las reparaciones realizadas y fallas constatadas de mi vehículo **para** validar el estado de mi vehículo. | **Escenario 1:  Realiza diagnóstico previo Dado** que el conductor independiente ingresa a la aplicación **Y** realiza un diagnostico previo **Y** el sistema lee fallas **Cuando** solicita ver las reparaciones recientes **Entonces** el sistema muestra las fallas, el nivel de urgencia y el estado de la falla, también el problema solucionado de la reparación, la mejora del vehiculo a causa de la solucion y el día de la reparación.  **Escenario 2:  No realiza diagnóstico previo Dado** que el conductor independiente ingresa a la aplicación **Y** no realiza un diagnostico previo **Cuando** solicita ver las reparaciones recientes **Entonces** el sistema muestra que falta realizar un diagnostico previo. | EP06 |
| TS17 | Obtener el historia técnico del vehículo a través de RESTfulAPI | **Como developer,** **quiero** obtener el historial técnico de un vehículo mediante una API, **para** que esté este disponible para crear funciones para mis aplicaciones. | **Escenario 1: Consulta con identificador válido Dado que** el endpoint "/technical-history" esta disponible **Cuando** el developer realiza una solicitud GET incluyendo el id del vehículo y el id del usuario, **Entonces** el sistema devuelve el historial técnico correspondiente al vehículo con el estatus 200, incluyendo todos los datos del vehiculo.**Escenario 2: Consulta con identificador inválido Dado que** el endpoint "/technical-history" esta disponible **Cuando** el developer realiza una solicitud GET incluyendo un id de vehículo y/o del usuario erróneo, **Entonces** el sistema devuelve una respuesta con el estado 404 Not Found.  | EP07 |
| TS18 | Obtener mecánicos cercanos a través de RESTfulAPI | **Como developer,** **quiero** obtener los mecánicos cercanos mediante una API, **para** que esté este disponible para crear funciones para mis aplicaciones. | **Escenario 1: Obtener Mecánicos Cercanos Exitosamente Dado que** el endpoint "/mecánicos" esta disponible **Cuando** el developer realiza una solicitud GET incluyendo parámetros de latitud y longitud válidos, **Entonces** el sistema devuelve el historial técnico correspondiente al vehículo con el estatus 200 OK, Y el cuerpo de la respuesta incluye un array de respuestas json, donde cada recurso representa un mecánico cercano y contiene los campos nombre, dirección, teléfono de contacto y nombre de taller.**Escenario 2: No se Encuentran Mecánicos Cercanos Dado que** el endpoint "/mecánicos" esta disponible **Cuando** el developer realiza una solicitud GET incluyendo parámetros de litutid y longitud válidos, pero no hay mecánicos dentro del radio de búsqueda configurado, **Entonces** el sistema devuelve una respuesta con el estado 200ok y devuleve un array JSON vacío.  | EP07 |
| TS19 | Agregar Nuevo vehículo a través de RESTfulAPI | **Como** developer, **quiero** registrar un nuevo vehículo  **para** permitir a los usuarios registrar sus vehículos. | **Escenario 1: Registro exitoso del vehículo Dado que** el endpoint "/vehiculos" está disponible **Cuando** se realiza una solicitud POST con los los datos del vehículo (nombre del carro, modelo, kilometraje y año de fabricación), **Entonces** se recibe una respuesta con el status 201, y se incluye un recurso de estudiante en el cuerpo de la respuesta, con un nuevo ID y valores registrado. **Escenario 2: Error de Vehiculos existente Dado que** el endpoint "/vehiculos" está disponible **Cuando** se realiza una solicitud POST con los los datos del vehículo (nombre del carro, modelo, kilometraje y año de fabricación), **Y** el nombre de este se enucentra guardado **Entonces** se recibe una respuesta con el status 400, y se incluye un mensaje haciendo referiancia a la existencia de un vehículo con con el mismo nombre. | EP07 |
| US20 | Ver consumo de combustible | **Como** propietario de vehículo urbano, **quiero** ver mi consumo de combustible promedio, **para** manejar de forma más eficiente. | **Escenario 1: Datos disponibles Dado** que el propietario de vehículo urbano ingresa a la aplicación **Cuando** ingresa un vehículo **Entonces** se visualiza el consumo en porcentaje del combustible. **Escenario 2: Sin registros de consumo Dado** que aún no hay un vehículo registrado **Cuando** el propietario de vehículo urbano accede al perfil para verificar el consumo de gasolina de un vehículo **Entonces** se le indica que no hay registro de vehículo.  | EP03 |
| US21 | Edición de información personal | **Como** conductor independiente, **quiero** poder actualizar mi información personal, **para** mantener mis datos precisos y actualizados en la aplicación | **Escenario 1: Edición exitosa Dado** que el  conductor independiente actualiza sus datos, como: nombre, apellidos, correo, contraseña y número de celular, correctamente, **Cuando** solicita el guardado, **Entonces** el sistema los almacena y refleja los cambios en su perfil. **Escenario 2: Fallo en la edición Dado** que el conductor independiente introducen datos insuficientes, como: nombre, apellidos, correo, contraseña y/o número de celular, **Cuando** solicita guardar, **Entonces** el sistema le informa del error y notifica rellenar los campo faltante  | EP01 |
| US22 | Articulos técnicos | **Como** mecánico automotriz **quiero** acceder y leer documentacion de articulos técnicos relevantes **para** mantenerme informado sobre los avances automotrices y mejorar mis conocimientos. | **Escenario 1: Consulta de contenido disponible con PLAN PRO Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar el material técnico incluyendo como titulo, decripción, contenido y link. **Escenario 2: Consulta de contenido disponible con PLAN STANDARD Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar el material técnico incluyendo como titulo, decripción, contenido y link. | EP08 |
| US23 | Lengüage técnico | **Como** mecánico automotriz **quiero** tener los codigos de error asociados a las fallas **para** identificarlas rapidamente. | **Escenario 1: Visualizar código de error de las fallas del vehículo** **Dado** que el mecánico automotriz posee el PLAN PRO **Cuando** realiza un diagnóstico **Entonces** visualiza las fallas, sus código de error y una descripción de cada uno. **Escenario 2: Bloqueo de código de error de las fallas del vehículo** **Dado** que el mecánico automotriz posee el PLAN STANDARD **Cuando** realiza un diagnóstico **Entonces** no visualiza los código de error y se le informa adquirir el PLAN PRO. | EP05 |
| US24 | Noticias del sector automotriz | **Como** mecánico automotriz **quiero** acceder y leer noticias del sector automotriz **para** saber las noticias en el sector. | **Escenario 1: Consulta de contenido disponible con PLAN PRO Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar las últimas noticias del sector automotriz incluyendo titulo, decripción, contenido y link. **Escenario 2: Consulta de contenido disponible con PLAN STANDARD Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar las últimas noticias del sector automotriz incluyendo titulo, decripción, contenido y link. | EP08 |
| US25 | Avances del sector automotriz | **Como** mecánico automotriz **quiero** acceder y leer sobre los avances y tendencias del sector automotriz **para** mantenerme al día con la evolución de la tecnología y las prácticas en la industria. | **Escenario 1: Consulta de contenido disponible con PLAN PRO Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar los útlimos avances del sector automotriz incluyendo como titulo, decripción, contenido y link. **Escenario 2: Consulta de contenido disponible con PLAN STANDARD Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar las últimas noticias del sector automotriz incluyendo titulo, decripción, contenido y link. | EP08 |
| US26 | Pago de suscripciones | **Como** propietario de vehículo urbano **quiero** pagar la suscripción con mi tarjeta por medio de la aplicación **para** un pago rápido | **Escenario 1: Pago exitoso Dado** que los datos de la tarjeta como: numero de tarjeta, nombre del usuario, appelido del usuario, fecha de expiracion y código de seguridad, **Cuando** el propietario de vehículo urbano procede con el pago, **Entonces** se confirma la suscripción al plan correspondiente. **Escenario 2: Fallo en el pago Dado** que los datos de la tarjeta como: número de tarjeta, nombre y apellido del usuario, fecha de expiración y código de seguridad, no son válidos o no coinciden con el usuario, **Cuando** el propietario de vehículo urbano procede con el pago, **Entonces** el sistema pide corregir los campos. | EP06 |
| US27 | Vida útil del coche | **Como** propietario de vehiculos urbanos **quiero** acceder a la informacion relevante sobre la vida útil de mi vehículo **para** mantener en óptimas condiciones mi vehículo. | **Escenario 1:  Diagnóstico previo del vehículo Dado** que el propietario de vehiculos urbanos ingresa a la aplicación **Y** realiza un diagnóstico **Cuando** solicita ver la vida útil de su vehículo **Entonces** el sistema muestra indicadores del kilometrage, tiempo estimado de vida, y porcentaje de la salud del vehículo. **Escenario 2: No se realiza diagnóstico previo del vehículo Dado** que el propietario de vehiculos urbanos ingresa a la aplicacion **Y** no realiza un diagnóstico **Cuando** solicita ver la vida útil de su vehículo **Entonces** el sistema informa que no hay datos disponibles **Y** le permite escanear el vehículo.  | EP03 |
| US28 | Eliminación de vehículo | **Como** mecánico automotriz **quiero** eliminar un vehículo de mi lista **para** actualizar mis vehículos. | **Escenario 1: Eliminación confirmada Dado** que el mecánico automotriz decide eliminar un vehículo, **Cuando** realiza la solicitud, **Entonces** la aplicación pide confirmación **Y** al aceptar elimina el vehículo. **Escenario 2: Cancelación de la eliminación Dado** que el mecánico automotriz decide eliminar un vehículo, **Cuando** realiza la solicitud, **Entonces** la aplicación pide confirmación **Y** al cancelarlo no elimina el vehículo. | EP01 |
| US29 | Acceso a la Aplicación desde la Página Principal | **Como** visitante del segmento conductores independientes **quiero** ser guiado a la aplicación, **para** usar las funcionalidades disponibles.  | **Escenario 1: Redirección exitosa a la aplicación web Dado** que el visitante del segmento conductores independientes accede a la landing page, **Cuando** indica su intecion de acceder a la aplicación, **Entonces** el sistema lo redirige a la aplicación web principal.**Escenario 1: Redirección para registro de cuenta Dado** que el visitante del segmento conductores independientes accede a la landing page, **Cuando** indica su intencion de registrarse en la aplicación, **Entonces** el sistema lo redirige a la págian de registro de la aplicación.| EP02 |
| US30 | Implementación de testimonios | **Como** visitante del segmento conductores independientes **quiero** visualizar los testimienos de otros usuarios, **para** conocer sus experiencias y generar confianza en el servicio.  | **Escenario 1: Visualización de testimonios existentes Dado** que hay testimonios de usuarios registrados en el sistema, **Cuando** ingresa a la landing page **Entonces** el sistema muestra testimonios de usuarios con nombre, calidad en estrellas y comentario. **Escenario 2: Ausencia de testimonios Dado** que no hay testimonios de usuarios registrados en el sistema, **Cuando** accede a la landing page, **Entonces** el sistema no muestra los testimonios e informa la falta de estos. | EP02 |
| US31 | Crear planes de suscripción | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** ver e informarme de los planes de suscripción **para** poder adquirir uno. | **Escenario 1: Visualización de planes activps Dado** que existen diferentes 2 tipos de suscripciones: STANDARD y PRO, **Cuando** el visitante del segmento de propietarios de vehículos urbanos solicita los planes de suscripción, **Entonces** el sistema muestra las suscripciones, incluyendo título, términos, beneficios y costos.  **Escenario 2: Ausencia de planes Dado** que no existen suscripciones **Cuando** el visitante del segmento de propietarios de vehículos urbanos solicita los planes de suscripción, **Entonces** el sistema muestra la falta de suscripciones.  | EP02 |
| US32 | Guía de conexiones | **Como** propietario de vehículos urbanos **quiero** tener una guía de conexión vehículo-aplicación **para** usar la aplicación sin errores. | **Escenario 1: Visualización Multimedia Dado** que el visitante del segmento de propietarios de vehículos ingresa al sistema, **Cuando** solicita una sincronización con un vehículo, **Entonces** se muestra un video explicativo de la instalación. **Escenario 2: Visualización Textual Dado** que el visitante del segmento de propietarios de vehículos ingresa al sistema, **Cuando** solicita una sincronización con un vehículo, **Entonces** se muestra una lista de pasos enumerados y concisos del proceso de instalación y conexión. | EP02 |
| US33 | Soporte y redes | **Como** visitante del segmento conductores independientes **quiero** poder contactar a soporte **para** resolver mis dudas | **Escenario 1: Envío exitoso de consulta Dado** que el visitante del segmento de conductores independiente ingresa a la landing page, **Cuando** accede a la sección de contacto **Y** escribe, nombre, correo, tema de consulta y un mensaje, **Entonces** se envía la solicitud correctamente. **Escenario 2: Envío fallido de consulta Dado** que el visitante del segmento de conductores independiente ingresa a la landing page, **Cuando** accede a la sección de contacto **Y** escribe de manera incorrecta o no rellena nombre, correo, tema de consulta y/o un mensaje , **Entonces** se le solicita rellenar los campos. | EP02 |
| US34 | Adaptación a diferentes dispositivos | **Como** visitante del segmento de conductores independientes **quiero** visualizar la landing page **para** desde cualquier dispositivo. | **Escenario 1: Adaptación en pantalla móvil Dado** que el visitante del segmento de conductores independientes accede a la landing page desde un dispositivo con un ancho de pantalla inferior o igual a 900px, **Cuando** la página se carga, **Entonces** el sistema distribuye de forma óptima todos los elementos en el ancho disponible. **Escenario 2: Adaptación en pantalla de escritorio Dado** que el visitante del segmento de conductores independientes accede a la landing page desde un dispositivo con un ancho de pantalla superior a 900px, **Cuando** la página se carga, **Entonces** el sistema distribuye de forma óptima todos los elementos en el ancho disponible. | EP02 |
| US35 | Visualización de creadores | **Como** visitante del segmento de conductores independientes **quiero** ver la información sobre los creadores del proyectos **para** conocer al equipo de la aplicación.  | **Escenario 1: Visualización de la ifnromación de los creadores Dado** que se cuenta con una sección de quiénes somos, **Cuando** el visitante del segmento de conductores independientes accede al landign page, **Entonces** el sistema muestra los nombres, perfiles y fotos de los miembros del equipo. **Escenario 2: Ausencia de información de creadores Dado** que no hay información de los creadores registrados en el sistema, **Cuando** accede a la landing page, **Entonces** el sistema no muestra la sección de "Creadores del proyecto"  | EP02 |
| US36 | Soporte Multilingüe | **Como** visitante del segmento de conductores independientes **quiero** poder seleccionar el idioma en el que se muestra el contenido de la aplicación **para** comprender la información proporcionada. | **Escenario 1: Selecciona idioma en español Dado** que la landing page soporta seleccionar el idioma, **Cuando** se solicita la traducción a "español", **Entonces** todo el contenido textual de la landing page se muestra en idioma español. **Escenario 2: Selecciona idioma en inglés Dado** que la landing page soporta seleccionar el idioma, **Cuando** se solicita la traducción a "inglés", **Entonces** todo el contenido textual de la landing page se muestra en idioma inglés. | EP02 |
| US37 | Preguntas frecuentes | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** informarme de preguntas frecuentes **para** validarlo con mis preguntas. | **Escenario 1: Visualización de la sección de preguntas frecuentes Dado que** el visitante del segmento de propietarios de vehículos urbanos solicita las preguntas frecuentes de la aplicació  **Cuando** accede a la sección de preguntas frecuentes, **Entonces** el sistema muestra una lista de preguntas con título de cada una. **Escenario 2: Búsqueda de preguntas específicas Dado que** el visitante del segmento de propietarios de vehículos urbanos solicita una pregunta en específico de la aplicación  **Cuando** accede a la sección de preguntas frecuentes, **Entonces** el sistema muestra aquella que sea relevante **E** incluye título de pregunta y erspuesta.   | EP02 |
| US38 | Desarrollo de vehiculos compatibles | **Como** visitante del segmento de mecánicos automotriz **quiero** saber qué tipo de vehículos son compatibles con la aplicación **para** confirmar si puedo usarla con mi vehículo. | **Escenario 1: Visualización de la lista de vehículos compatibles Dado que** el visitante del segmento de mecánicos ingresa a la landing page, **Cuando** accede a la sección de vehículos compatibles, **Entonces** visualiza una lista clara que incluye marcas, modelos o tipos de vehículos soportados. **Escenario 2: Búsqueda de un Modelo de Vehículo Específico Dado que** el visitante del segmento de mecánicos automotrices explora la sección de vehículos compatibles, **Cuando** ingresa la marca, modelo o año de un vehículo, **Entonces** el sistema muestra si el vehículo es compatible. | EP02 |
| TS39 | Actualizar datos de un vehículo | **Como** developer, **quiero** actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, **para** que pueda mantener actualizada la información registrada en la plataforma.  | **Escenario 1: Actualización exitosa de datos del vehículo Dado que** el developer proporciona datos completos y válidos para actualizar, **Cuando** el developer realiza una solicitud PUT para modificar los datos de un vehículo, **Entonces** el sistema actualiza correctamente la información en la base de datos y confirma el éxito de la operación. **Escenario 2: Error por datos incompletos o erróneos Dado que** los datos enviados por el developer son incompletos o contienen errores de formato, **Cuando** el developer realiza una solicitud PUT para actualizar los datos, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error explicando los problemas detectados.  | EP07 |
| TS40 | Registro Usuario | **Como** developer, **quiero** crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, **para** que pueda permitir el registro de usuarios en la plataforma. | **Escenario 1: Registro exitoso de usuario Dado que** el developer proporciona un nombre, correo electrónico y contraseña válidos, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema crea el nuevo usuario y devuelve su información básica junto con una confirmación de éxito. **Escenario 2: Error por datos duplicados en el registro Dado que** el developer proporciona un correo electrónico que ya está registrado, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error indicando que el correo electrónico ya existe.  | EP07 |
| US41 | Último escaneo | **Como** conductor independiente **quiero** acceder a la informacion del último escaneo de mi vehículo **para** analizar el estado de mi vehículo. | **Escenario 1: Realiza diagnóstico previo Dado** que el conductor independiente ingresa a la aplicación **Y** realiza un diagnóstico **Cuando** solicita ver la informacion del útlimo escaneo de su vehiculo **Entonces** el sistema muestra las fallas en termino sencillo y técnico, y las malas prácticas **Escenario 2:  No realiza diagnóstico previo Dado** que el conductor independiente a ingresa a la aplicacion **Y** no realiza un diagnóstico previo **Cuando** solicita ver la información de su último escaneo **Entonces** el sistema informa que no hay datos disponibles **Y** le permite escanear el vehículo | EP03 |
| US42 | Acerca del vehículo | **Como** propietario de vehículo urbano **quiero** acceder a la informacion general de mi vehículo **para** conocer los datos relevantes de este. | **Escenario 1: Registra vehículo Dado** que el propietario de vehículo urbano ingresa a la aplicación **Y** registra un vehículo **Cuando** solicita conocer acerca de su vehiculo **Entonces** el sistema muestra descripción del vehiculo y datos como: nombre, kilometraje y año.  **Escenario 2: No Registra vehículo Dado** que el propietario de vehículo urbano ingresa a la aplicación **Y** no registra un vehículo **Cuando** solicita conocer acerca de su vehiculo **Entonces** el sistema muestra la falta del vehículo **Y** deja vincularse a un vehículo. | EP03 |
| US43 | Acceso a videos tutoriales | **Como** propietario de vehículo urbano **quiero** ver video tutoriales sobre el uso de la aplicación y temas de mantenimiento vehicular **para** aprender y comprender mejor como interactuar con mi vehículo y la plataforma. | **Escenario 1: Visualización de la lista de videos tutoriales con plan PRO Dado** que el propietario de vehículo urbano tiene el plan PRO **E** ingresa a la aplicación **Cuando** solicita los videos tutoriales **Entonces** el sistema muestra una lista de videos tutoriales con título, descripción e imagen referencial del video. **Escenario 2: Bloqueo de visualización por plan STANDARD Dado** que el propietario de vehículo urbano tiene el plan STANDARD **Cuando** solicita los videos tutoriales **Entonces** el sistema informa que debe de cambiar al plan PRO para el acceso a estos. | EP08 |
| US44 | Manual y guias técnicas | **Como** mecánico automotriz **quiero** a los manuales y guias técnicas **para** consultar información detallada sobre el uso de la aplicación y aspectos técnicos del vehículo. | **Escenario 1: Consulta con PLAN PRO Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca **Y** solicite el los manuales y guías técnicas, **Entonces** puede leer o visualizar el contenido con título, descripción y contenido. **Escenario 2: Consulta con PLAN STANDARD Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca **Y** solicite el los manuales y guías técnicas, **Entonces** puede leer o visualizar el contenido con título, descripción y contenido.| EP08 |
| US45 | Acceso a Recomendaciones de Cuidado Vehicular | **Como** mecánico automotriz **quiero** acceder a recomendaciones y consejos sobre el mantenimiento y cuidado de mi vehículo, **para** mantenerlo en óptimas condiciones y prolongar su vida útil. | **Escenario 1: Consulta con PLAN PRO Dado** que el mecanico automotriz tiene plan PRO **Cuando** accede a la biblioteca **Y** solicita las recomendaciones, **Entonces** puede leer o visualizar las recomendaciones con título, descripción y contenido. **Escenario 2: Consulta con PLAN STANDARD  Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** accede a la biblioteca **Y** solicita las recomendaciones, **Entonces** puede leer o visualizar las recomendaciones con título, descripción y contenido. | EP08 |

## 3.3. Impact Mapping
En este sección, nuestro equipo expone el uso del Impact Mapping, una técnica visual y participativa que permite conectar metas estratégicas con los resultados esperados, fomentando la alineación y el enfoque del equipo.

![impactmapping](/assets/imgs/chapter-III/impact-map.png)
## 3.4. Product Backlog
A continuación se detalla el Product Backlog del proyecto Vehix. En el Product Backlog mostraremos una lista ordenada de nuestras historias de usuario, priorizadas de acuerdo con el consenso del equipo. Para estimar la complejidad de cada tarea, empleamos la secuencia de Fibonacci (1, 2, 3, 5, 8) como referencia.

<table>
        <tr>
          <td><strong>#Orden</strong></td>
          <td><strong>User Stoy Id</strong></td>
          <td><strong>Título</strong></td>
          <td><strong>Descripción</strong></td>
          <td><strong>Story Points (1 / 2 / 3 / 5 / 8)</strong></td>
        </tr>
        <tr>
            <td>1</td>
            <td>US03</td>
            <td>Lista de beneficios</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero ver una lista de todos los beneficios para poder conocer las ventajas que se ofrecen</td>
            <td>5</td>
        </tr>
        <tr>
            <td>2</td>
            <td>US31</td>
            <td>Crear planes de suscripción</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero ver e informarme de los planes de suscripción para poder adquirir uno</td>
            <td>5</td>
        </tr>
        <tr>
            <td>3</td>
            <td>US02</td>
            <td>Búsqueda de Contenido</td>
            <td>Como visitante del segmento de mecánicos automotrices quiero ver contenido específico en el sistema para mayor claridad y rapidez al acceder a la información</td>
            <td>5</td>
        </tr>
        <tr>
            <td>4</td>
            <td>US38</td>
            <td>Desarrollo de vehiculos compatibles</td>
            <td>Como visitante del segmento de mecánicos automotriz quiero saber qué tipo de vehículos son compatibles con la aplicación para confirmar si puedo usarla con mi vehículo</td>
            <td>3</td>
        </tr>
        <tr>
            <td>5</td>
            <td>US30</td>
            <td>Implementación de testimonios</td>
            <td>Como visitante del segmento conductores independientes quiero visualizar los testimienos de otros usuarios, para conocer sus experiencias y generar confianza en el servicio</td>
            <td>3</td>
        </tr>
        <tr>
            <td>6</td>
            <td>US32</td>
            <td>Guía de conexiones</td>
            <td>Como propietario de vehículos urbanos quiero tener una guía de conexión vehículo-aplicación para usar la aplicación sin errores</td>
            <td>3</td>
        </tr>
        <tr>
            <td>7</td>
            <td>US37</td>
            <td>Preguntas frecuentes</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero informarme de preguntas frecuentes para validarlo con mis preguntas</td>
            <td>3</td>
        </tr>
        <tr>
            <td>8</td>
            <td>US29</td>
            <td>Acceso a la Aplicación desde la Página Principal</td>
            <td>Como visitante del segmento conductores independientes quiero ser guiado a la aplicación, para usar las funcionalidades disponibles</td>
            <td>3</td>
        </tr>
        <tr>
            <td>9</td>
            <td>US35</td>
            <td>Visualización de creadores</td>
            <td>Como visitante del segmento de conductores independientes quiero ver la información sobre los creadores del proyectos para conocer al equipo de la aplicación</td>
            <td>2</td>
        </tr>
        <tr>
            <td>10</td>
            <td>US33</td>
            <td>Soporte y redes</td>
            <td>Como visitante del segmento conductores independientes quiero poder contactar a soporte para resolver mis dudas</td>
            <td>2</td>
        </tr>
        <tr>
            <td>11</td>
            <td>US36</td>
            <td>Soporte Multilingüe</td>
            <td>Como visitante del segmento de conductores independientes quiero poder seleccionar el idioma en el que se muestra el contenido de la aplicación para comprender la información proporcionada</td>
            <td>2</td>
        </tr>
        <tr>
            <td>12</td>
            <td>US34</td>
            <td>Adaptación a diferentes dispositivos</td>
            <td>Como visitante del segmento de conductores independientes quiero visualizar la landing page para desde cualquier dispositivo</td>
            <td>1</td>
        </tr>
        <tr>
            <td>13</td>
            <td>US05</td>
            <td>Notificaciones de alerta del vehículo en tiempo real</td>
            <td>Como propietario de vehículo urbano, quiero recibir alerta inmediatas sobre el estado o fallos de mi vehículo para evitar daños mayores o situaciones de riesgo</td>
            <td>5</td>
        </tr>
        <tr>
            <td>14</td>
            <td>US07</td>
            <td>Diagnóstico vehicular</td>
            <td>Como mecánico automotriz quiero obtener un diagnóstico veraz del estado de mi vehículo para atender cualquier problema y considerar reparaciones o mantenimientos menos costosos.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>15</td>
            <td>US12</td>
            <td>Localizar un taller automotriz cercano</td>
            <td>Como conductor independiente, quiero localizar un taller mecánico cercano y confiable, para realizar arreglar o revisar mi vehículo</td>
            <td>5</td>
        </tr>
        <tr>
            <td>16</td>
            <td>US10</td>
            <td>Conexión bluetooth</td>
            <td>Como mecánico automotriz quiero conectarme a mi vehículo de manera rápida y precisa con bluetooth para tener información de mi vehículo en todo lugar y momento</td>
            <td>5</td>
        </tr>
        <tr>
            <td>17</td>
            <td>US13</td>
            <td>Auditoría de fallas</td>
            <td>Como conductor independiente, quiero ver la descripción y controlar el estado de la falla que tiene mi vehículo, para tomar medidas de mantenimiento y guardarlas en la aplicación</td>
            <td>5</td>
        </tr>
        <tr>
            <td>18</td>
            <td>US15</td>
            <td>Diagnóstico rápido</td>
            <td>Como conductor independiente quiero acceder al diagnóstico rápido de mi vehículo para obtener el estado de mi vehiculo de manera rápida y sencilla</td>
            <td>5</td>
        </tr>
        <tr>
            <td>19</td>
            <td>US27</td>
            <td>Vida útil del coche</td>
            <td>Como propietario de vehiculos urbanos quiero acceder a la informacion relevante sobre la vida útil de mi vehículo para mantener en óptimas condiciones mi vehículo</td>
            <td>5</td>
        </tr>
        <tr>
            <td>20</td>
            <td>US41</td>
            <td>Último escaneo</td>
            <td>Como conductor independiente quiero acceder a la informacion del último escaneo de mi vehículo para analizar el estado de mi vehículo</td>
            <td>5</td>
        </tr>
        <tr>
            <td>21</td>
            <td>US26</td>
            <td>Pago de suscripciones</td>
            <td>Como propietario de vehículo urbano quiero pagar la suscripción con mi tarjeta por medio de la aplicación para un pago rápido</td>
            <td>5</td>
        </tr>
        <tr>
            <td>22</td>
            <td>US20</td>
            <td>Ver consumo de combustible</td>
            <td>Como propietario de vehículo urbano, quiero ver mi consumo de combustible promedio, para manejar de forma más eficiente</td>
            <td>3</td>
        </tr
        <tr>
            <td>23</td>
            <td>US42</td>
            <td>Acerca del vehículo</td>
            <td>Como propietario de vehículo urbano quiero acceder a la informacion general de mi vehículo para conocer los datos relevantes de este</td>
            <td>3</td>
        </tr>
        <tr>
            <td>24</td>
            <td>US22</td>
            <td>Articulos técnicos</td>
            <td>Como mecánico automotriz quiero acceder y leer documentacion de articulos técnicos relevantes para mantenerme informado sobre los avances automotrices y mejorar mis conocimientos</td>
            <td>3</td>
        </tr>
        <tr>
            <td>25</td>
            <td>US43</td>
            <td>Acceso a videos tutoriales</td>
            <td>Como propietario de vehículo urbano quiero ver video tutoriales sobre el uso de la aplicación y temas de mantenimiento vehicular para aprender y comprender mejor como interactuar con mi vehículo y la plataforma</td>
            <td>3</td>
        </tr>
        <tr>
            <td>26</td>
            <td>US23</td>
            <td>Lengüage técnico</td>
            <td>Como mecánico automotriz quiero tener los codigos de error asociados a las fallas para identificarlas rapidamente</td>
            <td>3</td>
        </tr>
        <tr>
            <td>27</td>
            <td>US06</td>
            <td>Previsión de problemas</td>
            <td>Como conductor independiente quiero acceder a la informacion relevante sobre los problemas a futuro de mi vehículo para cuidar de mejor manera mi vehículo</td>
            <td>3</td>
        </tr>
        <tr>
            <td>28</td>
            <td>US16</td>
            <td>Fallas y reparaciones</td>
            <td>Como conductor independiente quiero acceder a la informacion de las reparaciones realizadas y fallas constatadas de mi vehículo para validar el estado de mi vehículo</td>
            <td>3</td>
        </tr>
        <tr>
            <td>29</td>
            <td>US24</td>
            <td>Noticias del sector automotriz</td>
            <td>Como mecánico automotriz quiero acceder y leer noticias del sector automotriz para saber las noticias en el sector</td>
            <td>3</td>
        </tr>
        <tr>
            <td>30</td>
            <td>US45</td>
            <td>Acceso a Recomendaciones de Cuidado Vehicular</td>
            <td>Como mecánico automotriz quiero acceder a recomendaciones y consejos sobre el mantenimiento y cuidado de mi vehículo, para mantenerlo en óptimas condiciones y prolongar su vida útil</td>
            <td>3</td>
        </tr>
        <tr>
            <td>31</td>
            <td>US44</td>
            <td>Manual y guias técnicas</td>
            <td>Como mecánico automotriz quiero a los manuales y guias técnicas para consultar información detallada sobre el uso de la aplicación y aspectos técnicos del vehículo</td>
            <td>3</td>
        </tr>
        <tr>
            <td>32</td>
            <td>US25</td>
            <td>Avances del sector automotriz</td>
            <td>Como mecánico automotriz quiero acceder y leer sobre los avances y tendencias del sector automotriz para mantenerme al día con la evolución de la tecnología y las prácticas en la industria</td>
            <td>3</td>
        </tr>
        <tr>
            <td>33</td>
            <td>US28</td>
            <td>Eliminación de vehículo</td>
            <td>Como mecánico automotriz quiero eliminar un vehículo de mi lista para actualizar mis vehículos</td>
            <td>2</td>
        </tr>
        <tr>
            <td>34</td>
            <td>US11</td>
            <td>Ingresar nuevo vehículo</td>
            <td>Como propietario de vehículo urbano quiero registrar mi vehículo para poder tener una lista ordenada de mis vehículos</td>
            <td>2</td>
        </tr>
        <tr>
            <td>35</td>
            <td>US08</td>
            <td>Cierre de sesión</td>
            <td>Como propietario de vehículo urbano, quiero cerrar mi sesión activa para poder proteger mi cuenta y finalizar mi interacción con el sistema de forma segura</td>
            <td>2</td>
        </tr>
        <tr>
            <td>36</td>
            <td>US01</td>
            <td>Registro de cuenta</td>
            <td>Como propietario de vehículo urbano, quiero registrarme para acceder a las funcionalidades de la aplicación </td>
            <td>2</td>
        </tr>
        <tr>
            <td>37</td>
            <td>US21</td>
            <td>Edición de información personal</td>
            <td>Como conductor independiente, quiero poder actualizar mi información personal, para mantener mis datos precisos y actualizados en la aplicación</td>
            <td>2</td>
        </tr>
        <tr>
            <td>38</td>
            <td>US04</td>
            <td>Inicio de sesión</td>
            <td>Como propietario de vehículo urbano quiero iniciar sesión en la aplicación para usar todas las funcionalidades de esta</td>
            <td>2</td>
        </tr>
        <tr>
            <td>39</td>
            <td>US09</td>
            <td>Historial de vehículos</td>
            <td>Como mecánico automotriz quiero ver un historial de vehículos previamente registrados para consultar información sobre ellos y gestionar mis datos de forma efectiva</td>
            <td>2</td>
        </tr>
        <tr>
            <td>40</td>
            <td>US14</td>
            <td>Estado de suscripción</td>
            <td>Como conductor independiente, quiero saber que suscripción poseo, para verificar mi estado de suscripción.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>41</td>
            <td>TS17</td>
            <td>Obtener el historia técnico del vehículo a través de RESTfulAPI</td>
            <td>Como developer, quiero obtener el historial técnico de un vehículo mediante una API, para que esté este disponible para crear funciones para mis aplicaciones</td>
            <td>5</td>
        </tr>
        <tr>
            <td>42</td>
            <td>TS18</td>
            <td>Obtener mecánicos cercanos a través de RESTfulAPI</td>
            <td>Como developer, quiero obtener los mecánicos cercanos mediante una API, para que esté este disponible para crear funciones para mis aplicaciones</td>
            <td>5</td>
        </tr>
        <tr>
            <td>43</td>
            <td>TS19</td>
            <td>Agregar Nuevo vehículo a través de RESTfulAPI</td>
            <td>Como developer, quiero registrar un nuevo vehículo para permitir a los usuarios registrar sus vehículos</td>
            <td>5</td>
        </tr>
        <tr>
            <td>44</td>
            <td>TS40</td>
            <td>Registro Usuario</td>
            <td>Como developer, quiero crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, para que pueda permitir el registro de usuarios en la plataforma</td>
            <td>5</td>
        </tr>
        <tr>
            <td>45</td>
            <td>TS39</td>
            <td>Actualizar datos de un vehículo</td>
            <td>Como developer, quiero actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, para que pueda mantener actualizada la información registrada en la plataforma</td>
            <td>5</td>
        </tr>
    </table>
A continuación, se le hace presente el link del product backlog:

**Link:**  [Product Backlog](https://trello.com/invite/b/68363c9576438ad07b9ea838/ATTI8fb235d4573d555662751062510e05a86E507E27/vehix)

Además se le presenta la captura de imagen del proct backlog el cyual ha sido diseñado en la herramienta de Jira
![Trello](/assets/imgs/chapter-III/sprint-backlog-trello.png)
