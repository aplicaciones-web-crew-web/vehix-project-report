# Capítulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.
En esta sección se detallan las herramientas y plataformas que se utilizaron para el desarrollo de la aplicacion Vehix
## Gestión del Proyecto
La gestión del proyecto es clave para coordinar actividades, tareas y equipos, asegurando que el proyecto Vehix avance dentro de los tiempos y objetivos planteados.

**Modelo SaaS Web:** 

Durante el desarrollo, se utilizó una solución basada en la nube accesible vía navegador, permitiendo la planificación, seguimiento de tareas y colaboración, sin la necesidad de instalar la aplicaion en las computadoras de los usuarios.
## Gestión de Requisitos
Esta disciplina asegura que el sistema cumpla con las necesidades de los usuarios y partes interesadas, mediante el levantamiento y seguimiento de requisitos funcionales y no funcionales.

**Pivotal Tracker:**  

Utilizada para gestionar historias de usuario, agruparlas en épicas y asignarles prioridades. Proporciona visibilidad en tiempo real del progreso del equipo y permite ajustes dinámicos en el flujo de trabajo.
## Diseño UX/UI del Producto
El diseño centrado en el usuario fue esencial para Vehix. Nuestro objetivo fue crear una interfaz intuitiva, accesible desde web y dispositivos móviles.
**Herramientas utilizadas:**
- **Uxpressia:**  
  Nos permitió desarrollar mapas de empatía, perfiles de usuario (User Personas) y Customer Journey Maps.
- **MIRO:**  
  Facilitó sesiones colaborativas para ideación, mapas mentales y estructuración del diseño de experiencia.
- **Figma:**  
  Herramienta central para la creación de prototipos interactivos y diseño visual responsive.
- **Lucidchart:**  
  Usada para la elaboración de diagramas UML, mapas mentales y arquitecturas del sistema.
- **Overflow:**  
  Utilizada para diseñar flujos de usuario (User Flows) y visualizar recorridos dentro de la aplicación.
## Desarrollo de Software
- **GitHub:**  
  Repositorio central de código fuente y seguimiento del control de versiones del proyecto Vehix.
- **Git:**  
  Herramienta instalada localmente que nos permitió gestionar cambios, crear ramas y coordinar el trabajo colaborativo.
- **WebStorm:**  
  IDE utilizado principalmente para desarrollo en frontend con HTML, CSS, JavaScript y Vue.js.
- **Rider:**  
  IDE empleado para el backend con C# y ASP.NET, donde se implementó el servicio web que alimenta a la aplicación Vehix.
## Pruebas de Software
El objetivo de esta fase fue validar y verificar el correcto funcionamiento del sistema.

**Lenguaje Gherkin:**  

Utilizamos este lenguaje específico de dominio (DSL) para redactar historias de usuario en formato estructurado, permitiendo automatizar pruebas basadas en escenarios.
Esto facilitó una verificación sistemática del comportamiento esperado de la aplicación.
## Documentación del Software

Incluye todo el material que describe el funcionamiento del sistema y cómo utilizarlo. La documentación fue elaborada tanto para usuarios finales como para el equipo técnico, y se integró como parte del repositorio del proyecto.
### 5.1.2. Source Code Management.
En esta sección se describe cómo se gestionaron las modificaciones al código del sistema **Vehix**, así como las convenciones empleadas para los commits y las versiones liberadas a lo largo del ciclo de desarrollo.

### Plataforma de Control de Versiones

Para el control y seguimiento del código fuente, se utilizó **GitHub** como plataforma centralizada. Allí se crearon distintos repositorios independientes para las principales partes del sistema: landing page, backend (servicio web), frontend y documentación técnica. El control de versiones se realizó de forma distribuida mediante **Git**, instalado localmente por cada integrante del equipo.

### Flujo de Trabajo Git (GitFlow)

Se adoptó el modelo de ramificación **GitFlow**, debido a su capacidad para mantener el código organizado y facilitar el trabajo colaborativo. Esta metodología define dos tipos de ramas:

#### Ramas Principales

- `main`: Contiene la versión estable y lista para producción del sistema Vehix. Todo código integrado aquí representa una nueva entrega oficial del producto.
- `develop`: Es la rama donde se integran funcionalidades completadas y testeadas. Sirve como entorno previo a producción para preparar nuevos lanzamientos.

