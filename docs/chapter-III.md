# Capítulo III: Requirements Specification
## 3.1. To-Be Scenario Mapping
En esta sección se abordará el To-Be Scenario Mapping para cada uno de las User Persona, en el cual describiremos en filas Phases, Doing, Thinking y Feeling.

Segmento 1: Propietarios de vehículos urbanos que desean prolongar la vida útil de su auto personal.
![to-be-scenario-mapping-segment-1](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-1.jpg)
En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Uso diaria del auto, notan un comportamiento extraño, problema evidente y post-reparación. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, se recata el análisis en tiempo real del vehículo, como actividad principal.

Segmento 2: Conductores independientes que generan ingresos con su vehículo.
![to-be-scenario-mapping-segment-2](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-2.jpg)
En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Inicio de jornada laboral, Durante el trabajo, Falla crítica o emergencia y Evaluación del gasto. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, se recata la ayuda activa de la aplicación para poder derivar a mecánicos cercanos y a la vez el diagnóstico rápido para manejar sin preocupación.

Segmento 3: Mecánicos o técnicos automotrices que desean mejorar sus diagnósticos y comunicación con los clientes.
![to-be-scenario-mapping-segment-3](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-3.jpg)
En el siguiente escenario se muestran las fases que se ha considerado a través de una lluvia de ideas con el equipo, siendo: Cliente llega con una falla, Diagnóstico, Datos útiles y Registro del caso. Siendo estos los escenarios clave donde se presenta del gran aporte de la aplicación con respecto a sus requisitos. Asimismo, el diagnóstico rápido, ahorro de tiempo y lenguage técnico.

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
| US01 | Registro de cuenta | **Como** propietario de vehículo urbano, **quiero** registrarme **para** acceder a las funcionalidades de la aplicación | **Escenario 1: Registro exitoso Dado** que el propietario de vehículo urbano ingresa información válida, como: nombre, apellidos, dni, correo personal, contraseña, número de celular y género,**Cuando** solicita el registro, **Entonces** su cuenta se crea correctamente y puede acceder a la plataforma. **Escenario 2: Error en el registro Dado** que el propietario de vehículo urbano ingresa información incompleta o incorrecta en los campos de nombre, apellidos, dni, correo personal, contraseña, número de celular, dni y/o género, **Cuando** solicita el registro, **Entonces** el sistema le notifica sobre el error y le permite corregirlo.| EP01 |
| US02 | Búsqueda de Contenido | **Como** visitante del segmento de mecánicos automotrices **quiero** encontrar contenido específico en el sistema **para** mayor claridad y rapidez al acceder a la información. | **Escenario 1: Acceso a las secciones Dado** que el visitante del segmento de mecánicos automotrices busca una sección en específico **Cuando** elige la sección, **Entonces** el sistema muestra la información correspondiente. **Escenario 2: Búsqueda sin resultados Dado que** que el visitante del segmento de mecánicos automotrices se encuentra en la página, **Cuando** busque con una sección específica **Y** no se encuentre **Entonces** el sistema mostrará toda la información.  | EP02 |
| US03 | Lista de beneficios | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** ver una lista de todos los beneficios **para** poder conoceer las ventajas que se ofrecen. | **Escenario 1: Visualización exitosa de beneficios Dado** que el visitante del segmento de propietarios de vehículos urbanos ingresa a la landing page **Cuando** solicite los beneficios **Entonces** la landing page muestra una lista de todos los beneficios activos  **Escenario 2: No hay beneficios activos para mostrar Dado que** que el visitante del segmento de propietarios de vehículos urbanos ingresa a la landing page **Cuando** no existen beneficios activos **Entonces** la landing page informa que no hay beneficios disponibles en este momento  | EP02 |
| US04 | Inicio de sesión | **Como** propietario de vehículo urbano **quiero** iniciar sesión en la aplicación **para** usar todas las funcionalidades de esta. | **Escenario 1: Inicio de sesión exitoso Dado** que el propietario de vehículo urbano ingresa credenciales válidas de DNI y contraseña **Cuando** solicita acceder a la aplicación, **Entonces** ingresa a la aplicacón sin errores. **Escenario 2: Credenciales inválidas Dado**  que el propietario de vehículo urbano ingresa datos incorrectos de DNI y/o contraseña, **Cuando** intenta ingresar a la aplicación, **Entonces** recibe un aviso y puede volver a intentarlo. **Escenario 3: Falta de credeneciales Dato que** el propietario de vehículo urbano ingresa uno o ningún DNI o contraseña , **Cuando** solicita acceder a la aplicación, **Entonces** el sistema informe la falta de credencial.| EP01 |
| US05 | Notificaciones de alerta del vehículo en tiempo real | **Como** propietario de vehículo urbano, **quiero** recibir alerta inmediatas sobre el estado o fallos de mi vehículo **para** evitar daños mayores o situaciones de riesgo. | **Escenario 1: Generación de alerta por evento crístico del vehículo Dado que** el propietario de vehículo urbano esta conectado correctamente al vehículo, **Cuando** el sistema procesa la información de una anomalía crítica **Entonces** el sistema genera una notificación de alerta **E** indicando la magnitud del defecto. **Escenario 2: Alerta por acción inadedcuada del usuario que afecta al vehículo Dado** que el propietario realiza una acción que afecta el estado del vehículo,  **Cuando** el sistema registra el estado del vehículo **Entonces** el sistema genera una notificacion de alerta si el estado actual es crítico. **Escenario 3: Historial de alertas Dado** que el propietario de vehiculos urbanos visualiza las alertas,  **Cuando** solicite revisar todas las alerta **Entonces** el sistema mostrará todas la lista de alertas del vehículo. | EP03 |
| US06 | Vida útil del vehículo | **Como** conductor independiente **quiero** acceder a la informacion relevante sobre la vida útil de mi vehículo **para** mantener mi vehículo en el mejor estado. | **Escenario 1: Diagnóstico previo para la vida útil del vehículo Dado** que el conductor independiente ingresa a la aplicación **Y** halla realizado un diagnóstico previo **Cuando** solicita ver la informacion de la vida útil de su vehiculo **Entonces** el sistema muestra indicacores relevantes como el kilometraje total y cantidad años de servicio en las mejores condiciones. **Escenario 2: No se realiza diagnóstico previo para la vida útil del vehículo Dado** que el conductor independiente a ingresado a la aplicacion **Y** no halla realizado un diagnóstico previo **Cuando** solicite ver la información de la vida útil de su vehículo **Entonces** el sistema informa que no hay datos disponibles **Y** le permitirá escanear el vehículo | EP03 |
| US07 | Previsión de problemas |  **Como** conductor independiente **quiero** acceder a la informacion relevante sobre los problemas a futuro de mi vehículo **para** cuidar de mejor manera mi vehículo. | **Escenario 1:  Diagnóstico previo para la previsión de problemas del vehículo Dado** que el conductor independiente ingresa a la aplicación **Y** halla realizado un diagnóstico previo **Cuando** solicita ver los problemas o fallas a futuro de su vehículo **Entonces** el sistema muestra indicacores relevantes del pronóstico considerando los 7 sistemas principales del vehiuclo **Y** las probabilidades de falla en cada uno **Escenario 2: No se realiza diagnóstico previo para la previsión de problemas del vehículo Dado** que el conductor independiente a ingresado a la aplicacion **Y** no halla realizado un diagnóstico previo **Cuando** solicita ver los problemas o fallas a futuro de su vehículo **Entonces** el sistema informa que no hay datos disponibles **Y** le permitirá escanear el vehículo. | EP03 |
| US08 | Diagnóstico vehicular| **Como** mecánico automotriz **quiero** obtener un diagnóstico veraz del estado de mi vehículo **para** atender cualqueir problema y considerar reparaciones o mantenimientos menos costosos. | **Escenario 1: Ejecución Exitosa de un Diagnóstico General Dado que** el mecánico automotriz se ha enlazado con un vehículo **Cuando** el mecánico automotriz solicite el escaneo del vehículo, **Entonces** el sistema muestra los errores del vehículo en lenguage simple y técnico, malas prácticas de manejo, nivel de urgencia **Y** consejos para solucionarlo. **Escenario 2: Ejecución Fallida de un Diagnóstico General Dado que** el mecánico automotriz no se ha enlazado con un vehículo **Cuando** el mecánico automotriz solicite el escaneo del vehículo, **Entonces** el sistema muestra el error de conexión con el vehículo **Y** le permite buscar vehículos por bluetooth.  | EP03 |
| US09 | Cierre de sesión | **Como** propietario de vehículo urbano, **quiero** cerrar mi sesión activa **para** poder proteger mi cuenta y finalizar mi interacción con el sistema de forma segura | **Escenario 1: Cierre exitoso Dado** que el propietario del vehículo urbano está con una sesión activa, **Cuando** solicita cerrar su sesión, **Entonces** el sistema funaliza su sesión actual **Y** lo redirige al estado de inicio de sesión. **Escenario 2: Intento de acceso Posterior a cerrar sesión Dado que** el propietario del vehículo urbano cierra su sesión **Cuando** intente acceder a una función **Entonces** el sistema le impide el acceso a esa funcionalidad **Y** solicita que inicie sesión nuevamente.  | EP01 |
| US10 | Historial de vehículos | **Como** mecánico automotriz **quiero** ver un historial de vehículos previamente registrados **para** consultar información sobre ellos y gestionar mis datos de forma efectiva. | **Escenario 1: Visualización del Historial de Vehículos con plan PRO Dado** que el mecánico automotriz ya ha registrado uno o más vehículos con el plan PRO **Cuando** solicite ver el historial de vehiculos registrados, **Entonces** el sistema muestra una lista de todos los vehículos que ha registrado con el nombre del vehículo asignado **Escenario 2: Visualización del Historial de Vehículos con plan STANDARD Dado Dado** que el mecánico automotriz tiene el plan standard **Y** ha registrado a un vehículo, **Cuando** solicite la lista de vehículos, **Entonces** la aplicación muestra el único vehículo **Y** no se le permite añadir más vehículos. **Escenario 3: Historial de vehículos vacío Dado** que el mecánico automotriz tiene el plan PRO o STANDARD, **Cuando** solicite la lista de vehículos, **Entonces** se le informa que debe registrar vehículos **Y** se le permite registrar.  | EP03 |
| US11 | Conexión bluetooth | **Como** mecánico automotriz **quiero** conectarme a mi vehículo de manera rápida y precisa con bluetooth **para** tener información de mi vehículo en todo lugar y momento. | **Escenario 1: Transmisión de datos correctos Dado** que el mecánico automotriz instala en el puerto OBD2 del vehiculo, el adaptador de diagnóstico VEHIX, **E** incia sesión correctamente en la aplicación **Cuando** el sistema detecta el vehículo y se intenta la conexión, **Entonces** el sistema establece una conexión **Y** muestra la opción de registrar el vehículo. **Escenario 2: Transmisión de datos incorrecto Dado** que el mecánico automotriz instala de manera errónea el adaptador diagnóstico VEHIX **E** intenta conectar a este por la aplicación por medio de la aplicación **Cuando** el mecanico automotriz activa el bluetooh **Y** no se visualize ningún adaptador en pantalla **Entonces** la aplicación mostrará el video de instalación y la guía rapida de instalación. | EP04 |
| US12 | Ingresar nuevo vehículo | **Como** propietario de vehículo urbano **quiero** registrar mi vehículo **para** poder tener una lista ordenada de mis vehículos. | **Escenario 1: Registro exitoso de vehículo Dado** que el propietario de vehículo urbano conecta de manera exitosa su vehículo con la aplicación **Cuando** el propietario de vehiculo urbano ingresa información válida y completa del vehículo, como: nombre del vehículo, modelo, kilometraje y año de producción **Entonces** el sistema guarda el vehículo en la lista de vehículos. **Escenario 2: Registro fallido de vehículo Dado** que el propietario de vehículo urbano conecta de manera exitosa su vehículo con la aplicación **Cuando** el propietario de vehiculo urbano ingresa información inválida o imcompleta del vehículo, como: nombre del vehículo, modelo, kilometraje y año de producción **Entonces** el sistema guarda informa que debe ingresar correctamente los datos.  **Escenario 2: Bloqueo de registro Dado** que el propietario de vehículo urbano registra un vehiculo y tiene el plan STANDARD **Cuando** intente registrar otro vehículo. **Entonces** la aplicación mostrará que debe de adquirir el plan PRO. | EP01 |
| US13 | Localizar un taller automotriz cercano | **Como** conductor independiente, **quiero** localizar un taller mecánico cercano y confiable, **para** realizar arreglar o revisar mi vehículo | **Escenario 1: Mecánicos disponibles en la zona Dado** el conductor independiente ha ingresado a la aplicación **Y** halla realizado un diagnóstico, **Cuando** este solicite ayuda **Y** active el gps **Entonces** se le muestran opciones de mecánicos cercanos, certificados y expertos en su falla. **Escenario 2: No hay mecánicos cercanos Dado** el conductor independiente ha ingresado a la aplicación **Y** halla realizado un diagnóstico, **Cuando** solicite ayuda **Y** active el gps **Entonces** se le informa que no hay resultados de mecánicos cercanos, certificados y expertos en su falla. **Escenario 3: No activa el GPS Dado** que el conductor independiente ingrese a la aplicación **Y** halla realizado un disagnóstico **Cuando** solicite ayuda **Y** no active el GPS **Entonces** no visualizará mecánicos cercanos, certificados y expertos en su falla.  | EP05 |
| US14 | Auditoría de fallas | **Como** conductor independiente, **quiero** ver la descripción y controlar el estado de la falla que tiene mi vehículo, **para** tomar medidas de mantenimiento y guardarlas en la aplicación. | **Escenario 1: Falla identificada Dado** que el sistema ha detectado un error o se ha registrado un escaneo de diagnóstico, **Cuando** el conductor independiente accede a la auditoría de fallas, **Entonces** se muestran las fallas con título referencial, motivo **Y** permitiendo ingresar si se resolvió la falla. **Escenario 2: Vehículo en buen estado Dado** que la aplicación no a detectado ninguna una falla a través del diagnóstico, **Cuando** el conductor independiente ingresae a la auditoría de fallas **Entonces** se le informa que su vehículo está en buen estado | EP03 |
| US15 | Estado de suscripción | **Como** conductor independiente, **quiero** saber que suscripción poseo, **para** verificar mi estado de suscripción. | **Escenario 1: Suscripción activa Dado** que el conductor independiente tiene una suscripción, **Cuando** accede al perfil, **Entonces** se le muestra la fecha de renovación. **Escenario 2: Cambio de suscripción Dado** que la suscripción se encuentra activa **Cuando** el conductor independiente quiere cambiar de plan **Entonces** el sistema le pedirá ingresar número de tarjetas, mes y año de expiracion y codigo de seguridad de la tarjeta. **Escenario 3: Suscripción expirada Dado** que la suscripción se encuentra expirada **Cuando** el conductor independiente ingresa a la aplicación **Entonces** el sistema se le pedirá renovar su suscripción solicitandole número, mes y año de expiracion y codigo de seguridad de la tarjeta.| EP06 |
| US16 | Diagnóstico rápido | **Como** conductor independiente **quiero** acceder al diagnóstico rápido de mi vehículo **para** obtener el estado de mi vehiculo de manera rápida y sencilla. | **Escenario 1: Diagnóstico rápido exitoso Dado** que el conductor independiente ingresa a la aplicación **Y** se halla conectado a un vehículo **Cuando** solicita ver el diagnóstico rápido de su vehículo **Entonces** el sistema muestra indicacores relevantes del pronóstico considerando los 4 sistemas principales del vehiculo, como motor, bateria, frenos y sensores **Y** el estado en cada uno **Escenario 2: Bloqueo de diagnóstico rápido Dado** que el conductor independiente tiene el plan STANDARD **Cuando** solicita ver el diagnóstico rápido de su vehículo **Entonces** el sistema informa que debe de cambiar al plan PRO. | EP03 |
| US17 | Fallas y reparaciones | **Como** conductor independiente **quiero** acceder a la informacion de las reparaciones realizadas y fallas constatadas de mi vehículo **para** validar el estado de mi vehículo. | **Escenario 1:  Realiza diagnóstico previo Dado** que el conductor independiente ingresa a la aplicación **Y** realiza un diagnostico previo **Y** el sistema lea fallas **Cuando** solicite ver las reparaciones recientes **Entonces** el sistema muestra las fallas, el nivel de urgencia y el estado de la falla, también el problema solucionado de la reparación, la mejora del vehiculo a causa de la solucion y el día de la reparación.  **Escenario 2:  No realiza diagnóstico previo Dado** que el conductor independiente ingresa a la aplicación **Y** no realiza un diagnostico previo **Cuando** solicite ver las reparaciones recientes **Entonces** el sistema muestra que falta realizar un diagnostico previo. | EP06 |
| TS18 | Obtener el historia técnico del vehículo a través de RESTfulAPI | **Como developer,** **quiero** obtener el historial técnico de un vehículo mediante una API, **para** que los usuarios puedan ver el estado del vehiculo general. | **Escenario 1: Consulta con identificador válido Dado que** el identificador del vehículo proporcionado es válido, **Cuando** el developer realiza una solicitud GET para consultar el historial, **Entonces** el sistema devuelve el historial técnico correspondiente al vehículo. **Escenario 2: Consulta con identificador inexistente Dado que** el identificador proporcionado no corresponde a ningún vehículo registrado, **Cuando** el developer realiza una solicitud GET para consultar el historial, **Entonces** el sistema devuelve un mensaje de error informativo indicando que no se encontró el vehículo.  | EP07 |
| TS19 | Mecánico cercanos | **Como developer,** **quiero** listar los mecánicos cercanos mediante una solicitud GET, **para** que los conductores puedan encontrar soporte técnico de forma rápida y confiable. | **Escenario 1: Ubicación válida con mecánicos disponibles Dado que** existen mecánicos cercano a la ubicación proporcionada, **Cuando** el developer realiza una solicitud GET indicando la ubicación **Y** tipo de fallo, **Entonces** el sistema muestra una lista de mecánicos disponibles cercanos **y** especializados en la falla. **Escenario 2: Ubicación sin mecánicos registrados Dado que** no existen mecánicos registrados para la ubicación actual del usuario, **Cuando** el developer realiza una solicitud GET, **Entonces** el sistema devuelve una lista vacía junto con un mensaje informativo indicando que no se encontraron mecánicos disponibles en esa área. | EP07 |
| TS20 | Vehículos registrados | **Como developer,** **quiero** registrar un nuevo vehículo enviando sus datos mediante una solicitud POST, **para** que pueda añadir vehículos al sistema y mantener actualizada la información disponible. | **Escenario 1: Registro exitoso del vehículo Dado que** los datos del vehículo (nombre del carro, modelo, kilometraje y año de fabricación) proporcionados por el developer están completos y son válidos, **Cuando** el developer realiza una solicitud POST para registrar un nuevo vehículo, **Entonces** el sistema guarda el vehículo en la base de datos **y** confirma el registro exitoso.  **Escenario 2: Error por datos incompletos o erróneos Dado que** los datos enviados (nombre del carro, modelo, kilometraje y año de fabricación) por el developer están incompletos o contienen errores de formato, **Cuando** el developer realiza una solicitud POST para registrar el vehículo, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error explicando los problemas encontrados. | EP07 |
| US21 | Ver consumo de combustible | **Como** propietario de vehículo urbano, **quiero** ver mi consumo de combustible promedio, **para** manejar de forma más eficiente. | **Escenario 1: Datos disponibles Dado** que el sistema ha registrado un vehículo **Cuando** el propietario de vehículo urbano ingresa al inicio **Y** elige u vehículo **Entonces** se visualiza el consumo en porcentaje del combustible. **Escenario 2: Sin registros de consumo Dado** que aún no hay un vehículo registrado **Cuando** el propietario de vehículo urbano accede al perfil para verificar el consumo de gasolina de un vehículo **Entonces** se le indica que no hay registro de vehículo.  | EP03 |
| US22 | Edición de información personal | **Como** conductor independiente, **quiero** editar la información de mi perfil, **para** cambiar mis datos si lo veo necesario | **Escenario 1: Edición exitosa Dado** que el  conductor independiente actualiza sus datos, como: nombre, apellidos, correo, contraseña y número de celular, correctamente, **Cuando** solicite el guardado, **Entonces** el sistema los almacena y refleja los cambios en su perfil. **Escenario 2: Fallo en la edición Dado** que el conductor independiente introducen datos insuficientes, como: nombre, apellidos, correo, contraseña y/o número de celular, **Cuando** solicite guardar, **Entonces** el sistema le informa del error y notifica rellenar los campo faltante  | EP01 |
| US23 | Biblioteca automotriz | **Como** mecánico automotriz **quiero** leer documentación acerca de métodos o avances tecnológicos en el sector **para** mantenerme informado. | **Escenario 1: Consulta de contenido disponible Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar el material técnico y multimedia. **Escenario 2: Bloqueo de contenido Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca, **Entonces** puede solo leer el material técnico mas no visualizar el material multimedia. | EP05 |
| US24 | Datos técnicos | **Como** mecánico automotriz **quiero** tener el estado de mi vehículo a la mano **para** un análisis rápido. | **Escenario 1: Visualizar estado del vehículo** **Dado** que el mecánico automotriz accede al perfil técnico del vehículo **Cuando** acceda a la sección de diagnostico **Entonces** podrá visualizar el apartado de previsión de problemas, vida útil del vehículo **Y** un diagnóstico rápido con lenguage técnico **Y** estadisticas intuitiva. **Escenario 2: Visualización de técnico del vehículo** **Dado** que el mecánico automotriz accede al apartado de diagnóstico **Cuando** esté en el diagnostico rapido **Entonces** predominará la información del estado del motor, bateria, frenos y sensores.. | EP05 |
| US25 | Recordatorios de Revisiones técnicas | **Como** conductor independiente **quiero** que la aplicación me recuerde el día de la próxima revisión técnica **para** recodarlo y estar alerta. | **Escenario 1: Recordatorio registrado Dado** que el conductor independiente ha registrado una nueva fecha de revision con título, descripción y fecha, **Cuando** solicite el registro de la revisión, **Entonces** el sistema informará el registro de este exitosamente. **Escenario 2: Recordatorios no registrado Dado** que el conductor independiente ha registrado una nueva fecha de revision con título, descripción y/o fecha errónea, **Cuando** solicite el registro de la revisión, **Entonces** el sistema envía el error y permite editarlos.  | EP03 |
| US26 | Registro de datos de vehículo. | **Como** conductor independiente, **quiero** guardar registros de los datos de mi vehículo **para** mantenerme informado. | **Escenario 1: Registro exitoso Dado** que el conductor independiente ha ingresado los datos como: nombre del carro, modelo, kilometraje y año de fabricación **Cuando** solicita el registro, **Entonces** el vehículo estará disponible en la lista de vehículos **Escenario 2: Falla en el registro Dado** que el conductor independiente ingresa datos, como nombre de carro, modelo, kilometrage y año de fabricación de manera errónea **Cuando** intente guardarlos, **Entonces** el sistema informa acerca de la corrección de datos.  | EP03 |
| US27 | Pago de suscripciones | **Como** propietario de vehículo urbano **quiero** pagar la suscripción con mi tarjeta por medio de la aplicación **para** un pago rápido | **Escenario 1: Pago exitoso Dado** que los datos de la tarjeta como: numbero de tarjeta, fecha de expiracion y código de seguridad, **Cuando** el propietario de vehículo urbano proceda con el pago, **Entonces** se confirma la suscripción al plan correspondiente. **Escenario 2: Fallo en el pago Dado** que los datos de la tarjeta como: número de tarjeta, fehca de expiración y código de seguridad, no son válidos, **Cuando** el propietario de vehículo urbano proceda con el pago, **Entonces** el sistema pedirá corregir los campos. | EP06 |
| US28 | Estado del vehículo | **Como** propietario de vehículo urbano **quiero** información acerca del estado de mi vehículo **para** estar informado. | **Escenario 1: Datos visualizados correctamente Dado** que existe un diagnóstico previo, **Cuando** el propietario de vehículo urbano accede a la vida útil del coche, **Entonces** se muestra la información correspondiente, como: mes-kilometrage, tiempo de vida estimado y calidad del vehículo. **Escenario 2: Sin datos registrados Dado** que  el propietario de vehículo urbano aún no realiza ningún diagnóstico **Cuando** el usuario accede a la vida útil del coche, **Entonces** la aplicación indicará que faltan datos. | EP03 |
| US29 | Eliminación de vehículo | **Como** mecánico automotriz **quiero** eliminar un vehículo de mi lista **para** actualizar mis vehículos. | **Escenario 1: Eliminación confirmada Dado** que el mecánico automotriz decide eliminar un vehículo, **Cuando** realiza la solicitud, **Entonces** la aplicación pide confirmación **Y** al aceptar elimina el vehículo. **Escenario 2: Cancelación de la eliminación Dado** que el mecánico automotriz decide eliminar un vehículo, **Cuando** realiza la solicitud, **Entonces** la aplicación pide confirmación **Y** al no acepta no elimina el vehículo. | EP01 |
| US30 | Desarrollar visualización y call to action | **Como** visitante del segmento conductores independientes **quiero** entender de qué trata la plataforma, **para** saber si es útil para mí.  | **Escenario 1: Información clara y accesible Dado** que el visitante del segmento conductores independientes accede a la landing page, **Cuando** ingresa, **Entonces** visualiza la propuesta valor **Y** el diferenciador de la aplicación. **Escenario 2: Visitante nuevo sin conocimientos técnicos Dado** que el visitante del segmento de conductores independientes no conoce de mecánica o diagnósticos automotrices, **Cuando** accede a la información general, **Entonces** encontrará información, clara concisa y sin tecnicismos. | EP02 |
| US31 | Implementación de testimonios | **Como** visitante del segmento conductores independientes **quiero** visualizar testimonios reales, **para** usar la aplicación.  | **Escenario 1: Atajo de testimonios Dado** que existen testimonios publicados, **Cuando** el visitante del segmento de conductores independientes accede a la sección de testimonios, **Entonces** puede visualizar las experiencias compartidas. **Escenario 2: Visualización de la calificación Dado** que cada testimonio incluye una calificación, comentario, nombre y apellido, **Cuando** el visitante del segmento de conductores independientes visualiza la lista de testimonios, **Entonces** cada testimonio muestra la calificación asignada. | EP02 |
| US32 | Crear planes de la aplicación | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** membresías o planes **para** informarme. | **Escenario 1: Visualización de planes activa Dado** que existen diferentes 2 tipos de suscripciones, **Cuando** el visitante del segmento de propietarios de vehículos urbanos accede a la sección correspondiente, **Entonces** observa los beneficios de cada plan y sus diferenciadores. **Escenario 2: Más información de planes Dado** que el visitante del segmento de propietarios de vehículos urbanos busca más información de planes, **Cuando** revisa los contactos, **Entonces** el sistema permite ingresar datos de consulta, como: nombre, correo, tema de consulta y un mensaje. | EP02 |
| US33 | Guía de conexiones | **Como** visitante del segmento propietarios de vehículos urbanos **quiero** tener una guía de conexión vehículo-aplicación **para** usar la aplicación sin errores. | **Escenario 1: Visualización Multimedia Dado** que el visitante del segmento de propietarios de vehículos ingresa a la landing page, **Cuando** está en la sección de uso, **Entonces** se muestra un video explicativo de la instalación. **Escenario 1: Visualización Textual Dado** que el visitante del segmento de propietarios de vehículos ingresa a la landing page, **Cuando** está en la sección de uso, **Entonces** se muestra un video explicativo con subtítulos. | EP02 |
| US34 | Soporte y redes | **Como** visitante del segmento conductores independientes **quiero** poder contactar a soporte **para** resolver mis dudas | **Escenario 1: Envío exitoso de consulta Dado** que el visitante del segmento de conductores independiente ingresa a la landing page, **Cuando** accede a la sección de contacto **Y** escribe, nombre, correo, tema de consulta y un mensaje, **Entonces** se envía el contacto correctamente. **Escenario 2: Envío fallido de consulta Dado** que el visitante del segmento de conductores independiente ingresa a la landing page, **Cuando** accede a la sección de contacto **Y** escribe de manera incorrecta o no rellena nombre, correo, tema de consulta y/o un mensaje , **Entonces** se le solicita rellenar los campos. | EP02 |
| US35 | Diseño responsive | **Como** visitante del segmento de conductores independientes **quiero** visualizar la landing page **para** desde cualquier dispositivo. | **Escenario 1: Adaptación en pantalla móvil Dado** que el visitante del segmento de conductores independientes accede a la landing page desde un dispositivo con un ancho de pantalla inferior o igual a 900px, **Cuando** la página se carga, **Entonces** los elementos de la página se reorganizan y ajustan su tamaño para ser completamente visibles **Y** legibles. **Escenario 2: Adaptación en pantalla de escritorio Dado** que el visitante del segmento de conductores independientes accede a la landing page desde un dispositivo con un ancho de pantalla superior a 900px, **Cuando** la página se carga, **Entonces** los elementos de la página se distribuyen de forma óptima en el ancho disponible. | EP02 |
| US36 | Visualización de creadores | **Como** visitante del segmento de conductores independientes **quiero** saber quienes realizaron el proyecto, **para** informarme de estos.  | **Escenario 1: Información del equipo publicada Dado** que se cuenta con una sección de quiénes somos, **Cuando** el visitante del segmento de conductores independientes accede, **Entonces** puede ver los nombres, perfiles y fotos del equipo. **Escenario 2: Interés en el respaldo profesional Dado** que el visitante de conductores independientes busca la informacion de la trayectoria del equipo, **Cuando** accede al perfil de un integrante, **Entonces** puede ver breves descripciones de roles o trayectoria.  | EP02 |
| US37 | Soporte Multilingüe | **Como** visitante del segmento de conductores independientes **quiero** poder seleccionar el idioma español o inglés **para** entender completamente la información proporcionada. | **Escenario 1: Idioma español Dado** que la landing page ofrece la opción de seleccionar el idioma, **Cuando** el visitante elige la opción es, **Entonces** todo el contenido textual de la landing page se muestra en idioma español. **Escenario 2: Idioma inglés Dado** que la landing page ofrece la opción de seleccionar el idioma, **Cuando** el visitante elige la opción en, **Entonces** todo el contenido textual de la landing page se muestra en idioma inglés. | EP02 |
| US38 | Preguntas frecuentes. | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** informarme de preguntas frecuentes **para** validarlo con mis preguntas. | **Escenario 1: Visualización de la sección de preguntas frecuentes Dado** que el visitante del segmento de propietarios de vehículos urbanos quiere resolver sus dudas rápidamente,  **Cuando** accede a la sección de preguntas frecuentes, **Entonces** ve una lista clara de preguntas y respuestas relevantes sobre la aplicación. **Escenario 2: Interacción con preguntas expandibles Dado que** el visitante del segmento de propietarios de vehículos urbanos explora las preguntas frecuentes, **Cuando** hace clic sobre una pregunta, **Entonces** la respuesta se despliega de manera inmediata, sin recargar la página.  | EP02 |
| US39 | Desarrollo de vehiculos compatibles | **Como** visitante del segmento de mecánicos automotriz **quiero** saber qué tipo de vehículos es compatible con la aplicación **para** informarme. | **Escenario 1: Visualización de la lista de vehículos compatibles Dado que** el visitante del segmento de mecánicos ingresa a la landing page, **Cuando** accede a la sección de vehículos compatibles, **Entonces** visualiza una lista clara que incluye marcas, modelos o tipos de vehículos soportados. **Escenario 2: Visualización destacada de tipos de vehículos mediante imágenes Dado que** el visitante  del segmento de mecánicos explora la sección de vehículos compatibles, **Cuando** accede a la lista de tipos de vehículos, **Entonces** identifica rápida y facilmente los vehículos compatibles. | EP02 |
| TS40 | Actualizar datos de un vehículo | **Como** developer, **quiero** actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, **para** que pueda mantener actualizada la información registrada en la plataforma.  | **Escenario 1: Actualización exitosa de datos del vehículo Dado que** el developer proporciona datos completos y válidos para actualizar, **Cuando** el developer realiza una solicitud PUT para modificar los datos de un vehículo, **Entonces** el sistema actualiza correctamente la información en la base de datos y confirma el éxito de la operación. **Escenario 2: Error por datos incompletos o erróneos Dado que** los datos enviados por el developer son incompletos o contienen errores de formato, **Cuando** el developer realiza una solicitud PUT para actualizar los datos, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error explicando los problemas detectados.  | EP07 |
| TS41 | Registro Usuario | **Como** developer, **quiero** crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, **para** que pueda permitir el registro de usuarios en la plataforma. | **Escenario 1: Registro exitoso de usuario Dado que** el developer proporciona un nombre, correo electrónico y contraseña válidos, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema crea el nuevo usuario y devuelve su información básica junto con una confirmación de éxito. **Escenario 2: Error por datos duplicados en el registro Dado que** el developer proporciona un correo electrónico que ya está registrado, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error indicando que el correo electrónico ya existe.  | EP07 |

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
            <td>Crear beneficios</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero informarme de beneficios de usar la plataforma, para usar la aplicación.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>2</td>
            <td>US32</td>
            <td>Crear planes de la aplicación</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero membresías o planes para informarme.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>3</td>
            <td>US02</td>
            <td>Desarrollar búsqueda de Contenido</td>
            <td>Como visitante del segmento de mecánicos automotrices quiero un plataforma web seccionada para mayor claridad de información.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>4</td>
            <td>US39</td>
            <td>Desarrollo de vehiculos compatibles</td>
            <td>Como visitante del segmento de mecánicos automotriz quiero saber qué tipo de vehículos es compatible con la aplicación para informarme.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>5</td>
            <td>US31</td>
            <td>Implementación de testimonios</td>
            <td>Como visitante del segmento conductores independientes quiero visualizar testimonios reales, para usar la aplicación.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>6</td>
            <td>US33</td>
            <td>Guía de conexiones</td>
            <td>Como visitante del segmento propietarios de vehículos urbanos quiero tener una guía de conexión vehículo-aplicación para usar la aplicación sin errores.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>7</td>
            <td>US38</td>
            <td>Preguntas frecuentes</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero informarme de preguntas frecuentes para validarlo con mis preguntas.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>8</td>
            <td>US30</td>
            <td>Desarrollar visualización y call to action</td>
            <td>Como visitante del segmento conductores independientes quiero entender de qué trata la plataforma, para saber si es útil para mí.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>9</td>
            <td>US36</td>
            <td>Visualización de creadores</td>
            <td>Como visitante del segmento de conductores independientes quiero saber quienes realizaron el proyecto, para informarme de estos.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>10</td>
            <td>US34</td>
            <td>Soporte y redes</td>
            <td>Como visitante del segmento conductores independientes quiero poder contactar a soporte para resolver mis dudas.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>11</td>
            <td>US37</td>
            <td>Soporte Multilingüe</td>
            <td>Como visitante del segmento de conductores independientes quiero poder seleccionar el idioma español o inglés para entender completamente la información proporcionada.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>12</td>
            <td>US35</td>
            <td>Diseño responsive</td>
            <td>Como visitante del segmento de conductores independientes quiero visualizar la landing page para desde cualquier dispositivo.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>13</td>
            <td>US05</td>
            <td>Alertas en tiempo real</td>
            <td>Como propietario de vehículo urbano, quiero una aplicación que me notifique si tengo complicaciones con mi vehículo en tiempo real para informarme del estado de mi vehículo.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>14</td>
            <td>US08</td>
            <td>Diagnóstico vehicular</td>
            <td>Como mecánico automotriz quiero un diagnóstico exacto de un vehículo para saber el estado actual de este.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>15</td>
            <td>US13</td>
            <td>Localizar un taller automotriz cercano</td>
            <td>Como conductor independiente, quiero localizar un taller mecánico cercano y confiable, para realizar arreglar o revisar mi vehículo.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>16</td>
            <td>US11</td>
            <td>Conexión bluetooth</td>
            <td>Como mecánico automotriz quiero conectarme a mi vehículo de manera rápida y precisa con bluetooth para tener información de mi vehículo en todo lugar y momento.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>17</td>
            <td>US14</td>
            <td>Visualización de fallas</td>
            <td>Como conductor independiente, quiero ver la descripción de la falla que tiene mi vehículo, para tomar medidas de mantenimiento.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>18</td>
            <td>US16</td>
            <td>Registrar mantenimiento realizado</td>
            <td>Como propietario de un vehículo urbano, quiero registrar un mantenimiento realizado de una falla, para tener un historial de los mismos.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>19</td>
            <td>US28</td>
            <td>Estado del vehículo</td>
            <td>Como propietario de vehículo urbano quiero información acerca del estado de mi vehículo para estar informado.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>20</td>
            <td>US06</td>
            <td>Visualización de desgaste vehícular</td>
            <td>Como conductor independiente quiero tener el registro del desgaste vehicular con estadísticas visuales y sencillas de entender para mantener mi vehículo en buen estado.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>21</td>
            <td>US27</td>
            <td>Pago de suscripciones</td>
            <td>Como propietario de vehículo urbano quiero pagar la suscripción con mi tarjeta por medio de la aplicación para un pago rápido.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>22</td>
            <td>US21</td>
            <td>Ver consumo de combustible</td>
            <td>Como propietario de vehículo urbano, quiero ver mi consumo de combustible promedio, para manejar de forma más eficiente.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>23</td>
            <td>US23</td>
            <td>Biblioteca automotriz</td>
            <td>Como mecánico automotriz quiero leer documentación acerca de métodos o avances tecnológicos en el sector para mantenerme informado.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>24</td>
            <td>US24</td>
            <td>Datos técnicos</td>
            <td>Como mecánico automotriz quiero visualizar el estado del vehículo con lenguaje técnico para un mejor entendimiento.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>25</td>
            <td>US07</td>
            <td>Modo conductor</td>
            <td>Como conductor independiente quiero que las alertas no obstaculicen la visión de mi pantalla para no interrumpir mi navegación.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>26</td>
            <td>US17</td>
            <td>Renovar suscripción</td>
            <td>Como conductor independiente, quiero renovar mi suscripción desde la app, para mantener el servicio activo.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>27</td>
            <td>US25</td>
            <td>Recordatorios de Revisiones técnicas</td>
            <td>Como conductor independiente quiero que la aplicación me recuerde el día de la próxima revisión técnica para recodarlo y estar alerta.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>28</td>
            <td>US26</td>
            <td>Registro de datos de vehículo</td>
            <td>Como conductor independiente, quiero guardar registros de los datos de mi vehículo para mantenerme informado.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>29</td>
            <td>US29</td>
            <td>Eliminación de vehículo</td>
            <td>Como mecánico automotriz quiero eliminar un vehículo de mi lista para actualizar mis vehículos.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>30</td>
            <td>US12</td>
            <td>Ingresar nuevo vehículo</td>
            <td>Como propietario de vehículo urbano quiero registrar mi vehículo para poder tener una lista ordenada de mis vehículos.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>31</td>
            <td>US09</td>
            <td>Guardado de datos y cierre de sesión</td>
            <td>Como propietario de vehículo urbano, quiero cerrar mi sesión de la aplicación para no dejar mis datos expuestos.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>32</td>
            <td>US01</td>
            <td>Registro de cuenta</td>
            <td>Como propietario de vehículo urbano, quiero crear una cuenta para ingresar a la aplicación.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>33</td>
            <td>US22</td>
            <td>Edición de información personal</td>
            <td>Como conductor independiente, quiero editar la información de mi perfil, para cambiar mis datos si lo veo necesario.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>34</td>
            <td>US04</td>
            <td>Inicio de sesión</td>
            <td>Como propietario de vehículo urbano quiero iniciar sesión en la aplicación para usar todas las funcionalidades de esta.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>35</td>
            <td>US10</td>
            <td>Historial de vehículos</td>
            <td>Como mecánico automotriz quiero poder tener un historial de vehículos para tener un próximo seguimiento de estos.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>36</td>
            <td>US15</td>
            <td>Estado de suscripción</td>
            <td>Como conductor independiente, quiero saber que suscripción poseo, para verificar mi estado de suscripción.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>37</td>
            <td>TS18</td>
            <td>Historial técnico de vehiculo</td>
            <td>Como developer, quiero obtener el historial técnico de un vehículo mediante una solicitud GET, para que los usuarios puedan revisar los eventos y mantenimientos anteriores del vehículo.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>38</td>
            <td>TS19</td>
            <td>Mecánico cercanos</td>
            <td>Como developer, quiero listar los mecánicos cercanos mediante una solicitud GET, para que los conductores puedan encontrar soporte técnico de forma rápida y confiable.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>39</td>
            <td>TS20</td>
            <td>Vehículos registrados</td>
            <td>Como developer, quiero registrar un nuevo vehículo enviando sus datos mediante una solicitud POST, para que pueda añadir vehículos al sistema y mantener actualizada la información disponible.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>40</td>
            <td>TS41</td>
            <td>Registro Usuario</td>
            <td>Como developer, quiero crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, para que pueda permitir el registro de usuarios en la plataforma.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>41</td>
            <td>TS40</td>
            <td>Actualizar datos de un vehículo</td>
            <td>Como developer, quiero actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, para que pueda mantener actualizada la información registrada en la plataforma.</td>
            <td>5</td>
        </tr>
    </table>
A continuación, se le hace presente el link del product backlog:

**Link:**  [Product Backlog](https://trello.com/invite/b/68363c9576438ad07b9ea838/ATTI8fb235d4573d555662751062510e05a86E507E27/vehix)

Además se le presenta la captura de imagen del proct backlog el cyual ha sido diseñado en la herramienta de Jira
![Trello](/assets/imgs/chapter-III/sprint-backlog-trello.png)
