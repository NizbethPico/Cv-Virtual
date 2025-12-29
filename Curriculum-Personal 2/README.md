# CV Virtual — Plantilla Web Personalizada (HTML + CSS + JS)

Plantilla de **CV/Portafolio** en una sola página, con **menú vertical anclado**, **secciones dinámicas**, **animaciones fluidas**, **portfolio filtrable**, **modal AJAX**, **formulario de contacto por pasos** y **mapa interactivo**.

> Proyecto ideal para aprender maquetación web y publicar tu CV online de forma profesional.

![Preview - Portafolio de Nizbeth](assets/img/photos/image-copy.png)

---

## Demo

Cuando publiques tu proyecto:
- **GitHub Pages:** `https://TU_USUARIO.github.io/Curriculum-Personal/`
- **Vercel:** `https://curriculum-personal.vercel.app/`
- **Netlify:** `https://tu-dominio.netlify.app/`

---

## Tecnologías Utilizadas

- **HTML5** — Estructura semántica
- **CSS3** — Estilos responsivos con grid y flexbox
- **JavaScript** — Interactividad y lógica
- **jQuery 1.12.4** — Manipulación del DOM
- **Plugins JS** — Masonry layout, animaciones al scroll
- **Google Maps API** — Mapa interactivo
- **Iconos:** 
  - Themify Icons (pe-icon-7-stroke)
  - Font Awesome

---

## Estructura del Proyecto

```
Curriculum-Personal/
│
├── Curriculum-Personal.html          # Archivo principal
├── assets/CV_NIZBETH.pdf             # PDF descargable
├── README.md                          # Este archivo
│
├── assets/
│   ├── css/
│   │   └── styles.css                 # Estilos principales
│   │
│   ├── js/
│   │   ├── jquery-1.12.4.min.js       # Librería jQuery
│   │   ├── plugins.js                 # Plugins (masonry, animaciones, etc.)
│   │   └── core.js                    # Lógica principal (interactividad)
│   │
│   ├── img/
│   │   ├── favicon.png                # Favicon
│   │   ├── favicon_60x60.png
│   │   ├── favicon_76x76.png
│   │   ├── favicon_120x120.png
│   │   ├── favicon_152x152.png
│   │   ├── photos/                    # Fotos de perfil y sección start
│   │   ├── works/                     # Imágenes del portfolio
│   │   ├── posts/                     # Imágenes de blog/artículos
│   │   └── avatars/                   # Avatares de testimonios/clientes
│   │
│   └── fonts/                         # Fuentes personalizadas (si aplica)
```

---

## Cómo Ejecutarlo en Local

Este es un proyecto **100% estático** (sin backend), así que tienes varias opciones:

### Opción A — Abrir Directamente
1. Haz doble clic en `Curriculum-Personal.html`
2. Se abre en tu navegador

> **Nota:** Algunas funciones avanzadas (modal AJAX, descargas) funcionan mejor con servidor local.

### Opción B — Servidor Local (Recomendado)

#### Con Live Server en VS Code:
1. Abre el proyecto en VS Code
2. Instala la extensión **Live Server** (autor: Ritwick Dey)
3. Click derecho en `Curriculum-Personal.html` → **Open with Live Server**
4. Se abre automáticamente en `http://localhost:5500`

#### Con Python (Terminal):
```bash
# Python 3.x
python -m http.server 8000

# O con Python 2.x
python -m SimpleHTTPServer 8000
```
Luego abre `http://localhost:8000` en el navegador.

---

## Descripción de Archivos Clave

### `Curriculum-Personal.html`
**Contenido principal:**
- Loader inicial (`#page-loader`) — animación de carga
- Header vertical colapsable (`#header`) — navegación fija
- Secciones ancladas:
  - `#start` — Presentación inicial
  - `#resume` — Currículum (especialidades, habilidades, idiomas, educación)
  - `#portfolio` — Trabajos/proyectos con filtros
  - `#clients` — Testimonios/clientes
  - `#latest-posts` — Blog
  - `#contact` — Formulario de contacto