#### Ramas de Apoyo

- `feature`: Se crean desde `develop` para el desarrollo de nuevas funcionalidades específicas. Una vez finalizadas, se integran nuevamente en `develop`.
- `release`: Generadas desde `develop` para preparar una nueva versión estable. Incluyen ajustes menores, corrección de bugs y preparación para despliegue.
- `hotfix`: Se crean directamente desde `main` cuando se requiere resolver errores críticos en producción. Una vez resueltos, se integran tanto en `main` como en `develop`.

### Versionado Semántico (Semantic Versioning)

El proyecto implementa el estándar **Semantic Versioning 2.0.0**, permitiendo una numeración clara y predecible de versiones mediante el esquema `X.Y.Z`, donde:

- `Z` (Patch): Se incrementa por correcciones menores sin afectar compatibilidad.
- `Y` (Minor): Se incrementa cuando se agregan nuevas funcionalidades compatibles.
- `X` (Major): Se incrementa cuando se introducen cambios que rompen compatibilidad con versiones anteriores.

**Ejemplos de nombres de ramas release:**
- `release-1.0.5`
- `release-2.1.4`
- `release-2.2.1`

### Commits Convencionales (Conventional Commits)

Para mantener un historial claro y significativo de los cambios, se empleó el estándar **Conventional Commits**, con la siguiente estructura:

``` <type>[opcional scope]: <descripción> ```

```[optional body]```

```[optional footer]```

#### Tipos de Commit (`type`):

- `feat`: Nueva funcionalidad.
- `fix`: Corrección de errores.
- `docs`: Cambios en la documentación.
- `refactor`: Reestructuración sin alterar comportamiento.
- `perf`: Mejoras de rendimiento.
- `chore`: Tareas menores sin impacto funcional.
- `build`: Cambios relacionados a dependencias o configuración.

#### Otros Campos:

- **scope** *(opcional)*: Indica qué módulo o componente fue modificado.
- **description** *(obligatorio)*: Breve explicación del cambio, en minúsculas y forma imperativa.
- **body** *(opcional)*: Detalles adicionales del cambio.
- **footer** *(opcional)*: Información extra sobre _breaking changes_ u otros avisos.

Este enfoque facilita la trazabilidad, automatización del versionado y claridad en las revisiones por parte del equipo de desarrollo de *Vehix*.
### Commits Convencionales (Conventional Commits)

### 5.1.3. Source Code Style Guide & Conventions.
### 5.1.4. Software Deployment Configuration.
## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
<table>
	<tbody>
		<tr>
			<td><strong>Sprint #</strong></td>
			<td>Sprint 1</td>
		</tr>
		<tr>
			<td colspan="2"><strong>Spring Planing Background</strong></td>
		</tr>
		<tr>
			<td><strong>Date</strong></td>
			<td>2025-05-22</td>
		</tr>
		<tr>
			<td><strong>Time</strong></td>
			<td>4:50 PM</td>
		</tr>
		<tr>
			<td><strong>Location</strong></td>
			<td>Remote mode through the GitHub platform</td>
		</tr>
		<tr>
			<td colspan="2"><strong>Prepared by</strong></td>
		</tr>
		<tr>
			<td><strong>Attends (to planinning meeting)</strong></td>
			<td>All members of crewtech</td>
		</tr>
		<tr>
			<td><strong>Sprint 0 Review Summary</strong></td>
			<td>Since this is our initial development sprint, a sprint summary has not yet been completed.</td>
		</tr>
		<tr>
			<td><strong>Sprint 0 Retrospective Summary</strong></td>
			<td>Since this is our initial development sprint, a sprint summary has not yet been completed.</td>
		</tr>
		<tr>
			<td colspan="2"><strong>Sprint Goal & User Stories</strong></td>
		</tr>
		<tr>
			<td><strong>Spritn 1 Goal</strong></td>
			<td>We're focusing on building our landing page. We believe this contributes to the sustainability of the product within our organization. This will be confirmed when we see a significant increase in engagement with our landing page.</td>
		</tr>
		<tr>
			<td><strong>Sprint 1 Velocity</strong></td>
			<td>12</td>
		</tr>
		<tr>
			<td><strong>Sum of Story points</strong></td>
			<td>26</td>
		</tr>
	</tbody>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators.

