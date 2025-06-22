# Capítulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management.
Seguidamente, se mostrará un repositorio centralizado y estructurado que funcionará como referencia para un desarrollo enfocado y coherente de nuestra solución. Además se incluyen otras secciones para Source Code Management, Development Environment Configuration y Deployment Configuration.

### 5.1.1. Software Development Environment Configuration.
En esta sección, se detalla la configuración del entorno de desarrollo utilizado para construir la aplicación Vehix. Se describen las herramientas y plataformas que facilitaron la planificación del proyecto, el diseño centrado en el usuario, el desarrollo frontend y backend, las pruebas automatizadas y la documentación técnica. Estas soluciones permitieron una colaboración efectiva entre los miembros del equipo, asegurando un desarrollo ágil, organizado y alineado con los objetivos del sistema.
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
En esta sección se describe cómo se gestionaron las modificaciones al código del sistema Vehix, así como las convenciones empleadas para los commits y las versiones liberadas a lo largo del ciclo de desarrollo.

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
En esta parte del proyecto, nos centraremos en definir un conjunto uniforme de normas y convenciones de estilo y programación para el desarrollo de nuestra aplicación web Vehix. Estas pautas son fundamentales para asegurar que el código sea consistente, claro y bien estructurado, lo que a su vez facilitará su mantenimiento y escalabilidad durante todo el ciclo de vida del proyecto.

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
En esta sección se detalla y demuestra el proceso llevado a cabo para la implementación, pruebas, documentación y despliegue de la Landing Page, los Servicios Web y las Aplicaciones Web Frontend.

### 5.2.1. Sprint 1
En esta sección, documentaremos y explicaremos el desarrollo del Sprint 1 en términos de desarrollo del producto y el trabajo colaborativo del equipo. Se abordará varias secciones, incluyendo el Sprint Backlog, Development Evidence for Sprint Review, Sprint Planning.

#### 5.2.1.1. Sprint Planning 1.
En esta sección, especificáremos los principales aspectos del Sprint Planning Meeting 1.

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
			<td>11</td>
		</tr>
		<tr>
			<td><strong>Sum of Story points</strong></td>
			<td>34</td>
		</tr>
	</tbody>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators.
En esta sección se incluye la elaboración de el artefacto Leadership-andCollaboration Matrix (LACX), el cual elegirenos quién es el líder y quiénes son los colaboradores para este Sprint 1.

| Team Member (Last Name, First Name) | GitHub Username | Landing page |
| ------------------------------------|-----------------|-------------------------------------------|
| Rios Piñan, Dayro Richard|Addicted2u| C | 
| Julca Minaya, Sergio Gino|sergioJM05| C |
| Navarro Chinga, Antonio Jhair | AntonioNavarro24 | L | 
| Baca Camargo, Vitaly Arturo | Mr-Code-Star | C | 
| Elescano Leon, Piero Hugo | PieroHugo | C |


#### 5.2.1.3. Sprint Backlog 1
Nuestro principal objetivo con este primer sprint es desarrollar las funciones esenciales que permitan a los usuarios interesados en Vehix informarse sobre su propósito, conocer sus características destacadas y entender las acciones que podrán realizar dentro de su pagina web.

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
			<td rowspan="3">Búsqueda de Contenido</td>
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
			<td>Lista de beneficios</td>
			<td>T4</td>
			<td>Añadir lista de beneficios y estilo</td>
			<td>Se añade una lista de beneficios de usar la plataforma y estilos correspondientes</td>
			<td>0.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US29</td>
			<td rowspan="2">Acceso a la Aplicación desde la Página Principal</td>
			<td>T5</td>
			<td>Añadir descripción de la aplicación</td>
			<td>Se agrega un párrafo atractivo y concreto para el visitante</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T6</td>
			<td>Añadir imágenes y referencias</td>
			<td>Se agarega imagenes referenciales al aplicativo y se agrega los botones de redirección</td>
			<td>1</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US30</td>
			<td rowspan="2">Implementación de testimonios</td>
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
			<td rowspan="2">EP02-US31</td>
			<td rowspan="2">Crear planes de suscripción</td>
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
			<td rowspan="2">EP02-US36</td>
			<td rowspan="2">Soporte Multilingüe</td>
			<td>T11</td>
			<td>Creación de archivo en.html</td>
			<td>Se traduce el contenido de inglés a español en un archivo html</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T12</td>
			<td>Añadir botón de idioma</td>
			<td>Se agrega el botón de idioma para que el usuario eliga el de su preferencia</td>
			<td>0.5</td>
			<td>Antonio Navarro</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="2">EP02-US33</td>
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
			<td rowspan="2">EP02-US34</td>
			<td rowspan="2">Adaptación a diferentes dispositivos</td>
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
			<td rowspan="3">EP02-US35</td>
			<td rowspan="3">Visualización de creadores</td>
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
			<td>T20</td>
			<td>Añadir estilo al pie de pagina</td>
			<td>Se añaden estilos predefinidos al pie de pagina</td>
			<td>1</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="3">EP02-US37</td>
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
			<td rowspan="2">EP02-US38</td>
			<td rowspan="2">Desarrollo de vehiculos compatibles</td>
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
A continuación, se mostrarán los commits registrados en el repositorio correspondiente a nuestra Landing Page, para el desarrollo del sprint 1, previamente habiendo hecho el diseño en Figma. Se desarrollaron los features correspondientes, entre ellos las secciones de nuestra landing page y el cambio de idioma entre inglés y español.

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

Enlace del video: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202315283_upc_edu_pe/EVekU9kyDRNDgE2mhr4qbnMB56iZZ1XzpouL-3dxal5Tow?e=vvxgWJ

![banner img](/assets/imgs/chapter-V/banner_evidence.png)

![first_time_evidence img](/assets/imgs/chapter-V/first_time_evidence.png)

![choose plan img](/assets/imgs/chapter-V/plan_evidence.png)

![benefits img](/assets/imgs/chapter-V/benefits_evidence.png)