- Modal AJAX (`#ajax-modal`) — carga contenido dinámico
- Popup de contacto (`#contact-popup`) — formulario por pasos

### `assets/css/styles.css`
**Contiene:**
- Reset de estilos y estilos globales
- Sistema de grid (`container`, `row`, `col-*`)
- Componentes:
  - Header y navegación
  - Botones (primario, secundario)
  - Cards/tarjetas
  - Barras de progreso (habilidades)
  - Timeline (educación/empleo)
  - Portfolio/galería
  - Modal y popup
  - Animaciones (fade-in, slide, etc.)

### `assets/js/jquery-1.12.4.min.js`
Librería jQuery minificada para:
- Seleccionar y manipular elementos DOM
- Eventos (click, scroll, etc.)
- Animaciones y transiciones
- AJAX (cargar contenido dinámico)

### `assets/js/plugins.js`
Paquete de utilidades externas:
- **Masonry** — Layout tipo Pinterest (rejilla responsiva)
- **Owl Carousel** — Carruseles/sliders
- **Smooth Scroll** — Desplazamiento suave
- **Lazy Load** — Carga perezosa de imágenes
- **Tooltips y Popovers** — Información emergente

### `assets/js/core.js`
**"El cerebro" de la plantilla:**
- Inicializa componentes al cargar
- Controla animaciones (`data-animation`, delays)
- Gestiona el menú vertical y colapso
- Detección de scroll para activar efectos
- Controla filtros del portfolio
- Modal AJAX dinamizado
- Formulario de contacto por pasos
- Descarga de CV (función `downloadCV()`)
- Lee datos del mapa de Google

---

## Personalización Paso a Paso

### 1️⃣ Información Personal

Edita `Curriculum-Personal.html`, sección `#start`:

```html
<h1 class="text-lg mb-0"><em>¡Hola! Soy</em> Nizbeth Delgado</h1>
<p class="lead text-muted">Diseñadora UX/UI | Desarrolladora | Soporte Técnico</p>
```

Cambia:
- **Nombre:** `Nizbeth Delgado` ← tu nombre
- **Descripción:** `Diseñadora UX/UI...` ← tu profesión

### 2️⃣ Foto de Perfil

En la sección `#start`:

```html
<div class="bg-image zooming">
  <img src="assets/img/photos/coach_bg01.jpg" alt="">
</div>
```

Reemplaza `coach_bg01.jpg` con tu imagen en `assets/img/photos/`

**Pasos:**
1. Guarda tu foto en `assets/img/photos/`
2. Cambia el nombre del archivo en `src="assets/img/photos/TU_FOTO.jpg"`

### 3️⃣ Habilidades y Barras de Progreso

En la sección `#resume`, busca las barras de progreso:

```html
<div class="skill">
  <div class="progress">
    <div class="progress-bar" role="progressbar" aria-valuenow="85"></div>
  </div>
  <h5>Adobe Photoshop / Sketch</h5>
</div>
```

- **`aria-valuenow="85"`** → El porcentaje (0-100)
- **`<h5>Adobe...</h5>`** → El nombre de la habilidad

Cambia ambos valores según tus habilidades reales.

### 4️⃣ Educación y Experiencia Laboral

En la sección timeline de `#resume`:

```html
<div class="timeline-event animated">
  <div class="content">
    <span class="date">Sep 2023 - Sep 2025</span>
    <h4>Vendedora - El Corte Inglés</h4>
    <span class="caption">Escaparatismo, Gestión de cartera</span>
  </div>
</div>
```

Duplica este bloque para agregar más empleos/educación. Cambia:
- **`<span class="date">`** → Fechas
- **`<h4>`** → Título del puesto/certificación
- **`<span class="caption">`** → Empresa/institución y tareas

### 5️⃣ Portfolio / Proyectos

En la sección `#portfolio`, busca los items:

```html
<div class="mobileApps masonry-item col-md-4 col-sm-6 col-xs-12">
  <div class="image-box">
    <div class="image">
      <a href="project-example.html" data-toggle="ajax-modal">
        <img src="assets/img/works/work01.jpg" alt="">
      </a>
    </div>
  </div>
</div>
```

**Para cambiar categoría:**
- Reemplaza `mobileApps` por: `webdesign`, `socialMedia`, etc.
- Debe coincidir con el filtro arriba:
  ```html
  <li><a href="#" data-filter=".mobileApps">Aplicaciones Móviles</a></li>
  ```

**Para cambiar imagen:**
1. Guarda tu imagen en `assets/img/works/`
2. Cambia el `src=""` en el HTML

### 6️⃣ Información de Contacto

En la sección `#contact`, busca el formulario y actualiza:

```html
<input name="email" id="email" type="email" class="form-control"
       placeholder="Tu email..." required>
```

Y en `core.js`, busca la función `downloadCV()` para cambiar la ruta del PDF si es necesario.

### 7️⃣ Mapa

En `core.js`, busca la función que inicializa el mapa:

```javascript
var $googleMap = $('#google-map');
if($googleMap.length) {
  var latitude = parseFloat($googleMap.attr('data-latitude'));
  var longitude = parseFloat($googleMap.attr('data-longitude'));
  // ...
}
```

Y en el HTML:

```html
<div id="google-map"
     data-latitude="37.3891"
     data-longitude="-5.9845"
     data-style="dream"></div>
```

Cambia `data-latitude` y `data-longitude` con tus coordenadas.

**⚠️ Nota:** Google Maps ahora requiere **API Key**. Revisa "Solución de Problemas" más abajo.

### 8️⃣ Colores y Estilos

En `assets/css/styles.css`, busca las variables de color (generalmente al inicio):

```css
:root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  --dark-bg: #1a1a1a;
}
```

O busca el color principal en el archivo y cámbialo. Por ejemplo:

```css
.btn-primary {
  background-color: #007bff; /* ← Cambia este valor */
}
```

---

## Descargar CV (Función Implementada)

La plantilla incluye un botón **"Descargar CV"** que descarga tu archivo PDF.

**Archivo:** `assets/CV_NIZBETH.pdf`

**Para cambiar:**
1. Reemplaza `CV_NIZBETH.pdf` con tu PDF en la carpeta `assets/`
2. En `assets/js/core.js`, busca la función:

```javascript
function downloadCV() {
    var link = document.createElement('a');
    link.href = 'assets/CV_NIZBETH.pdf';  // ← Cambio aquí
    link.download = 'CV_NIZBETH.pdf';
    // ...
}
```

3. Cambia ambas rutas por el nombre de tu PDF.

---

## Publicación en GitHub

### 1. Crear Repositorio