| Team Member (Last Name, First Name) | GitHub Username | Landing page |
| ------------------------------------|-----------------|-------------------------------------------|
| Rios Piñan, Dayro Richard|Addicted2u| C | 
| Julca Minaya, Sergio Gino|sergioJM05| C |
| Navarro Chinga, Antonio Jhair | AntonioNavarro24 | L | 
| Baca Camargo, Vitaly Arturo | Mr-Code-Star | C | 
| Elescano Leon, Piero Hugo | PieroHugo | C |


#### 5.2.1.3. Sprint Backlog 1


<table>
	<tbody>
		<tr>
			<td><strong>Sprint #</strong></td>
			<td colspan="7">Sprint 1</td>
		</tr>
		<tr>
			<td colspan="2"><strong>User Story</strong></td>
			<td colspan="6"><strong>Work-item / Task</strong></td>
		</tr>
		<tr>
			<td><strong>Id</strong></td>
			<td><strong>Title</strong></td>
			<td><strong>Id</strong></td>
			<td><strong>Title</strong></td>
			<td><strong>Description</strong></td>
			<td><strong>Estimation (Hours)</strong></td>
			<td><strong>Assisgned To</strong></td>
			<td><strong>Status (To-do / In- Porcess / To-review / Done)</strong></td>
		</tr>
		<tr>
			<td rowspan="3">EP02-US02</td>
			<td rowspan="3">Navegación rápida</td>
			<td>T1</td>
			<td>Añadir lista de etiquetas</td>
			<td>Se añadirán las etiquetas de “Home”,” Subscriptions”,” Benefits”,” Testimonial”, ¿” Who are we?”, “FAQ”, “Support” y “Compatitbility”</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Vinculación de secciones y estilos</td>
			<td>Se concatenan las etiquetas con sus secciones respectivas, y se añaden estilos correspondientes</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Nav-var responsive</td>
			<td>Se añade las propiedades en css para el diseño responsive</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>EP02-US03</td>
			<td>Evidencia de beneficios</td>
			<td>T4</td>
			<td>Añadir lista de beneficios y estilo</td>
			<td>Se añade una lista de beneficios de usar la plataforma y estilos correspondientes</td>
			<td>0.5</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US31</td>
			<td rowspan="2">Contextualización de la plataforma</td>
			<td>T5</td>
			<td>Añadir descripción de la aplicación</td>
			<td>Se agrega un párrafo atractivo y concreto para el visitante</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T6</td>
			<td>Añadir imágenes y estilos</td>
			<td>Se agrega imagen referencial de dispositivos compatibles y estilos correspondientes</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US32</td>
			<td rowspan="2">Testimonios</td>
			<td>T7</td>
			<td>Añadir comentarios</td>
			<td>Se agrega un comentario por cada usuario acerca de su experiencia con la aplicación</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T8</td>
			<td>Agregar imágenes de usuarios y estilos</td>
			<td>Se agrega fotos de los usuarios que han dejado sus comentarios y se agrega estilos correspondientes</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US33</td>
			<td rowspan="2">Suscripciones</td>
			<td>T9</td>
			<td>Añadir tipo de plan y precios</td>
			<td>Se agregan los títulos de cada plan y sus precios</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T10</td>
			<td>Añadir beneficios y estilos.</td>
			<td>Se listan los beneficios de cada plan y se añaden los estilos correspondientes</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US34</td>
			<td rowspan="2">Video introductorio</td>
			<td>T11</td>
			<td>Creación de video</td>
			<td>Se sube video de guía a YouTube acerca de cómo funciona la aplicación</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T12</td>
			<td>Añadir video y estilo</td>
			<td>Se agrega el link del video de YouTube junto al estilo predefinido</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US35</td>
			<td rowspan="2">Soporte y redes</td>
			<td>T13</td>
			<td>Añadir redes</td>
			<td>Se añaden iconos de las redes sociales de la empresa</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T14</td>
			<td>Añadir sección de registro y estilos</td>
			<td>Se añade formulario y se añade los estilos correspondietes</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US36</td>
			<td rowspan="2">Diseño responsive</td>
			<td>T15</td>
			<td>Correccion de errores</td>
			<td>Se corrigen los errores de diseño responsive</td>
			<td>2</td>
			<td>Antonio Nvarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T16</td>
			<td>Añadir propiedades </td>
			<td>Se añaden propiedades principales de estilos y de diseño responsive faltantes.</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US37</td>
			<td rowspan="2">Visualización de creadores</td>
			<td>T17</td>
			<td>Añadir imágenes y estilos</td>
			<td>Se añade las fotos de cada integrante y se agregan el estilo correspondiente.</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T18</td>
			<td>Añadir descripción</td>
			<td>Se añaden descripciones de cada integrante</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US38</td>
			<td rowspan="2">Visualización de redes</td>
			<td>T19</td>
			<td>Añadir pie de pagina</td>
			<td>Se añade iconos referenciales de cada red social de la empresa</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T20</td>
			<td>Añadir estilo al pie de pagina</td>
			<td>Se añaden estilos predefinidos al pie de pagina</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP02-US39</td>
			<td rowspan="3">Preguntas frecuentes</td>
			<td>T21</td>
			<td>Añadir preguntas</td>
			<td>Se añaden preguntas frecuentes de los usuarios</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T22</td>
			<td>Añadir respuestas</td>
			<td>Se añade mínimo un párrafo de descripción a cerca de la pregunta correspondiente</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T23</td>
			<td>Añadir estilo</td>
			<td>Se añade estilos correspondientes y efecto acordeón</td>
			<td>1</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US40</td>
			<td rowspan="2">Sección de vehículos compatibles</td>
			<td>T24</td>
			<td>Añadir información de vehículos compatibles</td>
			<td>Se añade breve información de vehículos compatibles, resaltando el año y tipo de combustible.</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T25</td>
			<td>Añadir imagen referencial</td>
			<td>Se añade imagen referencial de carros correspondientes a la descripción.</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
	</tbody>
