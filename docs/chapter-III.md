# Capítulo III: Requirements Specification
## 3.1. To-Be Scenario Mapping
En esta sección se presenta el To-Be Scenario Mapping, una representación visual que describe cómo debería ser la experiencia ideal del usuario al interactuar con Vehix.
Segmento 1:

![to-be-scenario-mapping-segment-1](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-1.jpg)

Segemento 2: 

![to-be-scenario-mapping-segment-2](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-2.jpg)

Segemento 3:

![to-be-scenario-mapping-segment-3](/assets/imgs/chapter-III/to-be-scenario-mapping-segment-3.jpg)

## 3.2. User Stories

| Epic /Story ID | Título | Descripción | Criterios de aceptación | Relacionado con (Epic ID) |
| :---- | :---- | ----- | ----- | ----- |
| EP01 | Gestión de usuarios | \- | \- | \- |
| EP02 | Información de la plataforma (Landing Page) | \- | \- | \- |
| EP03 | Diagnóstico y mantenimiento vehicular | \- | \- | \- |
| EP04 | Conectividad del vehículo | \- | \- | \- |
| EP05 | Gestión de mecánicos | \- | \- | \- |
| EP05 | Suscripciones y pagos | \- | \- | \- |
| EP07 | Funcionalidades API RESTFUL (Developer) | \-  | \- | \- |
| US01 | Registro de cuenta | **Como** propietario de vehículo urbano, **quiero** crear una cuenta **para** ingresar a la aplicación | **Escenario 1: Registro exitoso Dado** que el propietario de vehículo urbano ingresa información válida, **Cuando** solicita el registro, **Entonces** su cuenta se activa correctamente y puede acceder a la plataforma. **Escenario 2: Registro con errores Dado** que el propietario de vehículo urbano ingresa información incompleta o incorrecta, **Cuando** intenta registrarse, **Entonces** el sistema le notifica sobre el problema y le permite corregirlo.  | EP01 |
| US02 | Navegación rápida | **Como** visitante del segmento mecánico automotriz **quiero** moverme rápidamente por las secciones de la plataforma **para** mayor comodidad. | **Escenario 1: Acceso fluido a secciones Dado** que el visitante mecánico automotriz se encuentra explorando la plataforma, **Cuando** solicita una sección específica, **Entonces** la información se carga rápidamente y sin obstáculos. **Escenario 2: Retroalimentación visual Dado** que el visitante mecánico automotriz se encuentra explorando en la plataforma, **Cuando** interactúa con una sección específica **Entonces** el sistema indica la interacción con un elemento navegable.  | EP02 |
| US03 | Evidencia de beneficios | **Como** visitante del segmento propietarios de vehículo urbano **quiero** ver los beneficios de usar la plataforma, **para** motivarme a probarla. | **Escenario 1: Visualización de beneficios Dado** que el visitante propietario de vehículo urbano navega por la landing page **Cuando** ve la información de los beneficios **Entonces** puede identificar rápidamente los precios y los beneficios de usar la plataforma. **Escenario 2: Identificación de planes Dado** que el visitante propietario de vehículo urbano navega por la landing page **Cuando** ve la información de los beneficios **Entonces** se identifica e interesa por la aplicación  | EP02 |
| US04 | Inicio de sesión | **Como** propietario de vehículo urbano **quiero** iniciar sesión con mi cuenta creada **para** usar las funcionalidades de mi aplicación | **Escenario 1: Inicio de sesión exitoso Dado** que el propietario de vehículo urbano ingresa credenciales válidas **Cuando** solicita acceder, **Entonces** puede usar la plataforma sin inconvenientes. **Escenario 2: Credenciales inválidas Dado**  que el propietario de vehículo urbano ingresa datos incorrectos, **Cuando** intenta ingresar, **Entonces** recibe un aviso y puede volver a intentarlo.  | EP01 |
| US05 | Alertas tempranas | **Como** propietario de vehículo urbano, **quiero** una aplicación que me alerte si hago una mala praxis en tiempo real **para** alargar la vida útil de mi carro. | **Escenario 1: Generación de alerta preventiva Dado** que el propietario de vehículo urbano realiza una acción que compromete su vehículo, **Cuando** la app lo detecta, **Entonces** le informa para que corrija el comportamiento. **Escenario 2: Conducción adecuada Dado** que el propietario de vehículo urbano no realiza una acción que compromete su vehículo **Cuando** la app monitorea el viaje, **Entonces** no se emite ninguna alerta. | EP03 |
| US06 | Historial de desgaste vehicular. | **Como** conductor independiente **quiero** saber el desgaste de mi vehículo en términos estadísticos **para** prevenir fallas. | **Escenario 1: Consulta con registros existentes Dado** que existen datos del vehículo, **Cuando** el conductor independiente accede a un diagnóstico del vehículo. **Entonces** puede visualizar estadísticas útiles sobre este **Escenario 2: Consulta sin registros previos Dado** que no hay datos aún del vehículo, **Cuando** el conductor independiente intenta acceder al historial **Entonces** el sistema informa que no hay datos disponibles. | EP03 |
| US07 | Modo conductor | **Como** conductor independiente **quiero** que las alertas no obstaculicen la visión de mi pantalla **para** concentrarme en mi ruta. | **Escenario 1: Activación del modo conductor Dado** que el conductor independiente se encuentra en ruta, **Cuando** el sistema detecta uso de aplicaciones externas en primer plano, **Entonces** las notificaciones se reducen a lo esencial y no distraen. **Escenario 2: Modo conductor desactivado Dado** que el usuario no está manejando, **Cuando** el sistema detecta inactividad, **Entonces** se permite mostrar toda la información de alertas. | EP03 |
| US08 | Diagnóstico vehicular PRO | **Como** mecánico automotriz **quiero** un diagnóstico técnico exacto de un vehículo **para** saber su estado actual. | **Escenario 1: Diagnóstico con datos completos Dado** que el vehículo está correctamente conectado al sistema, **Cuando** el mecánico automotriz realiza el diagnóstico, **Entonces** se genera un informe técnico e intuitivo. **Escenario 2: Diagnóstico rápido Dado** que el vehículo está correctamente conectado al sistema, **Cuando** el mecánico automotriz solicita un diagnóstico rápido, **Entonces** se genera un informe técnico e intuitivo generalizado.  | EP03 |
| US09 | Cerrar sesión | **Como** propietario de vehículo urbano, **quiero** cerrar mi sesión de la aplicación **para** no dejar mis datos expuestos. | **Escenario 1: Cierre exitoso Dado** que el propietario del vehículo ha terminado de usar la aplicación, **Cuando** solicita cerrar su sesión, **Entonces** el sistema revoca su acceso hasta el próximo inicio de sesión. **Escenario 2: Fallo al cerrar sesión Dado** que no se guardaron los datos de un vehículo **Cuando** el propietario de vehículo urbano intenta cerrar  sesión **Entonces** se le indica que guarde los datos.  | EP01 |
| US10 | Historial de vehículos | **Como** mecánico automotriz **quiero** poder tener un historial de vehículos diagnosticados **para** tener un próximo seguimiento. | **Escenario 1: Historial accesible Dado** que el mecánico automotriz ya ha diagnosticado vehículos previamente y tiene el plan PRO **Cuando** acceda a su lista de vehículo, **Entonces** puede ver la información almacenada por el vehículo. **Escenario 2: Sin historial previo Dado** que el mecánico automotriz aún no ha diagnosticado ningún vehículo, **Cuando** consulta su lista de vehículos, **Entonces** se le indica que no hay registros disponibles.  | EP03 |
| US11 | Conexión bluetooth | **Como** mecánico automotriz **quiero** que todos los datos del carro lleguen a la aplicación de manera rápida y precisa **para** tener un mejor diagnóstico. | **Escenario 1: Transmisión de datos correcta Dado** que el vehículo y el scanner están correctamente conectados por bluetooth, **Cuando** se realiza el escaneo, **Entonces** los datos se transmiten sin errores. **Escenario 2: Transmisión de datos incorrecta Dado** que el vehículo está apagado y el scanner conectado **Cuando** el mecanico automotriz intente leer el dispositivo por la aplicación **Entonces** cuando pase un tiempo sin conectar se recomendará verificar la conexión. | EP04 |
| US12 | Nuevo vehículo | **Como** propietario de vehículo urbano **quiero** registrar mi vehículo **para** poder tener una lista ordenada de mis vehículos. | **Escenario 1: Registro exitoso de vehículo Dado** que el propietario de vehículo urbano ingresa información válida del vehículo, **Cuando** realiza el registro, **Entonces** el sistema almacena correctamente los datos y los muestra en su lista. **Escenario 2: Error en el registro del vehículo Dado** que el propietario de vehículo urbano le falta datos **Cuando** intente registrar el vehículo. **Entonces** el sistema le notifica y solicita correcciones. **Escenario 2: Bloqueo de registro Dado** que el propietario de vehículo urbano ya registró un vehiculo y tiene el plan STANDARD **Cuando** intente registrar otro vehículo. **Entonces** el sistema muestra el motivo de | EP01 |
| US13 | Localizar un taller automotriz cercano | **Como** conductor independiente, **quiero** localizar un taller mecánico cerca de mí, **para** realizar mantenimiento a mi vehículo | **Escenario 1: Mecánicos disponibles en la zona Dado** que el sistema detecta la ubicación del usuario, **Cuando**  el conductor independiente solicita ayuda y activa el gps **Entonces** se le muestran las mejores opciones de mecácnicos cercanos y disponibles. **Escenario 2: No hay mecánicos cercanos Dado** que no hay mecánico registrados en el área, **Cuando** el conductor independiente solicita ayuda y activa el gps **Entonces** se le informa que no hay resultados y se sugieren zonas cercanas. **Escenario 3: No activa el GPS Dado** que el conductor independiente solicita ayuda **Cuando** no acepta la activación del gps **Entonces** no tendrá recomendaciones de registrados.  | EP05 |
| US14 | Ver descripción resumida de la falla del vehículo | **Como** conductor independiente, **quiero** ver la descripción simple de la falla que tiene mi vehículo, **para** llevarlo a mantenimiento | **Escenario 1: Falla identificada con resumen claro Dado** que el sistema ha detectado un error, **Cuando** el conductor independiente accede a los detalles del diagnóstico, **Entonces** se le presenta una explicación simple y comprensible. **Escenario 2: Falla identificada en tiempo real Dado** que el sistema ha detectado una falla durante el viaje, **Cuando** el conductor independiente reciba la notificación de falla **Entonces** se le presenta una explicación resumida y directa.  | EP03 |
| US15 | Ver estado de suscripción | **Como** conductor independiente, **quiero** saber el estado de mi suscripción, **para** evitar que el servicio se interrumpa. | **Escenario 1: Suscripción activa Dado** que el conductor independiente tiene una suscripción vigente, **Cuando** accede al perfil, **Entonces** se le muestra la fecha de renovación. **Escenario 2: Cambio de suscripción Dado** que la suscripción se encuentra activa **Cuando** el conductor independiente quiere cambiar de plan **Entonces** el sistema le mostrará la opción de cambiar de plan y sus nuevos beneficios. | EP06 |
| US16 | Registrar mantenimiento realizado | **Como** propietario de un vehículo urbano, **quiero** registrar un mantenimiento realizado de una falla, **para** tener un control de los mismos | **Escenario 1: Registro exitoso Dado** que el usuario completa la información del mantenimiento, **Cuando** lo registra, **Entonces** queda almacenado en el historial del vehículo. **Escenario 2: Información incompleta Dado** que al propietario de un vehículo le faltan rellenar datos clave, **Cuando** intenta registrar el mantenimiento, **Entonces** el sistema le solicita completar la información antes de continuar.  | EP03 |
| US17 | Renovar suscripción | **Como** conductor independiente, **quiero** renovar mi suscripción desde la app, **para** mantener el servicio activo. | **Escenario 1: Renovación exitosa Dado** que el conductor independiente cuenta con un método de pago válido, **Cuando** confirma la renovación, **Entonces** el sistema actualiza el estado de su suscripción. **Escenario 1: Renovación fallida Dado** que el los campos de pago están incompleta  **Cuando** el conductor independiente intente renovar, **Entonces** se notifica al usuario que falta agregar datos.  | EP06 |
| US18 | Diagnostico Standard | **Como** propietario de un vehículo urbano, **quiero** realizar un escaneo que me arroje los datos de falla de mi vehículo **para** estar alerta | **Escenario 1: Escaneo exitoso Dado** que el sistema logra comunicarse con el vehículo, **Cuando** el propietario de vehículo urbano realiza el escaneo, **Entonces** se presentan los datos de falla detectados de manera general e intuitiva. **Escenario 2: Limitación de escaneo STANDARD Dado** que el sistema logra comunicarse con el vehículo, **Cuando** el propietario de vehículo urbano realiza el escaneo, **Entonces** se presentarán las limitaciones del plan, bloqueando contenido PRO.  | EP05 |
| US19 | Historial técnico de vehiculo | **Como developer,** quiero obtener el historial técnico de un vehículo mediante una solicitud GET, **para que** los usuarios o mecánicos puedan revisar los eventos y mantenimientos anteriores. | **Escenario 1: Consulta con identificador válido Dado que** el identificador del vehículo proporcionado es válido, **Cuando** el developer realiza una solicitud GET para consultar el historial, **Entonces** el sistema devuelve el historial técnico correspondiente al vehículo. **Escenario 2: Consulta con identificador inexistente Dado que** el identificador proporcionado no corresponde a ningún vehículo registrado, **Cuando** el developer realiza una solicitud GET para consultar el historial, **Entonces** el sistema devuelve un mensaje de error informativo indicando que no se encontró el vehículo.  | EP07 |
| US20 | Mecánico cercanos | **Como developer,** quiero listar los mecánicos cercanos mediante una solicitud GET, **para que** los conductores puedan encontrar soporte técnico de forma rápida y confiable. | **Escenario 1: Ubicación válida con mecánicos disponibles Dado que** existen mecánicos cercano a la ubicación proporcionada, **Cuando** el developer realiza una solicitud GET indicando la ubicación, **Entonces** el sistema muestra una lista de mecánicos disponibles cercanos. **Escenario 2: Ubicación sin mecánicos registrados Dado que** no existen mecánicos registrados para la ubicación enviada, **Cuando** el developer realiza una solicitud GET, **Entonces** el sistema devuelve una lista vacía junto con un mensaje informativo indicando que no se encontraron mecánicos disponibles en esa área. | EP07 |
| US21 | Vehículos registrados | **Como developer,** quiero registrar un nuevo vehículo enviando sus datos mediante una solicitud POST, **para que** pueda añadir vehículos al sistema y mantener actualizada la información disponible. | **Escenario 1: Registro exitoso del vehículo Dado que** los datos del vehículo proporcionados por el developer están completos y son válidos, **Cuando** el developer realiza una solicitud POST para registrar un nuevo vehículo, **Entonces** el sistema guarda el vehículo en la base de datos y confirma el registro exitoso.  **Escenario 2: Error por datos incompletos o erróneos Dado que** los datos enviados por el developer están incompletos o contienen errores de formato, **Cuando** el developer realiza una solicitud POST para registrar el vehículo, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error explicando los problemas encontrados. | EP07 |
| US22 | Ver consumo de combustible | **Como** propietario de vehículo urbano, **quiero** ver mi consumo de combustible promedio, **para** manejar de forma más eficiente. | **Escenario 1: Datos disponibles Dado** que el sistema ha registrado un vehículo **Cuando** el propietario de vehículo urbano ingresa al inicio **Entonces** se visualiza el consumo intuitivo del combustible. **Escenario 2: Sin registros de consumo Dado** que aún no hay un vehículo registrado **Cuando** **el propietario de vehículo urbano** accede al perfil **Entonces** se le indica que no hay registro de vehículo.  | EP03 |
| US23 | Edición de información personal | **Como** conductor independiente, **quiero** editar la información de mi perfil, **para** cambiar mis datos si lo veo necesario | **Escenario 1: Edición exitosa Dado** que el  conductor independiente actualiza sus datos correctamente, **Cuando** los guarda, **Entonces** el sistema los almacena y refleja los cambios en su cuenta. **Escenario 2: Fallo en la edición Dado** que el conductor independiente introducen datos insuficientes **Cuando** se intenta guardar, **Entonces** el sistema informa del error y notifica rellenar los campo faltante  | EP01 |
| US24 | Biblioteca automotriz | **Como** mecánico automotriz **quiero** leer documentación acerca de métodos o avances tecnológicos en el sector **para** mantenerme informado. | **Escenario 1: Consulta de contenido disponible Dado** que el mecanico automotriz tiene plan PRO **Cuando** este accede a la biblioteca, **Entonces** puede leer o visualizar el material técnico y multimedia. **Escenario 2: Bloqueo de contenido Dado** que el mecanico automotriz tiene plan STANDARD **Cuando** este accede a la biblioteca, **Entonces** puede solo leer o material técnico. | EP05 |
| US25 | Datos técnicos | **Como** mecánico automotriz **quiero** visualizar el estado del vehículo con lenguaje técnico **para** un mejor entendimiento. | **Escenario 1: Visualizar estado del vehículo con lenguaje técnico** **Dado** que el mecánico automotriz accede al perfil técnico del vehículo **Cuando** navega entre las funcionalidades de diagnóstico **Entonces** visualiza todo con lenguaje técnico e intuitivo. **Escenario 2: Visualización de dashboards** **Dado** que el mecánico automotriz accede al perfil técnico del vehículo **Cuando** navega entre las funcionalidades predictivas **Entonces** predominará la visualización de dashboards. | EP05 |
| US26 | Recordatorios de Revisiones técnicas | **Como** conductor independiente **quiero** que la aplicación me recuerde el día de la próxima revisión técnica **para** estar alerta | **Escenario 1: Recordatorio programado Dado** que el conductor independiente ha configurado una fecha de revisión, **Cuando** se acerque la fecha, **Entonces** el sistema le envía una notificación anticipada. **Escenario 2: Registro Dado** que el usuario no ha configurado una revisión, **Cuando** intenta acceder al recordatorio, **Entonces** el sistema le sugiere registrar una revisión  | EP03 |
| US27 | Registro de datos. | **Como** conductor independiente, **quiero** guardar registros de los datos de mi vehículo **para** futuras revisiones técnicas o ventas. | **Escenario 1: Registro exitoso Dado** que el conductor independiente ha ingresado los datos correctamente, **Cuando** se almacenen en el sistema, **Entonces** el vehículo debe estar disponible en futuras consultas **Escenario 2: Falla en el registro Dado** que el conductor independiente ingresa datos y están incompletos **Cuando** intente guardarlos, **Entonces** el sistema informa acerca de completar los datos.  | EP03 |
| US28 | Pago de suscripciones | **Como** propietario de vehículo urbano **quiero** pagar la suscripción con mi tarjeta por medio de la aplicación **para** un pago rápido | **Escenario 1: Pago exitoso Dado** que los datos de la tarjeta son válidos, **Cuando** el propietario de vehículo urbano proceda con el pago, **Entonces** se confirma la suscripción al plan correspondiente. **Escenario 2: Fallo en el pago Dado** que los datos de la tarjeta no son válidos, **Cuando** el propietario de vehículo urbano proceda con el pago, **Entonces** el sistema pedirá corregir los campos. | EP06 |
| US29 | Estadística intuitiva | **Como** propietario de vehículo urbano **quiero** ver una gráfica acerca del estado de mi vehículo **para** estar alerta. | **Escenario 1: Datos visualizados correctamente Dado** que existe información registrada, **Cuando** el propietario de vehículo urbano accede a la sección de estadísticas, **Entonces** se muestra la información en forma gráfica clara y comprensible. **Escenario 2: Sin datos registrados Dado** que  el propietario de vehículo urbano aún no realiza el diagnóstico **Cuando** el usuario accede, **Entonces** el sistema mostrará la falta de datos. | EP03 |
| US30 | Eliminación de vehículo | **Como** conductor independiente **quiero** borrar un vehículo de mi historial **para** mantener actualizada mi información. | **Escenario 1: Eliminación confirmada Dado** que el conductor independientE decide eliminar un vehículo, **Cuando** confirma la acción, **Entonces** el vehículo ya no aparece en su lista. **Escenario 2: Cancelación de la eliminación Dado** que el conductor independiente arrepiente antes de confirmar, **Cuando** cancela la acción, **Entonces** el sistema no realiza ningún cambio. | EP01 |
| US31 | Contextualización de la plataforma | **Como** visitante del segmento conductores independientes **quiero** entender de qué trata la plataforma, **para** saber si es útil para mí.  | **Escenario 1: Información clara y accesible Dado** que el visitante del segmento conductores independientes accede a la landing page, **Cuando** revisa la sección informativa, **Entonces** comprende fácilmente la propuesta de valor. **Escenario 2: Visitante nuevo sin conocimientos técnicos Dado** que el visitante del segmento de conductores independientes no conoce de mecánica o diagnósticos automotrices, **Cuando** accede a la información general, **Entonces** debe encontrar una explicación sencilla sin tecnicismos. | EP02 |
| US32 | Testimonios | **Como** visitante del segmento conductores independientes **quiero** ver testimonios reales, **para** ganar confianza en la plataforma.  | **Escenario 1: Testimonios visibles Dado** que existen testimonios publicados, **Cuando** el visitante del segmento de conductores independientes accede a la sección, **Entonces** puede leer las experiencias compartidas. **Escenario 2: Visitante interesado en casos similares al suyo Dado** que el visitante del segmento de conductores independientes busca experiencias de usuarios con un perfil parecido, **Cuando** revisa los testimonios, **Entonces** se siente identificado con alguna de ellas.  | EP02 |
| US33 | Suscripciones | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** ver las membresías disponibles **para** informarme. | **Escenario 1: Visualización de planes activa Dado** que existen diferentes tipos de suscripciones, **Cuando** el visitante del segmento de propietarios de vehículos urbanos accede a la sección correspondiente, **Entonces** puede ver una comparación de beneficios por cada plan. **Escenario 2: Dudas sobre cuál plan elegir Dado** que el visitante del segmento de propietarios de vehículos urbanos no tiene claro qué plan le conviene, **Cuando** revisa la información, **Entonces** el sistema debe ofrecer orientación o una comparación destacada según el perfil del usuario. | EP02 |
| US34 | Video introductorio. | **Como** visitante del segmento propietarios de vehículos urbanos **quiero** ver un video introductorio **para** entender cómo funciona la aplicación. | **Escenario 1: Reproducción del video Dado** que el visitante del segmento de propietarios de vehículos urbanos está explorando la landing page, **Cuando** accede a la sección de presentación, **Entonces** el video se reproduce sin interrupciones. **Escenario 2: Visitante con conexión lenta Dado** que el visitante del segmento de propietarios de vehículos urbanos accede desde una red inestable, **Cuando** intenta ver el video, **Entonces** debe tener la opción de ver una versión de baja resolución o resumen en texto. **Escenario 3: Visitante con problemas auditivos Dado** que el visitante del segmento de propietarios de vehículos urbanos y tiene problemas con el sonido **Cuando** intenta ver el video, **Entonces** debe tener la opción de subtítulos.  | EP02 |
| US35 | Soporte y redes | **Como** visitante del segmento conductores independientes **quiero** poder contactar a soporte **para** resolver dudas antes de registrarse | **Escenario 1: Acceso exitoso a soporte Dado** que el visitante del segmento de conductores independiente tiene dudas, **Cuando** accede a la sección de contacto, **Entonces** puede enviar una consulta o mensaje fácilmente. **Escenario 2: Usuario solicita contacto directo Dado** que el visitante del segmento de conductores independiente necesita atención personalizada, **Cuando** accede a la sección de soporte. **Entonces** puede ver la opción del correo empresarial para contactarse personalmente. | EP02 |
| US36 | Diseño responsive | **Como** visitante del segmento de conductores independientes **quiero** un diseño que se adapte a mi pantalla **para** ver la información desde cualquier dispositivo. | **Escenario 1: Navegación desde dispositivo móvil Dado** que el visitante del segmento de conductores accede desde un teléfono o tablet, **Cuando** navega por la landing page, **Entonces** la información se visualiza correctamente sin necesidad de ampliar o mover contenido. **Escenario 2: Navegación desde ordenadores Dado** que el visitante del segmento de conductores accede desde un ordenador **Cuando** navega por la landing page, **Entonces** la información se visualiza correctamente sin necesidad de ampliar o mover contenido. | EP02 |
| US37 | Visualización de creadores | **Como** visitante del segmento de conductores independientes **quiero** conocer al equipo detrás del proyecto, **para** sentir más cercanía y confianza.  | **Escenario 1: Información del equipo publicada Dado** que se cuenta con una sección de "Quiénes somos", **Cuando** el visitante del segmento de conductores independientes accede, **Entonces** puede ver los nombres, perfiles o fotos del equipo. **Escenario 2: Interés en el respaldo profesional Dado** que el visitante de conductores independientes busca validar la experiencia del equipo, **Cuando** accede al perfil de un integrante, **Entonces** puede ver breves descripciones de roles o trayectoria..  | EP02 |
| US38 | Visualización de redes | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** conocer las redes sociales de la aplicación **para** informarme. | **Escenario 1: Acceso a redes sociales activo Dado** que el visitante del segmento de propietarios de vehículos urbanos quiere explorar más sobre la marca, **Cuando** accede aL footer **Entonces** encuentra enlaces funcionales a las plataformas activas. **Escenario 6: Realce visual de redes Dado** que el visitante del segmento de propietarios de vehículos urbanos quiere explorar más sobre la marca, **Cuando** pasa el cursor sobre un ícono de red social, **Entonces** el ícono se resalta visualmente indicando que es interactivo y clickeable.  | EP02 |
| US39 | Preguntas frecuentes. | **Como** visitante del segmento de propietarios de vehículos urbanos **quiero** una sección de preguntas frecuentes **para** no tener dudas. | **Escenario 1: Visualización de la sección de preguntas frecuentes Dado** que el visitante del segmento de propietarios de vehículos urbanos quiere resolver sus dudas rápidamente,  **Cuando** accede a la sección de preguntas frecuentes, **Entonces** ve una lista clara de preguntas y respuestas relevantes sobre la aplicación. **Escenario 2: Interacción con preguntas expandibles Dado que** el visitante del segmento de propietarios de vehículos urbanos explora las preguntas frecuentes, **Cuando** hace clic sobre una pregunta, **Entonces** la respuesta se despliega de manera inmediata, sin recargar la página.  | EP02 |
| US40 | Seccion de vehiculos compatibles | **Como** visitante del segmento de mecánicos automotriz **quiero** saber qué tipo de vehículos es compatible con la aplicación **para** informarme. | **Escenario 1: Visualización de la lista de vehículos compatibles Dado que** el visitante del segmento de mecánicos desea informarse sobre la compatibilidad, **Cuando** accede a la sección de vehículos compatibles, **Entonces** visualiza una lista clara que incluye marcas, modelos o tipos de vehículos soportados. **Escenario 2: Visualización destacada de tipos de vehículos mediante imágenes Dado que** el visitante  del segmento de mecánicos explora la sección de vehículos compatibles, **Cuando** accede a la lista de tipos de vehículos, **Entonces** visualiza íconos o imágenes representativas que mejoran la identificación rápida y facilitan la comprensión de los vehículos compatibles. | EP02 |
| US41 | Actualizar datos de un vehículo | **Como** developer, **quiero** actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, **para** que pueda mantener actualizada la información registrada en la plataforma.  | **Escenario 1: Actualización exitosa de datos del vehículo Dado que** el developer proporciona datos completos y válidos para actualizar, **Cuando** el developer realiza una solicitud PUT para modificar los datos de un vehículo, **Entonces** el sistema actualiza correctamente la información en la base de datos y confirma el éxito de la operación. **Escenario 2: Error por datos incompletos o erróneos Dado que** los datos enviados por el developer son incompletos o contienen errores de formato, **Cuando** el developer realiza una solicitud PUT para actualizar los datos, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error explicando los problemas detectados.  | EP07 |
| US42 | Registro Usuario | **Como** developer, **quiero** crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, **para** que pueda permitir el registro de usuarios en la plataforma. | **Escenario 1: Registro exitoso de usuario Dado que** el developer proporciona un nombre, correo electrónico y contraseña válidos, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema crea el nuevo usuario y devuelve su información básica junto con una confirmación de éxito. **Escenario 2: Error por datos duplicados en el registro Dado que** el developer proporciona un correo electrónico que ya está registrado, **Cuando** el developer realiza una solicitud POST para registrar un usuario, **Entonces** el sistema rechaza la solicitud y devuelve un mensaje de error indicando que el correo electrónico ya existe.  | EP07 |