1. Ve a [github.com](https://github.com) e inicia sesión
2. **New Repository**
3. Nombre: `Curriculum-Personal`
4. Descripción: "Mi CV online — Portafolio profesional"
5. **Create Repository**

### 2. Subir Archivos

**Opción A — GitHub Desktop:**
1. Instala GitHub Desktop
2. Clone tu repositorio
3. Copia todos los archivos en la carpeta local
4. Commit y Push

**Opción B — Terminal (Git):**

```bash
cd /Users/nizbethpico/Documents/Curriculum-Personal

git init
git add .
git commit -m "Initial commit: CV online personalizado"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/Curriculum-Personal.git
git push -u origin main
```

### 3. Activar GitHub Pages

1. Ve a **Settings** → **Pages**
2. **Source:** Selecciona `main` branch, carpeta `/root`
3. Guarda
4. Espera 1-2 minutos
5. Tu sitio estará en: `https://TU_USUARIO.github.io/Curriculum-Personal/`

---

## Publicación en Vercel (Recomendado)

**Ventajas:** Más rápido, mejor rendimiento, dominio gratuito personalizado.

### 1. Conectar GitHub

1. Ve a [vercel.com](https://vercel.com)
2. **Sign up** con tu cuenta GitHub
3. **Authorize Vercel**

### 2. Crear Proyecto

1. **Add New Project**
2. **Import Git Repository**
3. Selecciona `Curriculum-Personal`
4. Vercel detecta automáticamente que es un proyecto estático
5. Click en **Deploy**

### 3. Dominio Personalizado (opcional)

1. En tu proyecto en Vercel → **Settings** → **Domains**
2. Agrega un dominio personalizado (por ejemplo: `nizbethdelgado.com`)
3. Sigue las instrucciones para apuntar el DNS

---

## Solución de Problemas

### ❌ No aparecen iconos (cuadrados vacíos)

**Causa:** Falta la carpeta `assets/fonts/` o el CSS no las referencia.

**Solución:**
1. Verifica que `assets/fonts/` exista
2. En `styles.css`, busca `@font-face` y asegúrate de que las rutas sean correctas:

```css
@font-face {
  font-family: 'themify';
  src: url('../fonts/themify.woff') format('woff'),
       url('../fonts/themify.woff2') format('woff2');
}
```

3. Las rutas deben ser **relativas** (con `../`)

### ❌ El botón "Descargar CV" no funciona

**Causa:** La ruta del PDF es incorrecta o el archivo no existe.

**Solución:**
1. Verifica que `assets/CV_NIZBETH.pdf` exista
2. En `core.js`, línea de `downloadCV()`, revisa la ruta:

```javascript
link.href = 'assets/CV_NIZBETH.pdf';
```

3. Si has renombrado el archivo, cambia aquí también

### ❌ El modal AJAX no carga contenido

**Causa:** Abrir directamente (`file://`) sin servidor local rompe AJAX.

**Solución:**
- Usa **Live Server** o publica en Vercel/GitHub Pages
- AJAX no funciona con protocolo `file://`

### ❌ Google Maps no aparece

**Causa:** API Key faltante o deshabilitada.

**Solución:**
1. Ve a [Google Cloud Console](https://console.cloud.google.com)
2. Crea un proyecto nuevo
3. Habilita **Maps JavaScript API**
4. Crea una **API Key**
5. En `Curriculum-Personal.html`, busca el script de Maps:

```html
<script src="https://maps.googleapis.com/maps/api/js?key=TU_API_KEY"></script>
```

6. Reemplaza `TU_API_KEY` con tu clave

### ❌ Error "$ is not defined"

**Causa:** jQuery no cargó antes que los scripts que lo usan.

**Solución:** Verifica el orden en `Curriculum-Personal.html`:

```html
<!-- Debe ser en este orden: -->
<script src="assets/js/jquery-1.12.4.min.js"></script>
<script src="assets/js/plugins.js"></script>
<script src="assets/js/core.js"></script>
```

---

## Tareas Pendientes (Checklist)

- [ ] Personalizar nombre y descripción
- [ ] Cambiar foto de perfil
- [ ] Actualizar habilidades y barras de progreso
- [ ] Agregar experiencia laboral real
- [ ] Agregar educación y certificaciones
- [ ] Cargar proyectos en portfolio
- [ ] Actualizar información de contacto
- [ ] Configurar Google Maps (API Key)
- [ ] Probar en Live Server
- [ ] Subir a GitHub
- [ ] Activar GitHub Pages o Vercel
- [ ] Compartir enlace en CV tradicional y redes sociales

---

## Créditos y Licencia

- **Plantilla base:** Tema de CV/Portafolio responsive
- **Librerías:** jQuery, Masonry, Google Maps API
- **Iconos:** Themify Icons, Font Awesome
- **Fuentes:** Google Fonts
- **Personalización:** Nizbeth Delgado

---

## Contacto y Soporte

- 📧 **Email:** nizbethdelgado@gmail.com
- 🔗 **Portfolio:** https://TU_SITIO.com (cuando esté publicado)
- 💼 **LinkedIn:** [Tu perfil LinkedIn]

---

**Última actualización:** 29 de diciembre de 2025