</table>

#### 5.2.1.4. Development Evidence for Sprint Review.

Para el desarrollo del sprint 1, se ha implementado la landing page, previamente habiendo hecho el diseño en Figma. Se desarrollaron los features correspondientes, entre ellos las secciones de nuestra landing page y el cambio de idioma entre inglés y español.

| Repository | Branch | Commit Id | Commit Messaage | Commit Message Body | Commited on |
|------------|--------|-----------|-----------------|---------------------|-------------|
| sergioJM05/vehix-landing-page | main | cdb2968 | initial commit | - | 25/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | cdb2968 | initial commit | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | cdb2968 | initial commit | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | a8c3226 | docs: create route | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | - | Deleted branch | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | cdb2968 | Initial commit | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | 16c4996 | docs: create folder | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | 57e8011 | chore: add index.html | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | 74ed382 | chore: add index_es.html | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | 9e711c3 | chore: add structure landing | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/rapid-navigation | 9e711c3 | chore: add structure landing | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/rapid-navigation | 2b8d4cc | feat: add rapid navigation | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/rapid-navigation | 3b956da | feat: add rapid navigation in spanish | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | 948c856 | feat: add rapid navigation in en and es | - | 27/04/2025 |
| PieroHugo/vehix-landing-page | develop | 948c856 | feature/benefits-evidence | - | 27/04/2025 |
| PieroHugo/vehix-landing-page | feature/benefits-evidence | 948c856 | feature: add benefits evidence | - | 27/04/2025 |
| PieroHugo/vehix-landing-page | develop | 7953626 | feat: add benefits evidence | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/suscriptions | 7953626 | feat: add benefits evidence | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/suscriptions | 44269a1 | feat: add subscriptions | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/suscriptions | c8679c2 | feat: add subscriptions in spanish | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/suscriptions | c0c1b0e | chore: delete image | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | b0b9f54 | feat: add suscriptions | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/testimonials | b0b9f54 | feat: add suscriptions | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/testimonials | cb5f5ea | feat: add testimonials | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/testimonials | 844597c | feat: add testimonials in spanish | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | b4dbc40 | feat: add testimonials section in en and es | feature/testimonials | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | b4dbc40| feat: add testimonials section in en and es | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | 47e536f | feat: add creators visualization | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | aad6ed6 | feat: add creators visualization in spanish | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | 851efe1 | feat: update route images | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | e654ed2 | feat: fix assets imgs route | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | 57e1d39 | feat: update images routes | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/creators-visualization | aad1fbe | feat: update piero image route | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | develop | 9747cdc | feat: add creators visualization section | feature/creators-visualization | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | feature/structure-landing | b5a682e | chore: add app | - | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | feature/structure-landing | 1666534 | feat: add app.js | - | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | develop | f64e550 | feat: add app.js | - | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | feature/frequently-asked-questions | 9c472b7 | feat: add frequently asked questions | - | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | feature/frequently-asked-questions | 1c00ea3 | feat: add frequently asked questions | - | 27/04/2025 |
| Mr-Code-star/vehix-landing-page | develop | 26d577f | feat: add frequently asked questions section in en and es | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/structure-landing | 6cb28b6 | chore: add style | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/structure-landing | 4a35460 | feat: add styles | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | develop | 85b808f | feat: update structure landing | feature/structure-landing | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/compatible-vehicles | 85b808f | feat: update structure landing | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/compatible-vehicles | edd3dd8 | feat: add compatible vehicles en | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/compatible-vehicles | 8451d6b | feat: add compatible vehicles (es) | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/compatible-vehicles | ee06174 | chore: add images | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | feature/compatible-vehicles | d87a182 | chore: add images | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | develop | 69f9140 | feat: add compatible vehicles (en & es) and add images | feature/compatible-vehicles | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/support-and-networks | 69f9140 | feat: add compatible vehicles (en & es) and add images | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/structure-landing | fd209ac | feat: add style | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | 004dc84  | feat: add style | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/support-and-networks | 71cdb59  | feat: add support and networks | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/support-and-networks | 3af7b77  | feat: add support and networks in spanish | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | c11dce8   | feat: add support and networks section in en and es | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/network-visualization | c11dce8  | feat: add support and networks section in en and es | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/network-visualization | 305ce31  | feat: add networks visualization | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/introduction-video | c11dce8  | feat: add support and networks section in en and es | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/network-visualization | 3152963  | feat: add support and networks section in en and es | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | feature/network-visualization | b41bd76  | feat: update app.js route | - | 27/04/2025 |
| sergioJM05/vehix-landing-page | develop | 7582674  | feat: add network visualization section | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/introduction-video | c693755  | chore: update branch | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/introduction-video | 0a03e65  | feat: update introduction video | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | feature/introduction-video | 9daf591  | feat: update introduction video in spanish | - | 27/04/2025 |
| AntonioNavarro24/vehix-landing-page | develop | 0d31178  | feat: update introduction video in spanish | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | develop | 7339f11  | chore: delete img | - | 27/04/2025 |
| Addicted2u/vehix-landing-page | develop | b1faeb4  | chore: add img | - | 27/04/2025 |