## 3.3. Impact Mapping
![impactmapping](/assets/imgs/chapter-III/impact-map.png)
## 3.4. Product Backlog
<table>
        <tr>
          <td><strong>#Orden</strong></td>
          <td><strong>User Stoy Id</strong></td>
          <td><strong>Título</strong></td>
          <td><strong>Descripción</strong></td>
          <td><strong>Story Points
(1 / 2 / 3 / 5 / 8)</strong></td>
        </tr>
        <tr>
            <td>1</td>
            <td>US02</td>
            <td>Navegación rápida</td>
            <td>Como visitante del segmento mecánico automotriz quiero moverme rápidamente por las secciones de la plataforma para mayor comodidad.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>2</td>
            <td>US03</td>
            <td>Evidencia de beneficios</td>
            <td>Como visitante del segmento propietarios de vehículo urbano quiero ver los beneficios de usar la plataforma, para motivarme a probarla.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>3</td>
            <td>US31</td>
            <td>Contextualización de la plataforma</td>
            <td>Como visitante del segmento conductores independientes quiero entender de qué trata la plataforma, para saber si es útil para mí.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>4</td>
            <td>US32</td>
            <td>Testimonios</td>
            <td>Como visitante del segmento conductores independientes quiero ver testimonios reales, para ganar confianza en la plataforma.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>5</td>
            <td>US33</td>
            <td>Suscripciones</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero ver las membresías disponibles para informarme.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>6</td>
            <td>US34</td>
            <td>Video introductorio</td>
            <td>Como visitante del segmento propietarios de vehículos urbanos quiero ver un video introductorio para entender cómo funciona la aplicación.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>7</td>
            <td>US35</td>
            <td>Soporte y redes</td>
            <td>Como visitante del segmento conductores independientes quiero poder contactar a soporte para resolver dudas antes de registrarse</td>
            <td>3</td>
        </tr>
        <tr>
            <td>8</td>
            <td>US36</td>
            <td>Diseño responsive</td>
            <td>Como visitante del segmento de conductores independientes quiero un diseño que se adapte a mi pantalla para ver la información desde cualquier dispositivo.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>9</td>
            <td>US37</td>
            <td>Visualización de creadores</td>
            <td>Como visitante del segmento de conductores independientes quiero conocer al equipo detrás del proyecto, para sentir más cercanía y confianza.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>10</td>
            <td>US38</td>
            <td>Visualización de redes</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero conocer las redes sociales de la aplicación para informarme.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>11</td>
            <td>US39</td>
            <td>Preguntas frecuentes</td>
            <td>Como visitante del segmento de propietarios de vehículos urbanos quiero una sección de preguntas frecuentes para no tener dudas.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>12</td>
            <td>US40</td>
            <td>Seccion de vehiculos compatibles</td>
            <td>Como visitante del segmento de mecánicos automotriz quiero saber qué tipo de vehículos es compatible con la aplicación para informarme.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>13</td>
            <td>US01</td>
            <td>Registro de cuenta</td>
            <td>Como propietario de vehículo urbano, quiero crear una cuenta para ingresar a la aplicación.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>14</td>
            <td>US04</td>
            <td>Inicio de sesión</td>
            <td>Como propietario de vehículo urbano quiero iniciar sesión con mi cuenta creada para usar las funcionalidades de mi aplicación.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>15</td>
            <td>US05</td>
            <td>Alertas tempranas</td>
            <td>Como propietario de vehículo urbano, quiero una aplicación que me alerte si hago una mala praxis en tiempo real para alargar la vida útil de mi carro.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>16</td>
            <td>US09</td>
            <td>Cerrar sesión</td>
            <td>Como propietario de vehículo urbano, quiero cerrar mi sesión de la aplicación para no dejar mis datos expuestos.</td>
            <td>1</td>
        </tr>
        <tr>
            <td>17</td>
            <td>US12</td>
            <td>Nuevo vehículo</td>
            <td>Como propietario de vehículo urbano quiero registrar mi vehículo para poder tener una lista ordenada de mis vehículos.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>18</td>
            <td>US16</td>
            <td>Registrar mantenimiento realizado</td>
            <td>Como propietario de un vehículo urbano, quiero registrar un mantenimiento realizado de una falla, para tener un control de los mismos.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>19</td>
            <td>US22</td>
            <td>Ver consumo de combustible</td>
            <td>Como propietario de vehículo urbano, quiero ver mi consumo de combustible promedio, para manejar de forma más eficiente.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>20</td>
            <td>US28</td>
            <td>Pago de suscripciones</td>
            <td>Como propietario de vehículo urbano quiero pagar la suscripción con mi tarjeta por medio de la aplicación para un pago rápido.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>21</td>
            <td>US29</td>
            <td>Estadística intuitiva</td>
            <td>Como propietario de vehículo urbano quiero ver una gráfica acerca del estado de mi vehículo para estar alerta.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>22</td>
            <td>US06</td>
            <td>Historial de desgaste vehicular</td>
            <td>Como conductor independiente quiero saber el desgaste de mi vehículo en términos estadísticos para prevenir fallas.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>23</td>
            <td>US07</td>
            <td>Modo conductor</td>
            <td>Como conductor independiente quiero que las alertas no obstaculicen la visión de mi pantalla para concentrarme en mi ruta.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>24</td>
            <td>US13</td>
            <td>Localizar un taller automotriz cercano</td>
            <td>Como conductor independiente, quiero localizar un taller mecánico cerca de mí, para realizar mantenimiento a mi vehículo.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>25</td>
            <td>US14</td>
            <td>Ver descripción resumida de la falla del vehículo</td>
            <td>Como conductor independiente, quiero ver la descripción simple de la falla que tiene mi vehículo, para llevarlo a mantenimiento.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>26</td>
            <td>US15</td>
            <td>Ver estado de suscripción</td>
            <td>Como conductor independiente, quiero saber el estado de mi suscripción, para evitar que el servicio se interrumpa.</td>
            <td>2</td>
        </tr>
        <tr>
            <td>27</td>
            <td>US17</td>
            <td>Renovar suscripción</td>
            <td>Como conductor independiente, quiero renovar mi suscripción desde la app, para mantener el servicio activo.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>28</td>
            <td>US23</td>
            <td>Edición de información personal</td>
            <td>Como conductor independiente, quiero editar la información de mi perfil, para cambiar mis datos si lo veo necesario.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>29</td>
            <td>US26</td>
            <td>Recordatorios de Revisiones técnicas</td>
            <td>Como conductor independiente quiero que la aplicación me recuerde el día de la próxima revisión técnica para estar alerta.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>30</td>
            <td>US27</td>
            <td>Registro de datos</td>
            <td>Como conductor independiente, quiero guardar registros de los datos de mi vehículo para futuras revisiones técnicas o ventas.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>31</td>
            <td>US30</td>
            <td>Eliminación de vehículo</td>
            <td>Como conductor independiente quiero borrar un vehículo de mi historial para mantener actualizada mi información.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>32</td>
            <td>US08</td>
            <td>Diagnóstico vehicular PRO</td>
            <td>Como mecánico automotriz quiero un diagnóstico técnico exacto de un vehículo para saber su estado actual.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>33</td>
            <td>US10</td>
            <td>Historial de vehículos</td>
            <td>Como mecánico automotriz quiero poder tener un historial de vehículos diagnosticados para tener un próximo seguimiento.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>34</td>
            <td>US11</td>
            <td>Conexión bluetooth</td>
            <td>Como mecánico automotriz quiero que todos los datos del carro lleguen a la aplicación de manera rápida y precisa para tener un mejor diagnóstico.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>35</td>
            <td>US18</td>
            <td>Diagnostico Standard</td>
            <td>Como propietario de un vehículo urbano, quiero realizar un escaneo que me arroje los datos de falla de mi vehículo para estar alerta.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>36</td>
            <td>US24</td>
            <td>Biblioteca automotriz</td>
            <td>Como mecánico automotriz quiero leer documentación acerca de métodos o avances tecnológicos en el sector para mantenerme informado.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>37</td>
            <td>US25</td>
            <td>Datos técnicos</td>
            <td>Como mecánico automotriz quiero visualizar el estado del vehículo con lenguaje técnico para un mejor entendimiento.</td>
            <td>3</td>
        </tr>
        <tr>
            <td>38</td>
            <td>US19</td>
            <td>Historial técnico de vehiculo</td>
            <td>Como developer, quiero obtener el historial técnico de un vehículo mediante una solicitud GET, para que los usuarios o mecánicos puedan revisar los eventos y mantenimientos anteriores.</td>
            <td>8</td>
        </tr>
        <tr>
            <td>39</td>
            <td>US20</td>
            <td>Mecánico cercanos</td>
            <td>Como developer, quiero listar los mecánicos cercanos mediante una solicitud GET, para que los conductores puedan encontrar soporte técnico de forma rápida y confiable.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>40</td>
            <td>US21</td>
            <td>Vehículos registrados</td>
            <td>Como developer, quiero registrar un nuevo vehículo enviando sus datos mediante una solicitud POST, para que pueda añadir vehículos al sistema y mantener actualizada la información disponible.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>41</td>
            <td>US41</td>
            <td>Actualizar datos de un vehículo</td>
            <td>Como developer, quiero actualizar los datos técnicos de un vehículo enviando la información editada mediante una solicitud PUT, para que pueda mantener actualizada la información registrada en la plataforma.</td>
            <td>5</td>
        </tr>
        <tr>
            <td>42</td>
            <td>US42</td>
            <td>Registro Usuario</td>
            <td>Como developer, quiero crear un nuevo usuario enviando su nombre, correo electrónico y contraseña, para que pueda permitir el registro de usuarios en la plataforma.</td>
            <td>5</td>
        </tr>
    </table>
    
**Link:**  [Product Backlog](https://antonionavarroch24.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog?epics=visible&atlOrigin=eyJpIjoiYjc5OTdkY2Q0ZTlmNGFmN2FkYWIxNWU3Zjk0NzY1MWEiLCJwIjoiaiJ9)

![Jira](/assets/imgs/chapter-III/jira.png)

