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

Para asegurar la consistencia y calidad en el desarrollo de nuestra Landing Page implementaremos una serie de convenciones específicas para los distintos lenguajes y tecnologías que utilizamos:

#### HTML

-  Siempre iniciar los documentos HTML con `<!DOCTYPE html>` y configurar `<meta charset="UTF-8">`.

-  Nombres de etiquetas y atributos siempre en minúsculas (`<div>`, `<section>`, `<button>`, etc.).

-  Siempre se deben usar **comillas dobles**  `(")` para los valores de los atributos.
Ejemplo: `<input type="text" name="email" />`

``` 
input type="text" name="email" />
```

-  Se incluirán los atributos `alt`, `width` y `height` en las imágenes para mejorar la accesibilidad y el diseño responsivo.

-  Utilizar comentarios `<!-- -->` para marcar secciones importantes del código.

-  Definir la codificación de caracteres como UTF-8 para soportar la mayoría de los caracteres de   todos los idiomas, `<meta charset="UTF-8">`

-  Inclusión de la hoja de estilos CSS, la hoja de estilo principal debe ser enlazada dentro de la sección `<head>`. Usando siempre la etiqueta `<link>` de la siguiente manera:

``` 
<link rel="stylesheet" href="styles.css">                                 
``` 
   
-  Inclusión de archivos JavaScript, los archivos JavaScript deben incluirse **antes del cierre de la etiqueta `</body>`** para mejorar el tiempo de carga de la página.

``` 
<script src="script.js"></script>
</body>
</html>
``` 


#### CSS

- Todos los nombres de clases e IDs deben estar en inglés y escritos usando el formato **kebab-case**, es decir, en minúsculas y separando palabras con guiones (`-`), por ejemplo: `.hero-text`, `.plan-card-pro`, `.faq-title`.

-  cada declaración debe terminar con un punto y coma `;`.
    Ejemplo correcto:
    
 ```
.title-who {
  font-size: 34px;
  font-weight: bold;
  padding: 2%;
}	
```

-  Las llaves `{}` deben colocarse en la misma línea que el selector.

```
.benefit-card {
  background: black;
  color: white;
}
```

- Implementar **media queries** (`@media`) para adaptar el diseño a diferentes dispositivos.

```
@media (max-width: 768px) {
  .hero-text {
    text-align: center;
  }
}
```


#### JavaScript

-  Usar `const` para valores que no cambian y `let` para los que sí.

```
const wrapper = document.getElementById("main-wrapper");
let currentSlide = 0;
```

- Evitar el uso de `var` por completo (obsoleto).

- Las llaves `{}` deben abrirse en la misma línea que la declaración.

```
function toggleMenu() {
  // lógica aquí
}
```

- Punto y coma obligatorio al final de cada instrucción.

```
document.addEventListener("DOMContentLoaded", updateSlider);
```

- cada función debe hacer una sola cosa.

```
document.addEventListener("DOMContentLoaded", updateSlider);
```

- Usar **event delegation y listeners** con funciones nombradas cuando sea posible.

```
document.querySelectorAll('.faq-question').forEach(button => {
  button.addEventListener('click', () => {
    // ...
  });
});
```

### 5.1.4. Software Deployment Configuration.

En esta sección, se tratará de explicar el procedimiento de despliegue de nuestros proyectos como LandingPage, Backend y FrontEnd.

##### LandingPage

Para el despliegue de nuestra landing page se escogio Git Page siendo una alternativa facil de usar y de configurar.

 - **Paso 1:** Para desplegar el LandingPage hay que dirigirse al repositorio del landingPage y luego entrar a la opción de settings.

![paso_1](/assets/imgs/chapter-V/paso-1.PNG)

 - **Paso 2**: Ahora entraremos a la opción de Pages donde seleccionaremos la rama del proyecto que queremos desplegar

![paso_2](/assets/imgs/chapter-V/paso-2.png)

- **Paso 3:** Es asi como debe quedarla selección de la rama 

![paso_3](/assets/imgs/chapter-V/paso-3.png)

- **Paso 4:** Luego de esperar unos minutos la pagina del LandingPage se desplegara y aparecerá la opción de acceder a esta misma