![testimonials img](/assets/imgs/chapter-V/testimonials.png)

![who are we img](/assets/imgs/chapter-V/who-are-we-web.png)

![questions frequently asked img](/assets/imgs/chapter-V/questions_evidence.png)

![compatibility img](/assets/imgs/chapter-V/compatibility_evidence.png)

![compatibility img_2](/assets/imgs/chapter-V/compatibility_evidence_2.png)

![contact us img](/assets/imgs/chapter-V/contact_evidence.png)

![footer img](/assets/imgs/chapter-V/footer_evidence.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
No contamos pruebas de documentacion a razón que nuestro enfoque en el primer sprint estuvo dirigido a la elaboración del landing page.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review
En esta sección presentaremos los procesos realizados durante el Sprint 1:
Para el desarrollo de este sprint, utilizamos Github Pages, una herramienta que se integró fácilmente a nuestro flujo de trabajo y nos sirvió para desplegar la Landing Page a partir de un repositorio. También desarrollamos actividades enfocadas a preparar el entorno de despliegue.

![github-pages](/assets/imgs/chapter-V/img-page.PNG)


Enlace de la Landing Page: 
https://aplicaciones-web-crew-web.github.io/vehix-landing-page/

![landing-page](/assets/imgs/chapter-V/img-lp.PNG)
#### 5.2.1.8. Team Collaboration Insights during Sprint.
En esta vista se evidencia como el equipo a trabajado de manera colaborativa para lograr la entrega del presente sprint. De esta manera, se incluyen las métricas correspondientes a la creación de la landing page, con el uso de HTML, CSS y JavaScript, y sus commits correspondientes.

![individual-commits](/assets/imgs/chapter-V/individual-commits.png)

![contributors-general-commits](/assets/imgs/chapter-V/contributors-general-commits.png)

### 5.2.2. Sprint 2
En esta sección, documentaremos y explicaremos el desarrollo del Sprint 2 en términos de desarrollo del producto y el trabajo colaborativo del equipo. Se abordará varias secciones, incluyendo el Sprint Backlog, Development Evidence for Sprint Review, Sprint Planning.

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
			<td>7</td>
		</tr>
		<tr>
			<td>Sum of Story points</td>
			<td>23</td>
		</tr>
	</tbody>
</table>

#### 5.2.2.2. Aspect Leaders and Collaborators
En esta sección se incluye la elaboración de el artefacto Leadership-andCollaboration Matrix (LACX), el cual elegirenos quién es el líder y quiénes son los colaboradores para este Sprint 2.

| Team Member (Last Name, First Name) | GitHub Username | Diagnostic view from web application | Improve Landing Page |
| ------------------------------------|-----------------|-------------------------------------------|-----------------|
| Rios Piñan, Dayro Richard|Addicted2u| C | C |
| Julca Minaya, Sergio Gino|sergioJM05| L | C |
| Navarro Chinga, Antonio Jhair | AntonioNavarro24 | C | L |
| Baca Camargo, Vitaly Arturo | Mr-Code-Star | C | C | 
| Elescano Leon, Piero Hugo | PieroHugo | C | C |

#### 5.2.2.3. Sprint Backlog 2
Nuestro objetivo principal sprint 2 es realizar la primera version de la aplicacion web y una segunda versión del Landing Page, implementando las vistas principales que contiene diferentes componentes para el análisis y las operaciones de nuestros clientes.

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
			<td rowspan="4">Previsión de problemas</td>
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
			<td rowspan="3">EP03-US07</td>
			<td rowspan="3">Diagnóstico vehicular</td>
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
			<td rowspan="3">EP05-US12</td>
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
			<td rowspan="3">EP06-US14</td>
			<td rowspan="3">Estado de suscripción</td>
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
			<td rowspan="4">EP05-US32</td>
			<td rowspan="4">Guía de conexiones</td>
			<td>T1</td>
			<td>Crear la vista sincronización</td>
			<td>Dentro de la vista de "sync" crear la ruta correspondiente</td>
			<td>0.5</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Añadir componentes de dispositivos compatibles</td>
			<td>Dentro de la vista de "sync", agregar los componentes que harán referencia a los dispositivos cercanos.</td>
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
			<td>T4</td>
			<td>Añadir componentes</td>
			<td>Se crean los componentes que falten</td>
			<td>3</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td rowspan="4">EP05-US23</td>
			<td rowspan="4">Lengüage técnico</td>
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
			<td rowspan="3">EP03-US27</td>
			<td rowspan="3">Vida útil del coche</td>
			<td>T1</td>
			<td>Crear componentes</td>
			<td>Se crea los componentes para mostrar los gráficos estadísticos</td>
			<td>3</td>
			<td>Sergio Julca</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
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
A continuación, se mostrarán los commits registrados en el repositorio correspondiente a nuestra Aplicación Web, para el desarrollo del sprint 2, el cual se ha implementado el frontend, previamente habiendo hecho el diseño en Figma. Se desarrollaron los features correspondientes.

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
Lo que se logró para este Sprint 2 es el peliegue de la primera versión de la aplicación web. En esta logramos desarrollar el toolbar, la vista de Maintenance y los componentes que se encuentran en dicha vista. Se realizó la metodología GitFlow, trabajando en ramas con el fin de ejecutar pruebas y aplicar actualizaciones sin comprometer la estabilidad de la rama principal. A continuación se mostrarán las evidencias de ejecución.
![image](https://github.com/user-attachments/assets/b7a81dab-ff07-407e-bd38-20e2a3bd2cc5)
![image](https://github.com/user-attachments/assets/5fecfc3a-ea68-43f8-a295-0a294e402227)
![image](https://github.com/user-attachments/assets/155012c3-ced9-49f7-90c9-de8c33d48a00)
![image](https://github.com/user-attachments/assets/a14e6210-a2d2-43ca-ae51-d244d1a22eed)
![image](https://github.com/user-attachments/assets/06feb40d-fe1f-45f5-a6ad-10de15ac8f66)
![image](https://github.com/user-attachments/assets/68aa52c5-aabf-42ba-bdad-9747a46d44c7)

![image](https://github.com/user-attachments/assets/900f6f49-bbc5-4e93-90f5-04a013b5d420)
![image](https://github.com/user-attachments/assets/f60f9457-280c-4262-906e-cc8cd443ae8c)

#### 5.2.2.6. Services Documentation Evidence for Sprint Review
En esta sección se incluye la relación de los endpoints documentados. A continuación se muestra el proyecto el cual evidencia el desplique de la aplicación.

Aquí tenemos el servicio de json server que ha sido usado para almacenar a la fake API que hemos creado.

![image-json](/assets/imgs/chapter-V/json_server.png)


Aquí tenemos el servicio firebase que ha sido usado para el despliegue de la aplicación web.

![image-firebase](/assets/imgs/chapter-V/firebase.png)	

#### 5.2.2.7. Software Deployment Evidence for Sprint Review
En esta sección se resume los procesos realizados en relación con Deployment durante este Sprint. A continuacíon se presenta la aplicación desplegada usando firebase.

Aquí tenemos la vista de maintenence

![image-1](/assets/imgs/chapter-V/deployment_evidence_1.png)

Aquí tenemos la vista para buscar un taller cercano

![image-1](/assets/imgs/chapter-V/deployment_evidence_2.png)


#### 5.2.2.8. Team Collaboration Insights during Sprint
En este sección se evidencia como el equipo a trabajado de manera colaborativa para lograr la entrega del presente sprint. De esta manera, se incluyen las métricas correspondientes a la creación de la app frontend.

![image-1](/assets/imgs/chapter-V/1.PNG)

![image-2](/assets/imgs/chapter-V/2.PNG)


### 5.2.3. Sprint 3
En esta sección, documentaremos y explicaremos el desarrollo del Sprint 3 en términos de desarrollo del producto y el trabajo colaborativo del equipo. Se abordará varias secciones, incluyendo el Sprint Backlog, Development Evidence for Sprint Review, Sprint Planning.

#### 5.2.3.1. Sprint Planning 3
A continuación se mostrará el cuadro correspondiente al Sprint Planning 3, donde rescatamos los aspectos más importantes del Sprint Planning Meeting.

<table>
	<tbody>
		<tr>
			<td>Sprint #</td>
			<td>Sprint 3</td>
		</tr>
		<tr>
			<td colspan="2">Spring Planing Background</td>
		</tr>
		<tr>
			<td>Date</td>
			<td>2025-05-27</td>
		</tr>
		<tr>
			<td>Time</td>
			<td>4:30 PM</td>
		</tr>
		<tr>
			<td>Location</td>
			<td>Presencial mode in classroom</td>
		</tr>
		<tr>
			<td colspan="2">Prepared by</td>
		</tr>
		<tr>
			<td>Attends (to planinning meeting)</td>
			<td>All members of CrewWeb</td>
		</tr>
		<tr>
			<td>Sprint 1 Review Summary</td>
			<td>We have achived the creation of the landing page, interactive ind intuitive, with the respectives "call to action", which allows to redirect to our web application. But we need to remove the contact section.</td>
		</tr>
		<tr>
			<td>Sprint 1 Retrospective Summary</td>
			<td>We consider that the call to action are importants in the development of the landing page to attract customers. Our product owner thinks that we need a better organization of our deliverables</td>
		</tr>
		<tr>
			<td>Sprint 2 Review Summary</td>
			<td>we have achived the web application, developing the maintenance view and using internal and external API's. We consider that we achieved the objective, deploying the web application and showing the main views. </td>
		</tr>
		<tr>
			<td>Sprint 2 Retrospective Summary</td>
			<td> We consider that we have to improve the developent environment with gitflow, and update the project report with the new developed artifacts. </td>
		</tr>
		<tr>
			<td colspan="2">Sprint Goal & User Stories</td>
		</tr>
		<tr>
			<td>Sprint 3 Goal</td>
			<td>our focus is on offering a login view,a sign up view and a library view, wich contains an different sections to read articles, watch videos and read documentation. Also allow the developer create requests (GET,POST,PUT and DELETE) of the vehicles, users, mechanics and technical history. We believe it delivers confidence and active use of the product to new customers. This will be confirmed when the customers interact actively with the new features that we will offer to them. </td>
		</tr>
		<tr>
			<td>Sprint 3 Velocity</td>
			<td></td>
		</tr>
		<tr>
			<td>Sum of Story points</td>
			<td></td>
		</tr>
	</tbody>
</table>

#### 5.2.3.2. Aspect Leaders and Collaborators
En esta sección se incluye la elaboración de el artefacto Leadership-andCollaboration Matrix (LACX), el cual elegirenos quién es el líder y quiénes son los colaboradores para este Sprint 3.

| Team Member (Last Name, First Name) | GitHub Username | IAM | MONITORING | PREFERENCES | ANALYTICS | SUBSCRIPTIONS | ARM|
| ------------------------------------|-----------------|-----|------------|-------------|-----------|---------------|----|
| Rios Piñan, Dayro Richard | Addicted2u | C | C | C | L | C | C |
| Julca Minaya, Sergio Gino | sergioJM05 | C | L | C | C | C | C |
| Navarro Chinga, Antonio Jhair | AntonioNavarro24 | C | C | C | C| L | C |
| Elescano Leon, Piero Hugo | PieroHugo | L | C | C | C | C | C |


#### 5.2.3.3. Sprint Backlog 3
Nuestro objetivo principal sprint 3 es realizar la segunda version de la aplicacion web y una tercera versión del Landing Page, implementando las vistas principales que contiene diferentes componentes para el análisis y las operaciones de nuestros clientes además de migrar a un fakeAPI a un Backend.

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
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Creación de componentes </td>
			<td>Se crean los componentes necesarios para mostrar de manera intuitiva y amigable al usuario</td>
			<td>2</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Consideración de in-app navigation</td>
			<td>Todos los componentes usado, se muestran en /car-useful-life</td>
			<td>1</td>
			<td>Piero Elescano</td>
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
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T2</td>
			<td>Implementación de componente</td>
			<td>Integrar el en la vista /profile de modo aparezca la opción de cerrar sesión</td>
			<td>0.5</td>
			<td>Piero Elescano</td>
			<td>Done</td>
		</tr>
		<tr>
			<td>T3</td>
			<td>Validación de cerrado de sesión</td>
			<td>Verificar que el singleton.user sea nulo</td>
			<td>0.5</td>
			<td>Piero Elescano</td>
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
A continuación, se mostrarán los commits registrados en el repositorio correspondiente a nuestra Backend, para el desarrollo del sprint 3. Se desarrollaron los features correspondientes.


| Repository                      | Branch                                   | Commit Id | Commit Messaage                       | Commit Message Body | Commited on |
| ------------------------------- | ---------------------------------------- | --------- | ------------------------------------- | ------------------- | ----------- |
| sergioJM05/vehix-platform | main | 37e4c34 | chore: initial commit | -                   | 2025-06-04   |
| sergioJM05/vehix-platform | release | 37e4c34 | chore: initial commit | -                   | 2025-06-04   |
| sergioJM05/vehix-platform | develop | 37e4c34 | chore: initial commit | -                   | 2025-06-04   |
| sergioJM05/vehix-platform | feature/project-configuration | f175ee1 | feat: project configuration. | -                   | 2025-06-04   |
| sergioJM05/vehix-platform | develop | df266b4 | Merge pull request #1 | -                   | 2025-06-04   |
| sergioJM05/vehix-platform | feature/software-architecture | df266b4 | Merge pull request #1 | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | feature/software-architecture | 36fb8e4 | docs: add software-architecture.dsl | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | feature/software-architecture | 36fb8e4 | docs: add software-architecture.dsl | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | develop | d570de0  | docs: add software-architecture.dsl | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | feature/software-architecture | c5b1441  | docs: fix software-architecture.dsl | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | develop | 3bd5e43 | docs: fix software-architecture.dsl | -                   | 2025-06-05   |
| PieroHugo/vehix-platform | feature/project-structure | 3bd5e43 | docs: fix software-architecture.dsl | -                   | 2025-06-10   |
| PieroHugo/vehix-platform | feature/project-structure | e6e2349   | feat(publishing): add initial entities and value objects for Vehicle | -                   | 2025-06-10   |
| PieroHugo/vehix-platform | feature/project-structure | ca9a7e0   | chore: remove .idea folder from version control | -                   | 2025-06-10   |
| PieroHugo/vehix-platform | feature/project-structure | c9477f0   | chore(api): remove duplicate file | -                   | 2025-06-10   |
| sergioJM05/vehix-platform | develop | a825d72    | feat:add project structure | -                   | 2025-06-17   |
| sergioJM05/vehix-platform | feature/analytics-value-objects | 78bc309     | feat(analytics): add analytics related value objects. | -                   | 2025-06-18   |
| sergioJM05/vehix-platform | feature/analytics-value-objects | 6e45447    | feat(analytics): delete profile id, because there is no relation with. | -           | 2025-06-18   |
| sergioJM05/vehix-platform | feature/analytics-value-objects | 8dadb0a    | feat(monitoring): add monitoring value objects.| -           | 2025-06-18   |
| Addicted2you/vehix-platform | feature/IAM | 42affe7     | feat(profile): add value object and aggregates | -           | 2025-06-18   |
| AntonioNavarro24/vehix-platform | feature/monitoring-value-objects | 23de928      | chore: update monitoring value objects. | -           | 2025-06-18   |
| Addicted2you/vehix-platform |feature/IAM | 42affe7     | Deleted branch | -           | 2025-06-18   |
| AntonioNavarro24/vehix-platform |feature/monitoring-value-objects | cffe16a      | feat(monitoring): update monitoring value objects. | -           | 2025-06-18   |
| Addicted2you/vehix-platform |feature/subscriptions-and-payments | 0eda80c       | feat(subscriptions): add value objects and entities | -           | 2025-06-18   |
| Addicted2you/vehix-platform |feature/subscriptions-and-payments | 115a078    | Merge remote-tracking branch 'origin/feature/subscriptions-and-payments' | -     | 2025-06-18   |
| sergioJM05/vehix-platform |feature/monitoring-value-objects | ac78f57     | feat(monitoring): update monitoring commands and queries. | -     | 2025-06-18   |
| AntonioNavarro24/vehix-platform |feature/monitoring-value-objects | 8f92e48      | feat(monitoring): update monitoring commands and queries. | -     | 2025-06-19   |
| Addicted2you/vehix-platform |feature/subscriptions-and-payments | 7ec2fec       | feat(subscriptions): add commands, aggregates | -     | 2025-06-19   |
| sergioJM05/vehix-platform |feature/monitoring-value-objects | b34e71c        | feat(monitoring): update value objects. | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | 667a4ae      | Merge pull request #5 | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | b3eabc0       | feature(monitoring): update monitoring repositories. | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | 4b79e0c      | Merge pull request #6 | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | f2e57fa     | feat(monitoring): add monitoring services. | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | f6a5056    | Merge pull request #7 | -     | 2025-06-20   |
| sergioJM05/vehix-platform |feature/add-cortex-dependencye | 7d055b4     | fix(project): add cortex.mediator dependencies. | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | dbbf7c1      | Merge pull request #8 | -     | 2025-06-20   |
| sergioJM05/vehix-platform |feature/monitoring-add-application-layer | bf614d8       | feat(monitoring): add monitoring event handlers. | -     | 2025-06-20   |
| sergioJM05/vehix-platform |develop | f867274        | Merge pull request #9 | -     | 2025-06-20   |
| AntonioNavarro24/vehix-platform |feature/management-value-objects | 2349b16      | Merge pull request #9 | -     | 2025-06-20   |
| AntonioNavarro24/vehix-platform |feature/assets-and-resource-management | 2349b16       | Merge pull request #9 | -     | 2025-06-21   |
| AntonioNavarro24/vehix-platform |feature/management-value-objects | 2349b16       | Deleted branch| -     | 2025-06-21   |
| AntonioNavarro24/vehix-platform |feature/management | 2349b16        | feat(management): add management resources.| -     | 2025-06-21   |
| AntonioNavarro24/vehix-platform |feature/assets-and-resource-management | 2349b16        | Deleted branch| -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/monitoring-infrastructure-layer | 3dd5ff4       | Deleted branch| -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/monitoring-infrastructure-layer | 6f5b0c3       |Merge pull request #10 | -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/monitoring-infrastructure-layer | 96910ae         |feat(monitoring): add EFC repositories. | -     | 2025-06-21   |
| sergioJM05/vehix-platform |develop | 76c958d        |Merge pull request #11 | -     | 2025-06-21   |
| sergioJM05/vehix-platform |develop | f83678b         |feature(monitoring): add monitoring interface resources. | -     | 2025-06-21   |
| sergioJM05/vehix-platform |develop | fe3095d          |Merge pull request #12 | -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/add-monitoring-interface-transformation | fe3095d           |Merge pull request #12 | -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/add-monitoring-interface-transformation | 51296db          |feature(monitoring): add monitoring transform interfaces. | -     | 2025-06-21   |
| sergioJM05/vehix-platform |develop | 9a0a783           |Merge pull request #13 | -     | 2025-06-21   |
| sergioJM05/vehix-platform |feature/add-monitoring-controllers | 009d442            |feat(monitoring): add monitoring controllers.| -     | 2025-06-21   |
| sergioJM05/vehix-platform |develop | 8bf7f4a           |Merge pull request #14 | -     | 2025-06-21   |
| sergioJM05/vehix-platform | feature/update-program-cs | 774dad1 | feat(monitoring): update program cs. | – | 2025-06-21 |
| sergioJM05/vehix-platform | develop | 8bf7f4a | Merge pull request #15 | – | 2025-06-21 |
| PieroHugo/vehix-platform | feature/IAM | e09d0c2 | Merge pull request #17 | – | 2025-06-21 |
| PieroHugo/vehix-platform | develop | 937d743 | Merge pull request #17 | – | 2025-06-21 |
| PieroHugo/vehix-platform| feature/IAM | e09d0c2 | feat: implement IAM | – | 2025-06-21 |
| PieroHugo/vehix-platform | feature/IAM | feba0a5 | chore: remove IDE-specific .idea files from repository | – | 2025-06-21 |
| sergioJM05/vehix-platform | fix/connection-to-mysql | e27d509 | feature(monitoring): latest program update cs. | – | 2025-06-21 |
| sergioJM05/vehix-platform | develop | e09d0c2 | Merge pull request #18 | – | yesterday |
|sergioJM05/vehix-platform | fix/monitoring-add-error-type | 2cecf59 | fix(monitoring): update validation of error type. | – | 2025-06-21 |
| sergioJM05/vehix-platform | develop | 22006d0 | Merge pull request #19 | – | 2025-06-21 |
| AntotnioNavarro24/vehix-platform | feature/management | 2349b16 | feat(management): add management resources. | – | 2025-06-21 |
| Addicted2you/vehix-platform | feature/subscriptions-and-payments | 7ec2fec | feat(subscriptions): moved files and add functions | – | 2025-06-22 |
| PieroHugo/vehix-platform | feature/Identity | 9540b49 | Merge pull request #19 | – | 2025-06-22 |
| PieroHugo/vehix-platform | feature/Identity | c660421 | feat: Implemnet Indentity | – | 2025-06-22 |
| PieroHugo/vehix-platform | feature/Identity | 0058934 | feat: Implement Identity | – | 2025-06-22 |
|PieroHugo/vehix-platform | feature/Identity | b438aec | feat: update database | – | 2025-06-22 |
| PieroHugo/vehix-platform | feature/Identity | 0b4ee4c | fix: docker file | – | 2025-06-22 |
| PieroHugo/vehix-platform | feature/Identity | 0022185 | feat: update Program.cs | – |  2025-06-22 |

#### 5.2.3.5. Execution evidence for Sprint Review
Lo que se logró para este Sprint 3 es el peliegue de la segunda versión de la aplicación web. Además, implementamos la primera versión del backend, donde hemos realizado acerca de los usuarios, vehículos e historial de reparaciones. Se realizó la metodología GitFlow, trabajando en ramas con el fin de ejecutar pruebas y aplicar actualizaciones sin comprometer la estabilidad de la rama principal.

#### 5.2.3.6. Services Documentation Evidence for Sprint Review
En esta sección se incluye la relación de los endpoints documentados.
![Image](https://github.com/user-attachments/assets/5ab4c058-c31d-469b-bd83-5fc395cffd4f)

![Image](https://github.com/user-attachments/assets/747ff5f5-9655-4b37-a80f-8e31eee42200)
#### 5.2.3.7. Software Deployment Evidence for Sprint Review
En esta sección se resume los procesos realizados en relación con Deployment durante este Sprint.
El despligue del backend se realizo en Render
![Image](https://github.com/user-attachments/assets/c7375d67-aa4a-4b5a-80a9-5500be17dfdc)
![Image](https://github.com/user-attachments/assets/363719b0-071a-4df4-9d6e-8dd04b4420bd)
![Image](https://github.com/user-attachments/assets/5ab4c058-c31d-469b-bd83-5fc395cffd4f)
![Image](https://github.com/user-attachments/assets/c5ec308e-51ef-4644-9f6f-563deaafb2d7)

#### 5.2.3.8. Team Collaboration Insights during Sprint
En este sección se evidencia como el equipo a trabajado de manera colaborativa para lograr la entrega del presente sprint. De esta manera, se incluyen las métricas correspondientes a la creación del Backend.

## 5.3. Validation Interviews
En esta sección del informe se documentan y detallan las acciones relacionadas con las entrevistas de validación llevadas a cabo durante el desarrollo del proyecto. Estas entrevistas tienen como propósito fundamental recoger opiniones, identificar las expectativas y necesidades de los usuarios, y confirmar o descartar las suposiciones planteadas sobre el producto. Para ello, se facilitará la interacción de los participantes, pertenecientes a ambos segmentos definidos, con la landing page y la aplicación web, permitiendo así una evaluación directa de la experiencia.

### 5.3.1. Design Interviews
En esta sección se establece por cada segmento objetivo los elementos a incluir en la sesión de validación, incluyendo el Landing Page y las aplicaciones. Además se especifica cuáles serán los user flows de las aplicaciones, que formarán parte del proceso de validación.

Segmento 1: Propietarios de vehículos urbanos (uso personal)

Objetivo de la validación:
Comprobar si los usuarios entienden el valor de la plataforma para el mantenimiento preventivo y registro de su vehículo.

Elementos a incluir:

- Claridad del mensaje principal en la landing page

- Llamado a la acción (CTA)

- Opiniones sobre testimonios y beneficios listados.

- Visualización e interacción con el mapa digital

- Visualización de mecánicos

- Paneles de errores

Flujos a validar:

User Flow 1: Registro a la plataforma

User Flow 2: Inicio de sesión en la plataforma

User Flow 4: Registro de vehículo

User Flow 6: Descripción sencilla del problema detectado en el vehículo

User Flow 7: Talleres mecánicos cercanos a la ubicación

Segmento 2: Conductores independientes (Uber, InDriver, taxi, delivery)

Objetivo de la validación:
Validar si la plataforma les ayuda a optimizar el tiempo de mantenimiento y reducir fallas inesperadas que afectan sus ingresos.

Elementos a incluir:

- Mensaje de valor centrado en eficiencia y reducción de tiempo de inactividad.

- Testimonios de otros conductores.

- Registro de vehículos

- Visualización de problemas del vehículo

- Escaneo del vehículo

- Paneles de errores

Flujos a validar:

User Flow 1: Registro a la plataforma

User Flow 2: Inicio de sesión en la plataforma

User Flow 4: Registro de vehículo

User Flow 6: descripción sencilla del problema detectado en el vehículo

User Flow 7: Talleres mecánicos cercanos a la ubicación

User Flow 11: Escaneo básico del vehículo

Segmento 3: Mecánicos o técnicos automotrices

Objetivo de la validación:
Determinar si la aplicación puede mejorar la comunicación con sus clientes y ayudar en la gestión de diagnósticos.

Elementos a incluir:

- Enfoque en la gestión profesional de talleres o servicios técnicos.

- Beneficios como digitalización de diagnósticos, historial del vehículo, contacto con clientes.

- CTA dirigido: “Optimiza tu taller con Vehix”.

- Visualización de los vehículos registrados

- Visualización de la bibliteca automotriz y su contenido

- Visualización de datos del vehículo

- Paneles de errores

Flujos a validar:

User Flow 1: Registro a la plataforma

User Flow 2: Inicio de sesión en la plataforma

User Flow 3: Sincronización con el vehículo

User Flow 4: Registro de vehículo

User Flow 8: Acceso a biblioteca automotriz

User Flow 13: Visualizar el estado técnico del vehículo con datos detallados


### 5.3.2. Interview Record
En esta sección presentaremos el registro de cada entrevista de validación que hemos realizado para cada segmento objetivo de nuestro proyecto.

Segmento 1: Propietarios de vehículos urbanos (uso personal)

Entrevista 1:

![lucas val](/assets/imgs/chapter-V/lucas_val.png)

[00:00 - 9:55]

Duración: 9 minutos 55 segundos

Link de la entrevista: [entrevista 1](https://upcedupe-my.sharepoint.com/personal/u202315283_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202315283_upc_edu_pe%2FDocuments%2Fupc-pre-202510-1asi0730-4368-crewweb-sprint-3%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Efd7ee727-c7d4-4485-b5e6-022c7078e397&isDarkMode=false)

Nombre: Lucas 

Apellidos: Sanchez Heredia

Edad: 25 años

Distrito: Chorrillos

Resumen: Durante la sesión de validación con Lucas, un usuario representativo del segmento de propietarios de vehículos urbanos, se evaluaron tanto la landing page como la aplicación web de Vehix. Lucas interactuó activamente con la landing page, mostrando interés y comprensión del mensaje principal. La propuesta de valor fue clara y atractiva, y el llamado a la acción (CTA) fue identificado con facilidad. Los testimonios y beneficios listados fueron percibidos como útiles y confiables. Además, pudo visualizar correctamente el mapa digital y la lista de mecánicos cercanos, encontrándolos funcionales y relevantes. Los paneles de errores también fueron valorados positivamente, ya que aportan información útil para el diagnóstico.

En cuanto a la aplicación web, Lucas completó con éxito todos los flujos de usuario asignados. El registro (User Flow 1) y el inicio de sesión (User Flow 2) fueron intuitivos y sin dificultades. El registro del vehículo (User Flow 4) se realizó de forma clara, y la descripción del problema (User Flow 6) permitió expresar fácilmente el fallo percibido. Finalmente, la funcionalidad que muestra talleres mecánicos cercanos (User Flow 7) fue destacada como una característica especialmente útil.

Entrevista 2:

![cesar val](/assets/imgs/chapter-V/cesar_val.png)

[9:55 - 20:39]

Duración: 10 minutos 44 segundos

Link de la entrevista: [entrevista 2](https://upcedupe-my.sharepoint.com/personal/u202315283_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202315283_upc_edu_pe%2FDocuments%2Fupc-pre-202510-1asi0730-4368-crewweb-sprint-3%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Efd7ee727-c7d4-4485-b5e6-022c7078e397&isDarkMode=false)

Nombre: Cesar 

Apellidos: Bonifacio

Edad: 25 años

Distrito: Chorrillos

Resumen: Durante la sesión de validación con César, también perteneciente al segmento de propietarios de vehículos urbanos de uso personal, se observaron reacciones positivas frente a la propuesta de Vehix. César exploró con atención la landing page, mostrando comprensión del mensaje principal y del propósito general de la plataforma. El llamado a la acción (CTA) fue claro para él, y consideró útiles los beneficios destacados y los testimonios de otros usuarios. Además, interactuó sin inconvenientes con el mapa digital y la visualización de mecánicos cercanos, funciones que consideró prácticas para casos de emergencia o mantenimiento regular. Los paneles de errores también llamaron su atención, reconociendo su utilidad para entender mejor el estado del vehículo.

En lo referente a la aplicación web, César completó correctamente todos los flujos de usuario evaluados. El registro en la plataforma (User Flow 1) y el inicio de sesión (User Flow 2) fueron realizados sin complicaciones, mostrando fluidez en la interfaz. El registro de su vehículo (User Flow 4) le resultó sencillo, y destacó lo intuitivo del proceso. También logró describir el problema de su vehículo (User Flow 6) de manera clara gracias al diseño de la interfaz. Finalmente, valoró positivamente la opción de visualizar talleres mecánicos cercanos (User Flow 7), resaltando que es una función que usaría con frecuencia.

Entrevista 3: 

![ariana val](/assets/imgs/chapter-V/ariana_val.png)

[20:39 - 28:45]

Duración: 8 minutos 6 segundos

Link de la entrevista: [entrevista 3](https://upcedupe-my.sharepoint.com/personal/u202315283_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202315283_upc_edu_pe%2FDocuments%2Fupc-pre-202510-1asi0730-4368-crewweb-sprint-3%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Efd7ee727-c7d4-4485-b5e6-022c7078e397&isDarkMode=false)

Nombre: Ariana 

Apellidos: Yassan Laredo

Edad: 25 años

Distrito: San Juan de Miraflores

Resumen: Durante la prueba con Ariana, una usuaria representativa del segmento de propietarios de vehículos de uso personal, se evaluó su interacción con la landing page y la aplicación web de Vehix. Ariana navegó con interés por la página principal, comprendiendo de manera clara la propuesta de valor que ofrece la plataforma. Le pareció evidente el propósito del servicio, y el llamado a la acción fue fácil de identificar. Además, consideró que los testimonios y beneficios presentados aportaban credibilidad. Al explorar el mapa digital y la función para ver mecánicos cercanos, destacó lo útil que sería contar con esa información en tiempo real. También reaccionó positivamente ante los paneles de errores, ya que le permiten tener un mayor control sobre el estado de su vehículo.

Respecto a la web application, Ariana completó sin dificultad los flujos propuestos. El proceso de registro (User Flow 1) le resultó rápido, y el inicio de sesión (User Flow 2) fue simple. El registro de su vehículo (User Flow 4) se sintió natural dentro de la navegación, y no presentó dudas al hacerlo. Al momento de describir un problema del vehículo (User Flow 6), encontró que la plataforma le brindaba opciones claras para expresarse. Finalmente, la opción de ver talleres cercanos (User Flow 7) fue una de las que más valoró, ya que le pareció práctica y necesaria para cualquier conductor.

Entrevista 7: 

![richard val](/assets/imgs/chapter-V/richard_val.png)

[28:45 - 42:18]

Duración: 13 minutos 33 segundos

Link de la entrevista: [entrevista 7](https://upcedupe-my.sharepoint.com/personal/u202315283_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202315283_upc_edu_pe%2FDocuments%2Fupc-pre-202510-1asi0730-4368-crewweb-sprint-3%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Efd7ee727-c7d4-4485-b5e6-022c7078e397&isDarkMode=false)

Nombre: Richard 

Apellidos: Rios Sandoval

Edad: 54 años

Distrito: Villa el Salvador

Resumen: Durante la validación con Richard, mecánico automotriz, se evaluaron la landing page y la aplicación web de Vehix desde el enfoque profesional del Segmento 3. Richard comprendió rápidamente la propuesta de valor, destacando el mensaje principal y apreciando beneficios como la digitalización de diagnósticos, el historial del vehículo y el contacto con clientes. También valoró positivamente la visualización de vehículos registrados, la biblioteca automotriz y los paneles de errores, considerándolos herramientas útiles para su trabajo diario.

Al ingresar a la aplicación web, Richard completó satisfactoriamente los flujos asignados. El registro (User Flow 1) y el inicio de sesión (User Flow 2) fueron simples e intuitivos. Pudo realizar la sincronización con el vehículo (User Flow 3) sin complicaciones, lo cual consideró un punto clave para agilizar diagnósticos. El registro de vehículos (User Flow 4) también fue directo, y destacó la importancia de esta función para mantener un control ordenado de sus clientes. Además, navegó por la biblioteca automotriz (User Flow 8), encontrando información técnica relevante y bien organizada, lo que consideró un gran apoyo para su trabajo. Finalmente, al visualizar el estado técnico del vehículo con datos detallados (User Flow 13), valoró especialmente los paneles de errores y la presentación clara de los datos, mencionando que esta información le permitiría comunicarse mejor con sus clientes y respaldar sus diagnósticos con evidencia concreta.


### 5.3.3. Evaluation based on heuristics
Esta sección contiene el proceso de evaluación de las sesiones de validación basado en heurísticas, considerando heurísticas de usabilidad, arquitectura de información e inclusive design de la experiencia propuesta.
### UX Heuristics & Principles Evaluation
#### Usability – Inclusive Design – Information Architecture
---
CARRERA: Ingeniería de Software
CURSO : Aplicaciones Web
SECCIÓN : 4368
PROFESORES : Todos
AUDITOR : CrewWeb
CLIENTE(S) : 
---
**SITE o APP A EVALUAR:**
VEHIX

**TAREAS A EVALUAR:**
El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:
1. Inicio de Sesión
2. Registro de usuario Nuevo
3. Conexión con nuevo vehículo
4. Visualizacion de librerías automotrices
5. Pago de una subscripcion
6. Ayuda de talleres mecánicos
7. Visualización de fallas del vehículo
8. Lectura del vehículo con el scanner
No están incluidas en esta versión de la evaluación las siguientes tareas:
1. Reparación de fallas
2. Actualizacion de estado de fallas
3. Actualizacion de datos
4. Visualizacion de preguntas frecuentes
5. Visualización de analíticas

**ESCALA DE SEVERIDAD:**
Los errores serán puntuados tomando en cuenta la siguiente escala de severidad
|Nivel|Descripción|
|-----|-----------|
|1|Problema superficial: puede ser fácilmente superador por el usuario ó ocurre con muy poco frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.|
|2|Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente reléase|
|3|Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les debe asignar una prioridad alta.|
|4|Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.|

**TABLA RESUMEN:**
|#|Problema|Escala de severidad|Heurística/Principio violado(a)|
|--|-------|-------------------|-------------------------------|
|1|Se dificulta la navegación y el uso de la aplicación desde teléfonos celulares.|4|Usabilidad - Flexibilidad y eficiencia de uso|
|2|El sistema no siempre confirma claramente el éxito de una acción importante.|3|Usabilidad - Visibilidad del estado del sistema|
|3|El sistema no siempre confirma claramente el éxito de una acción importante.|2|Usabilidad - Visibilidad del estado del sistema|
|4|La sección de analíticas no responde al hacer clic, sin avisar su estado.|3|Usabilidad - Visibilidad del estado del sistema; Usabilidad - Control y libertad del usuario|
|5|No hay un botón de retroceso fácil en las secciones de la librería.|2|Usabilidad - Control y libertad del usuario; Usabilidad - Consistencia y estándares|


**DESCRIPCIÓN DE RPOBLEMAS:**
PROBLEMA #1: Se dificulta la navegación y el uso de la aplicación desde teléfonos celulares.

Severidad: 4

Heurística violada: Usabilidad - Flexibilidad y eficiencia de uso

Problema: Al intentar utilizar la aplicación desde un teléfono celular, el usuario experimenta una gran dificultad para navegar y ver el contenido de forma adecuada. Los elementos de la pantalla (textos, botones, imágenes) aparecen demasiado grandes o pequeños, desorganizados o incluso cortados, obligando al usuario a hacer zoom constantemente o a desplazarse horizontalmente. Esto hace que usar la aplicación en dispositivos móviles sea casi imposible y muy frustrante.

Recomendación: Es crucial que la aplicación se adapte y se vea correctamente en diferentes tamaños de pantalla, especialmente en teléfonos celulares. Se recomienda implementar un diseño que ajuste automáticamente la disposición de los elementos para facilitar la visualización y la interacción en dispositivos móviles.

---

PROBLEMA #2: El sistema no siempre confirma claramente el éxito de una acción importante.

Severidad: 3

Heurística violada: Usabilidad - Visibilidad del estado del sistema
Problema: Al registrar un nuevo vehículo o guardar cambios importantes, el usuario no recibe una confirmación visual clara e inmediata de que la operación fue exitosa. Aunque la aplicación puede mostrar algo en la consola, la falta de un mensaje en pantalla (como un "¡Vehículo guardado con éxito!") genera incertidumbre, haciendo que el usuario se pregunte si la acción se completó realmente.

Recomendación: Implementar mensajes de confirmación claros y visibles en la pantalla después de esta acción en específico

---
PROBLEMA #3: La guiá de conectar el escáner no es suficientemente clara.

Severidad: 2

Heurística violada: Usabilidad - Visibilidad del estado del sistema

Problema: Tras seguir los pasos para conectar el escáner, la aplicación simplemente indica "Done, let the app do the work.". No hay una confirmación explícita de si la conexión fue exitosa o si hay algún problema. El usuario queda a la expectativa sin saber si el escáner está realmente listo para la lectura o si necesita hacer algo más.

Recomendación: Proporcionar un mensaje claro de "Conexión exitosa" o "Error de conexión" después de intentar conectar el escáner.

---
PROBLEMA #4: La sección de analíticas no responde al hacer clic, sin avisar su estado.

Severidad: 3

Heurística violada: Usabilidad - Visibilidad del estado del sistema; Usabilidad - Control y libertad del usuario

Problema: El usuario intentar acceder a la sección de "Analíticas" haciendo clic en ella, pero no ocurre nada en la pantalla. La aplicación no muestra ningún mensaje que indique que la función no está disponible, que está en desarrollo o que hay un error. Esto frustra al usuario al no obtener la respuesta esperada y no saber por qué la acción no se completa.

Recomendación: Para elementos no funcionales o en desarrollo se debe indicar que la función no está disponible, o que está "Próximamente" si se espera implementarla.

---
PROBLEMA #5: No hay un botón de retroceso fácil en las secciones de la librería.

Severidad: 2

Heurística violada: Usabilidad - Control y libertad del usuario; Usabilidad - Consistencia y estándares

Problema: Cuando el usuario navega a una subsección dentro de las "Librerías automotrices", no hay un botón de "Atrás" o "Volver a Librería" claramente visible y fácil de usar dentro de la interfaz. Esto fuerza al usuario a depender del menu o navegador, lo que consume más pasos y esfuerzo.

Recomendación: Incluir un botón de "Atrás" en las subsecciones de la librería que permita al usuario regresar fácilmente a la página principal de librerías o a la sección anterior.

## 5.4. Video About the Product
En esta sección se describe el contenido del Video About-theProduct, el cual tiene como público objetivo los visitantes al Landing Page, quienes desean conocer sobre el modelo de negocio y las características principales de los productos de software, al igual que los usuarios de las Aplicaciones, quienes desean realizar tareas relacionadas con los procesos soportados por la solución.