#### 5.2.1.5. Execution Evidence for Sprint Review.


Nuestro equipo de desarrolladores logró concluir con el sprint 1, el cual involucra la implementación y despliegue de la landing page de Vehix. A continuación se mostrarán las evidencias.

link del video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202315283_upc_edu_pe/EVekU9kyDRNDgE2mhr4qbnMB56iZZ1XzpouL-3dxal5Tow?e=vvxgWJ

![banner img](/assets/imgs/chapter-V/banner_evidence.png)

![first_time_evidence img](/assets/imgs/chapter-V/first_time_evidence.png)

![choose plan img](/assets/imgs/chapter-V/plan_evidence.png)

![benefits img](/assets/imgs/chapter-V/benefits_evidence.png)

![testimonials img](/assets/imgs/chapter-V/testimonials_evidence.png)

![who are we img](/assets/imgs/chapter-V/who_are_we_evidence.png)

![questions frequently asked img](/assets/imgs/chapter-V/questions_evidence.png)

![compatibility img](/assets/imgs/chapter-V/compatibility_evidence.png)

![contact us img](/assets/imgs/chapter-V/contact_evidence.png)

![footer img](/assets/imgs/chapter-V/footer_evidence.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
#### 5.2.1.8. Team Collaboration Insights during Sprint.