![paso_4](/assets/imgs/chapter-V/paso-4.PNG)

## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
En esta sección se documenta el desarrollo correspondiente al Sprint 1 del proyecto Vehix. Se presentan los objetivos priorizados, las tareas asignadas al equipo, los entregables alcanzados y un resumen del progreso logrado. Este sprint marca el inicio del ciclo de trabajo iterativo, centrado en construir los cimientos del sistema y validar los supuestos iniciales.
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

![who are we img](/assets/imgs/chapter-V/who-are-we-web.png)

![questions frequently asked img](/assets/imgs/chapter-V/questions_evidence.png)

![compatibility img](/assets/imgs/chapter-V/compatibility_evidence.png)

![compatibility img_2](/assets/imgs/chapter-V/compatibility_evidence_2.png)

![contact us img](/assets/imgs/chapter-V/contact_evidence.png)

![footer img](/assets/imgs/chapter-V/footer_evidence.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
No contamos pruebas de documentacion a razón que nuestro enfoque en el primer sprint estuvo dirigido a la elaboración del landing page.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Para el desarrollo de este sprint, utilizamos Github Pages, una herramienta que se integró fácilmente a nuestro flujo de trabajo y nos sirvió para desplegar la Landing Page a partir de un repositorio. También desarrollamos actividades enfocadas a preparar el entorno de despliegue.

![github-pages](/assets/imgs/chapter-V/img-page.PNG)


Enlace de la Landing Page: 
https://aplicaciones-web-crew-web.github.io/vehix-landing-page/

![landing-page](/assets/imgs/chapter-V/img-lp.PNG)
#### 5.2.1.8. Team Collaboration Insights during Sprint.

En este apartado se evidencia como el equipo a trabajado de manera colaborativa para lograr la entrega del presente sprint. De esta manera, se incluyen las métricas correspondientes a la creación de la landing page, con el uso de HTML, CSS y JavaScript, y sus commits correspondientes.

![individual-commits](/assets/imgs/chapter-V/individual-commits.png)

![contributors-general-commits](/assets/imgs/chapter-V/contributors-general-commits.png)

### 5.2.2. Sprint 2
#### 5.2.2.1. Sprint Planning 2

A continuación se mostrará el cuadro correspondiente al Sprint Planning 2, donde rescatamos los aspectos más importantes del Sprint Planning Meeting.

<table>
	<tbody>
		<tr>
			<td>Sprint #</td>
			<td>Sprint 2</td>
		</tr>
		<tr>
			<td colspan="2">Spring Planing Background</td>
		</tr>
		<tr>
			<td>Date</td>
			<td>2025-05-22</td>
		</tr>
		<tr>
			<td>Time</td>
			<td>4:50 PM</td>
		</tr>
		<tr>
			<td>Location</td>
			<td>Remote mode through the GitHub platform</td>
		</tr>
		<tr>
			<td colspan="2">Prepared by</td>
		</tr>
		<tr>
			<td>Attends (to planinning meeting)</td>
			<td>All members of crewtech</td>
		</tr>
		<tr>
			<td>Sprint 1 Review Summary</td>
			<td>We have completed sprint 1 successfully, we have finished the landing page for Vehix. The answer from our team was great, even though at the beginning it was a bit hard.</td>
		</tr>
		<tr>
			<td>Sprint 1 Retrospective Summary</td>
			<td> Our team did a great job, but there are different aspects to be improved. We should have been organanized from the beginning to avoid some complications late, also we had keep a good communication through the development of the project to avoid misunderstandings between the members of the team. </td>
		</tr>
		<tr>
			<td colspan="2">Sprint Goal & User Stories</td>
		</tr>
		<tr>
			<td>Spritn 2 Goal</td>
			<td>Our focus is on the implementation of the main view from the web application, which contains different views for the analytics and operations for our customers. We believe it delivers an big approach from what we expoect of the project. This will be confirmed when the team are able to try the new features without any mistake. </td>
		</tr>
		<tr>
			<td>Sprint 2 Velocity</td>
			<td>16</td>
		</tr>
		<tr>
			<td>Sum of Story points</td>
			<td>42</td>
		</tr>
	</tbody>
</table>

#### 5.2.2.2. Aspect Leaders and Collaborators

A continuación mostramos los líderes y colaboradoeres de los aspectos a realizarse.

| Team Member (Last Name, First Name) | GitHub Username | Diagnostic view from web application | Improve Landing Page |
| ------------------------------------|-----------------|-------------------------------------------|-----------------|
| Rios Piñan, Dayro Richard|Addicted2u| C | C |
| Julca Minaya, Sergio Gino|sergioJM05| L | C |
| Navarro Chinga, Antonio Jhair | AntonioNavarro24 | C | L |
| Baca Camargo, Vitaly Arturo | Mr-Code-Star | C | C | 
| Elescano Leon, Piero Hugo | PieroHugo | C | C |

#### 5.2.2.3. Sprint Backlog 2

A continuación, se ve el sprint backlog 2, donde se han descompuesto los user stories y se verán las tareas designadas a cada integrante del equipo.

<table>
	<tbody>
		<tr>
			<td><strong>Sprint #</strong></td>
			<td colspan="7">Sprint 2</td>
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
			<td rowspan="4">EP03-US06</td>
			<td rowspan="4">Historial de desgaste vehicular</td>
			<td>T1</td>
			<td>Añadir imágenes</td>
			<td>Se añaden imágenes para tener una mejor referencia</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Añadir componentes</td>
			<td>Se añañen componentes como gráficos estadísticos y cards</td>
			<td>3</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que la vista sea responsive</td>
			<td>1.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Añadir descripción</td>
			<td>Se añade una descripción general del reporte en un párrafo</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US08</td>
			<td rowspan="3">Diagnóstico vehicular PRO</td>
			<td>T1</td>
			<td>Crear la vista diagnóstico</td>
			<td>Se crea la vista correspondiente a diagnóstico rápido</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Vinculación de la vista maintenance a la vista diagnóstico rápido</td>
			<td>Dentro de la vista maintenance habrá un componente que redirigirá a la vista diagnóstico rápido para una navegación óptima</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que sea responsive</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US13</td>
			<td rowspan="3">Localizar un taller automotriz cercano</td>
			<td>T1</td>
			<td>Crear la estructura de la vista para encontrar un taller automotriz cercano</td>
			<td>Se crea la estructura de la vista</td>
			<td>1.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Añadir mapa interactivo</td>
			<td>Dentro de la vista se deberá consumir una API para mostrar un mapa con el que se pueda interactuar</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que la vista sea responsive</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US14</td>
			<td rowspan="3">Ver descripción resumida de la falla del vehículo</td>
			<td>T1</td>
			<td>Mostrar resumen de la falla</td>
			<td>Se muestra una breve descripción de la falla del vehículo en un párrafo</td>
			<td>1.5</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Añadir gráfico</td>
			<td>Se añaden gráficos estadísticos</td>
			<td>2</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que la vista sea responsive</td>
			<td>2</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP05-US18</td>
			<td rowspan="4">Diagnostico Standard</td>
			<td>T1</td>
			<td>Crear la vista diagnóstico</td>
			<td>Se crea la vista correspondiente a diagnóstico rápido</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Vinculación de la vista maintenance a la vista diagnóstico</td>
			<td>Dentro de la vista maintenance habrá un componente que redirigirá a la vista diagnóstico rápido para una navegación óptima</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que sea responsive</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir componentes</td>
			<td>Se crean los componentes respectivos</td>
			<td>3</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP05-US25</td>
			<td rowspan="4">Datos técnicos</td>
			<td>T1</td>
			<td>Crear componentes</td>
			<td>Se crea los componentes para mostrar los datos técnicos</td>
			<td>3</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que sea responsive</td>
			<td>1.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir descripciones</td>
			<td>Se añaden descripciones de los datos estadísticos</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Añadir imágenes</td>
			<td>Se añaden imágenes para tener una mejor referencia</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US29</td>
			<td rowspan="3">Estadística intuitiva</td>
			<td>T1</td>
			<td>Crear componentes</td>
			<td>Se crea los componentes para mostrar los gráficos estadísticos</td>
			<td>3</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir estilos y propiedades responsive</td>
			<td>Se añade los estilos CSS y se añaden las propiedades para que sea responsive</td>
			<td>2</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir descripciones</td>
			<td>Se añaden descripciones concisas de los datos estadísticos</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
	</tbody>
</table>

#### 5.2.2.4. Development Evidence for Sprint Review

Para el desarrollo del sprint 2, se ha implementado el frontend, previamente habiendo hecho el diseño en Figma. Se desarrollaron los features correspondientes.

| Repository                      | Branch                                   | Commit Id | Commit Messaage                       | Commit Message Body | Commited on |
| ------------------------------- | ---------------------------------------- | --------- | ------------------------------------- | ------------------- | ----------- |
| sergioJM05/vehix-landing-page | feature/project-structure | 57bd15f   | chore: initial commit | -                   | 2025-04-25   |
| sergioJM05/vehix-landing-page | develop                   | 57bd15f   | chore: initial commit | -                   | 2025-04-25   |
| sergioJM05/vehix-landing-page | main                      | 57bd15f   | chore: initial commit | -                   | 2025-04-25   |
| sergioJM05/vehix-landing-page | master                    | 57bd15f   | chore: initial commit | -                   | 2025-04-25   |
| sergioJM05/vehix-landing-page | realese                   | 57bd15f   | chore: initial commit | -                   | 2025-04-25   |
| sergioJM05/vehix-landing-page | develop      	            | 57bd15f   | chore: initial commit      | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | 57bd15f   | chore: initial commit      | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | e3fc9b4   | feat: add db.json          | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | 27bf9f3   | Update routes.json         | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | 89ff840   | feat: add json server      | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | a744bfb   | feat: add .env.production  | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-server        | 357b818   | feat: add .env.development | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | develop                   | 53621f2   | feat: add .env.development | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | 53621f2   | feat: add server          | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | dd9446c   | feat: add i18n            | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | 8725b2c   | feat: add en.json         | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | 9d893e2   | feat: add es.json         | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | 9236d7b   | feat: add style.css main  | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | c6d4cf6   | feat: add main.js         | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feat/add-english-spanish                   | 4c4b27a   | feat: add app.vue         | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | develop                                    | 5374f12   | feat: add english-spanish | Pull request merge  | 25/04/2025  |
| sergioJM05/vehix-landing-page | develop                                    | -         | feat: add router          | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page | feature/add-assets-and-resource-management | 5374f12   | feat: add english-spanish | Pull request merge  | 25/04/2025  |
| sergioJM05/vehix-landing-page       | feature/add-monitoring                     | 5374f12   | feat: add english-spanish             | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page       | feature/add-public-components              | 5374f12   | feat: add english-spanish             | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page       | feature/add-public-pages                   | 5374f12   | feat: add english-spanish             | -                   | 25/04/2025  |
| sergioJM05/vehix-landing-page       | feature/add-shared                         | 5374f12   | feat: add english-spanish             | -                   | 25/04/2025  |
| Mr-Code-star/vehix-landing-page     | feature/add-public-components              | f725119   | feat: add english-spanish             | -                   | 25/04/2025  |
| PieroHugo/vehix-landing-page        | feature/add-public-pages                   | 11af925   | feat: add language-switcher.component | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 5ea9360   | feat add home.component.vue           | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | f2882c8   | feat: add audit failure list          | -                   | 25/04/2025  |
| PieroHugo/vehix-landing-page        | feature/add-public-pages                   | 7322aba   | feat: add bad practices               | -                   | 25/04/2025  |
| Mr-Code-star/vehix-landing-page     | develop                                    | 025f134   | feat: add library.component.vue       | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | de17004   | feat: add language-switcher.component | Pull request merge  | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 5ea9360   | feat: add car presentation          | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 0ef73d0   | feat: add maintenance.component.vue | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | de17004   | feat: add failure item              | -                   | 25/04/2025  |
| PieroHugo/vehix-landing-page        | feature/add-public-pages                   | 4595d78   | feat: add mechanic card list        | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | a911660   | feat: add profile.component.vue     | -                   | 25/04/2025  |
| PieroHugo/vehix-landing-page        | feature/add-public-pages                   | 09f757d   | feat: add system status item        | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 04d386a   | feat: add sync.component.vue        | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 843846a   | feat: update mechanic card list     | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 0eaf44f   | feat: add system status list        | -                   | 25/04/2025  |
| PieroHugo/vehix-landing-page        | develop                                    | 46746a7   | feat: add mechanic card component   | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 1549ee3   | feat: add public pages              | Pull request merge  | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 9be70c1   | feat: add simple isssues service | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 4132c67   | feat: add bad practices service  | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 3a9b112   | feat: add tap scan page          | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 2d31cca   | feat: add Status                 | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 8b8120e   | feat: add mechanic               | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 752898a   | feat: add Failure                | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | fe8dc52   | feat: add Audit page             | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 8e2d3b3   | feat: technical errors entity    | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 8c3990d   | feat: add System status          | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 6301c39   | feat: add simple issues entity   | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 28180ae   | feat: add bad practices entity   | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 365de22   | feat: add Failure                | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 6a0a32d   | feat: add technical errors       | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | 2660792   | feat: add simple issues          | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | feature/add-monitoring                     | bf21e87   | feat: add mechanic map component | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | feature/add-assets-and-resource-management | 1cb6afb   | feat: add monitoring domain              | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | develop                                    | 171b1b9   | chore: add image                         | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | develop                                    | 49979f7   | chore: add image                         | -                   | 25/04/2025  |
| Addicted2you/vehix-landing-page     | develop                                    | 24d5374   | feat: add assets and resource management | -                   | 25/04/2025  |
| AntonioNavarro24/vehix-landing-page | develop                                    | 46746a7   | feat: add technical error service        | -                   | 25/04/2025  |


#### 5.2.2.5. Execution Evidence for Sprint Review

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

A continuación se mostrará la documentación de los servicios usados.

Aquí tenemos el servicio de json server que ha sido usado para almacenar a la fake API que hemos creado.

![image-json](/assets/imgs/chapter-V/json_server.png)


Aquí tenemos el servicio firebase que ha sido usado para el despliegue de la aplicación web.

![image-firebase](/assets/imgs/chapter-V/firebase.png)	

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

A continuación se mostrarán las evidencias del despliegue de la aplicación web. Se desplegó la aplicación usando firebase

Aquí tenemos la vista de maintenence

![image-1](/assets/imgs/chapter-V/deployment_evidence_1.png)

Aquí tenemos la vista para buscar un taller cercano

![image-1](/assets/imgs/chapter-V/deployment_evidence_2.png)


#### 5.2.2.8. Team Collaboration Insights during Sprint
En este apartado se evidencia como el equipo a trabajado de manera colaborativa para lograr la entrega del presente sprint. De esta manera, se incluyen las métricas correspondientes a la creación de la app frontend.

![image-1](/assets/imgs/chapter-V/1.PNG)

![image-2](/assets/imgs/chapter-V/2.PNG)


### 5.2.3. Sprint 3
#### 5.2.3.1. Sprint Planning 3
#### 5.2.3.2. Aspect Leaders and Collaborators
#### 5.2.3.3. Sprint Backlog 3

<table>
	<tbody>
		<tr>
			<td><strong>Sprint #</strong></td>
			<td colspan="7">Sprint 3</td>
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
			<td rowspan="4">EP03-US10</td>
			<td rowspan="4">Historial de vehículos</td>
			<td>T1</td>
			<td>Añadir datos complmentarios de vehículo en el db.json</td>
			<td>Se añaden los datos pertinentes y la conexión entre objetos json</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creación del servicio vehiculo</td>
			<td>Se añade y consume el servicio de vehículo</td>
			<td>3</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Añadir componente para mostrar vehículo e i18n</td>
			<td>Se añade el/los componente(s) mostrando los datos de la fake API. Asimismo se considera las 3 tecnologías fundamentales y el i18n</td>
			<td>1.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Validaciones de negocio</td>
			<td>Se añade validaciones para la cantidad de  vehículos, tipo de usuario y manejo de errores</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP05-US24</td>
			<td rowspan="4">Biblioteca automotriz</td>
			<td>T1</td>
			<td>Añadir datos complementarios de vehículo en el db.json si se necesit a</td>
			<td>se añaden los datos pertinentes y la conexión entre objetos json</td>
			<td>0.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creación de componentes y consumo de servicios</td>
			<td>Situarse en la vista "library", mostrar los componentes que lo incluyen como "articles" y "news" consumiendo los servicios correspondientes</td>
			<td>1</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación con lógica de negocio</td>
			<td>Validar el estado de plan y tipo de plan que tiene el usuario</td>
			<td>1</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Redirecciones e in-app navigation</td>
			<td>Se añade los botones e hupervínculos a los sitios estáticos correspondientes a cada sección de la biblioteca y considerandose las rutas predefinidas</td>
			<td>1</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP03-US12</td>
			<td rowspan="4">Ingresar nuevo vehículo</td>
			<td>T1</td>
			<td>Rehuso de servicio</td>
			<td>Reusar el servicio del vehículo y agregar funcion con solicitud http tipo "POST" correspondiente</td>
			<td>1.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Componente de formulario e i18n</td>
			<td>Crear el componente considerando el modelo, kilometrage actual, año del carro, fecha de revisión ténica y nombre referencial de este</td>
			<td>2</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación de lógica de negocio</td>
			<td>Se añade la lógica de validacion en el componentes correspondiente para no repetir los vehiculo y no permitir agregar más de un vehículo en caso sea un cliente del plan standard</td>
			<td>2</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Añadir in-app navigation</td>
			<td>Se añade la ruta de la página donde se ingresarán todos los componentes considerados</td>
			<td>2</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP03-US16</td>
			<td rowspan="4">Registrar mantenimiento realizado</td>
			<td>T1</td>
			<td>Crear componentes con respecto a fallas</td>
			<td>Se crea componentes para registrar el mantimiento considerando el comentario de solucion</td>
			<td>1.5</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Consumo de servicio de fallas y solución</td>
			<td>Se crean las entidades de fallas y solucion, y se crea sus respectivo servicios</td>
			<td>2</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validaciones de lógica de negocio sobre la solución</td>
			<td>Se valida que el usuario tenga el plan pro, de lo contrario se considera "Upselling Content" </td>
			<td>2</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>In app navigation para registro de manenimiento</td>
			<td>Se crea el enrutamiento correspondiente, considerando un nombre alusivo a la acción, cómo "maintenance register"</td>
			<td>2</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP01-US30</td>
			<td rowspan="4">Eliminación de vehículo</td>
			<td>T1</td>
			<td>Rehusar el servicio de vehículos y añadir solicitud http tipo DELETE</td>
			<td>Se rehusa el servicio y se aumenta la funcionalidad "DELETE"</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creacion de componentes para la eliminacion de vehículo</td>
			<td>Se añade el "delete icon" y se coloca por cada vehiculo</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Funcionalidad y validación de negocio</td>
			<td>Se añade la funcionalidad poara eliminar y se valida si el usuario esta completamente seguro de realizar esa acción</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Verificar in-app navigation</td>
			<td>Se verifica el estado de la ruta y se añade el lazy loading correspondiente</td>
			<td>2</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP07-US21</td>
			<td rowspan="4">Vehículos registrados</td>
			<td>T1</td>
			<td>Definir la Entidad/Modelo de Vehículo en el Backend</td>
			<td>Crear la estructura de datos que representará un vehículo en el backend.</td>
			<td>3</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementar la Capa de Acceso a Datos para Vehículos</td>
			<td>Crear la lógica en el backend que permita interactuar directamente con la base de datos para la entidad Vehículo. Esto incluye una operación para "crear" un nuevo vehículo en la tabla Vehicles.</td>
			<td>1.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Desarrollar el Endpoint POST para el Registro de Vehículos</td>
			<td> Implementar la lógica del controlador/API en el backend que escuchará las solicitudes HTTP POST. Este endpoint recibirá los datos del vehículo desde el frontend, los validará, utilizará la capa de acceso a datos para guardarlos en la base de datos y enviará una respuesta HTTP adecuada.</td>
			<td>1</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Integrar el Frontend con el Nuevo Endpoint POST.</td>
			<td>Modificar el servicio de vehículos para que, en lugar de usar la Fake API, envíe los datos del vehículo al nuevo endpoint POST del backend real. Esto incluye manejar la suscripción a la respuesta del backend.</td>
			<td>0.5</td>
			<td>Vitaly Baca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US29</td>
			<td rowspan="3">Estado del vehículo</td>
			<td>T1</td>
			<td>Consumir el servicio de vehiculo</td>
			<td>Se cosnsume el servicio correspondiente y se agrega si es necesario atributos o nuevos datos para en la estructura de los objetos json correspondientes.</td>
			<td>2</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creación de componentes </td>
			<td>Se crean los componentes necesarios para mostrar de manera intuitiva y amigable al usuario</td>
			<td>2</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Consideración de in-app navigation</td>
			<td>Todos los componentes usado, se muestran en /car-useful-life</td>
			<td>1</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP03-US26</td>
			<td rowspan="3">Recordatorios de Revisiones técnicas</td>
			<td>T1</td>
			<td>Creación de entidad</td>
			<td>Se añade la entidad de notificaciones</td>
			<td>2</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Validaciones y consumo de servicios</td>
			<td>Se añade las solicitudes http tipo GET y POST para la validación de creación de una nueva fecha para la revision ténica</td>
			<td>2</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Visualización en desplegable</td>
			<td>Se usa el componente a considerar y en el desplegable se muestran las notificaciones</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP01-US23</td>
			<td rowspan="3">Edición de información personal</td>
			<td>T1</td>
			<td>Actualización del servicio de "user"</td>
			<td>Se añade en el servicio una petición http tipo "PUT", para actualizar los nueva información que ingrese el usuario</td>
			<td>2</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creación de un componente card</td>
			<td>Se añade dentro del componentes los inputs correspondientes y considerando i18n</td>
			<td>2</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación de datos</td>
			<td>Se valida con la lógica de negocio que considera solo números para el dni. </td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP03-US27</td>
			<td rowspan="4">Registro de datos de vehículo</td>
			<td>T1</td>
			<td>Rehuso de servicio</td>
			<td>Reusar el servicio del vehículo y agregar funcion con solicitud http tipo "POST" correspondiente</td>
			<td>1.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Componente de formulario e i18n</td>
			<td>Crear el componente considerando el modelo, kilometrage actual, año del carro, fecha de revisión ténica y nombre referencial de este</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación de lógica de negocio</td>
			<td>Se añade la lógica de validacion en el componentes correspondiente para no repetir los vehiculo y no permitir agregar más de un vehículo en caso sea un cliente del plan standard</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Añadir in-app navigation</td>
			<td>Se añade la ruta de la página donde se ingresarán todos los componentes considerados</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP07-US20</td>
			<td rowspan="4">Mecánico cercanos</td>
			<td>T1</td>
			<td>Definir la Entidad/Modelo de Mecánico en el Backend</td>
			<td>Definir la estructura de datos que se espera recibir de la API de Google Maps para un mecánico</td>
			<td>3</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementar la Lógica de Llamada a la API de Google Maps en el Backend</td>
			<td>Crear la lógica en el backend para realizar una solicitud HTTP (GET) a la API de Google Maps utilizando las credenciales y parámetros adecuados</td>
			<td>1.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Desarrollar el Endpoint GET para la lectura de Mecánicos</td>
			<td>Implementar el endpoint de la API REST en el backend que el frontend llamará. Este endpoint recibirá la ubicación del conductor, llamará a GoogleMapsService, procesará la respuesta de Google Maps y devolverá los mecánicos relevantes al frontend</td>
			<td>1</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Integrar el Frontend con el Nuevo Endpoint GET.</td>
			<td>Modificar el servicio para que, en lugar de una Fake API, envíe la solicitud GET al nuevo endpoint del backend. De esta manera, el frontend enviará la ubicación del conductor y manejará la respuesta de los mecánicos</td>
			<td>0.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP07-US19</td>
			<td rowspan="4">Historial técnico de vehiculo</td>
			<td>T1</td>
			<td>Definir la Entidad/Modelo de Historial ténico en el Backend</td>
			<td>Crear la estructura de datos que representará un registro dentro del historial técnico de un vehículo. Esto implica decidir qué atributos tendrá cada evento</td>
			<td>3</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementar la Capa de Acceso a Datos para el Historial Técnico.</td>
			<td>Crear la lógica en el backend que permita interactuar directamente con la base de datos para la entidad Historial Técnico. Esto incluye una operación para "leer" los registros del historial técnico, específicamente buscando por el id de un vehículo.</td>
			<td>1.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Desarrollar el Endpoint GET para el Historial Técnico de un Vehículo</td>
			<td> Implementar la lógica del controlador/API en el backend que escuchará las solicitudes HTTP GET para obtener el historial. Este endpoint recibirá el identificador del vehículo, utilizará la capa de acceso a datos para recuperar los registros del historial de la base de datos y enviará una respuesta HTTP adecuada.</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td> Integrar el Frontend con el Nuevo Endpoint GET del Historial Técnico</td>
			<td>Modificar el servicio de vehículos para que envíe una solicitud GET al nuevo endpoint del backend, pasando el id del vehículo.</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP06-US15</td>
			<td rowspan="2">Estado de suscripción</td>
			<td>T1</td>
			<td>Consumir servicio de suscripción</td>
			<td>Consumir el servicio de suscripcion y de usuario de modo que se consiga el estado de suscripcion y fehca del usuario</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementación de componente</td>
			<td>Integrar el componentes en la vista /profile de modo que aparezca los datos recuperados</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP01-US09</td>
			<td rowspan="3">Guardado de datos y cierre de sesión</td>
			<td>T1</td>
			<td>Consumir servicio user.singleton</td>
			<td>Se consume el servicio del singleton para cerrar sesión y redirigirlo a la vista de registro</td>
			<td>0.5</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementación de componente</td>
			<td>Integrar el en la vista /profile de modo aparezca la opción de cerrar sesión</td>
			<td>0.5</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación de cerrado de sesión</td>
			<td>Verificar que el singleton.user sea nulo</td>
			<td>0.5</td>
			<td>Moises Espinoza</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP07-TS41</td>
			<td rowspan="4">Actualizar datos de un vehículo</td>
			<td>T1</td>
			<td>Actualizar la Entidad de Vehículo en el Backend</td>
			<td>Revisar la entidad Vehículo existente para asegurar que contiene todos los campos necesarios que un usuario podría querer actualizar. Si es necesario, añadir atributos</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementar la Operación de Actualización (Update) en la Capa de Acceso a Datos para Vehículos.</td>
			<td>Añadir o modificar la lógica en el componente para Vehículo que permita actualizar un registro existente en la base de datos. De manera que la operación toma el ID del vehículo a actualizar y los nuevos datos, y los cree en la tabla Vehicles.</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Desarrollar el Endpoint PUT para la Actualización de Vehículos</td>
			<td>Implementar la lógica del controlador/API en el backend que escuchará las solicitudes HTTP PUT. Este endpoint recibirá el ID del vehículo a actualizar y los datos editados, validará la información, utilizará la capa de acceso a datos para aplicar la actualización y enviará una respuesta HTTP adecuada.</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T4</td>
			<td>Implementar la Interfaz de Usuario y la Integración Frontend para la Edición de Vehículo</td>
			<td> Modificar los componentes correspondientes para que los usuarios puedan editar los datos de un vehículo existente. De manera que, tambien se debe cargar los datos actuales del vehículo, permitir la edición en un formulario y luego enviar los datos editados al nuevo endpoint PUT del backend.</td>
			<td>1</td>
			<td>Dayro Rios</td>
			<td>Done</td>
		</tr>
	</tbody>
</table>

#### 5.2.3.4. Development Evidence for Sprint Review
#### 5.2.3.5. Execution evidence for Sprint Review
#### 5.2.3.6. Services Documentation Evidence for Sprint Review
#### 5.2.3.7. Software Deployment Evidence for Sprint Review
#### 5.2.3.8. Team Collaboration Insights during Sprint

## 5.3. Validation Interviews
### 5.3.1. Design Interviews
### 5.3.2. Interview Record
### 5.3.3. Evaluation based on heuristics
## 5.4. Video About the Product


