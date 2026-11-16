# B1. Galería de tu setup
 
> Todos los ejercicios van en la carpeta `boletin_html2/`, con las imágenes en `boletin_html2/imagenes/`.
>
> Muestra **tres veces la misma imagen**: a tamaño original; a 200 × 150 px con el atributo **style**; y a 200 × 150 con los atributos **width y height**. Todas con alt. Después rompe a propósito el nombre de una en el `src` y observa qué se muestra. **Pregunta (en un comentario):** ¿por qué se recomienda `style` frente a `width` y `height`?

Nota: **los .jpg que coloque en la respuesta del ejercicio, serían a cómo lo tendría yo en una carpeta para usarla con VisualStudioCode** 

### Código: 

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B1. Galería de tu setup</title>
</head>
<body>
  <h1>Galería de mi setup</h1>
  <h2>Tamaño original</h2>
  <img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos">
  <h2>200 × 150 con el atributo style</h2>
  <img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos" style="width:200px; height:150px;">
  <h2>200 × 150 con los atributos width y height</h2>
  <img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos" width="200" height="150">
  <h2>Imagen rota a propósito</h2>
  <img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos">
  <!--
    Pregunta: ¿por qué se recomienda style frente a width y height?
    Respuesta: con style el tamaño pasa a ser CSS, como el resto del aspecto de la página.
    Así no lo puede cambiar sin querer una hoja de estilos y todo el diseño está en el mismo sitio.
  -->
</body>
</html>
```
### Qué se ve con la imagen rota

El `src` apunta a `setp.jpg` que no existe, en lugar de la foto el navegador muestra el **icono de imagen rota** junto al texto del `alt`. Por eso el `alt` debe describir la imagen.

### Recordatorios:

- `<img>` no se cierra. Lleva `src` (ruta de la imagen) y `alt` (texto alternativo).
- Con `style` se pone la unidad: `width:200px;`. Con los atributos, solo el número: `width="200"`

# B2. Perfil de una red social

> Un `<h1>` con el nombre del creador; una foto de perfil con **borde de 5 px verde continuo** y `float: right`; tres párrafos de biografía que rodeen la imagen; una segunda imagen con `float: left` y borde punteado azul; y una tercera con `float: none` y sin borde. **Pregunta:** ¿qué diferencia visual hay entre `left`, `right` y `none`?


### Código: 

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B2. Perfil de una red social</title>
</head>
<body>
  <h1>Lucía Pixel</h1>
  <img src="imagenes/perfil.jpg" alt="Foto de perfil de Lucía Pixel" style="width:180px; border:5px solid green; float:right;">
  <p>Lucía Pixel es creadora de contenido sobre tecnología desde 2019. Empezó grabando vídeos cortos sobre cómo montar un ordenador por piezas y hoy tiene una comunidad de miles de seguidores que la acompañan cada semana en sus directos.</p>
  <p>En su canal explica de forma sencilla cómo elegir componentes, cómo cuidar la seguridad de las cuentas y cómo sacar partido a programas gratuitos. Sus vídeos favoritos son los de comparativas, en los que pone a prueba dos productos durante una semana.</p>
  <p>Cuando no está grabando, estudia un ciclo de informática y participa en torneos de videojuegos.</p>
  <img src="imagenes/setup.jpg" alt="El escritorio de Lucía" style="width:160px; border:3px dotted blue; float:left;">
  <p>Este es el escritorio desde el que graba todos sus vídeos: dos pantallas, un micrófono de condensador y un teclado mecánico con interruptores silenciosos para que no se oiga en los directos. Además, ha colocado una lámpara de luz cálida detrás de las pantallas para cansar menos la vista cuando graba por la noche. Todo el cableado va recogido por detrás de la mesa para que en cámara se vea ordenado.</p>
  <p><img src="imagenes/logo.png" alt="Logo del canal de Lucía" style="width:120px; float:none;"> Este es el logo del canal. No flota: se queda en la línea del texto, como si fuera una letra más.</p>
</body>
</html>
```
### Pregunta:

¿Qué diferencia hay entre `left`, `right` y `none`?

### Respuesta a la pregunta

- `float: left`: la imagen se pega a la **izquierda** y el texto la rodea por la derecha.
- `float: right`: la imagen se pega a la **derecha** y el texto la rodea por la izquierda.
- `float: none` (el valor por defecto): la imagen **no flota**. Se queda en su sitio dentro del texto y este no la rodea.

### Recordatorio:

- Para que se note que el texto rodea la imagen, el párrafo tiene que ser más largo que la imagen. Si no, pon la imagen más pequeña con `width`.
- Borde: `border: grosor estilo color;` → `border:5px solid green;`.

# B3. ¿Qué formato elijo?

> Escribe cinco párrafos, cada uno con una necesidad, e indica con `<strong>` el formato recomendado y su extensión: foto de vacaciones con muchos colores; logo con fondo transparente; icono nítido a cualquier tamaño; animación corta tipo meme; icono de la pestaña del navegador. Incluye **al menos dos imágenes de formatos distintos**.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B3. ¿Qué formato elijo?</title>
</head>
<body>
  <h1>¿Qué formato de imagen elijo?</h1>
  <p>Para una foto de vacaciones con muchos colores: <strong>JPEG (.jpg)</strong>, porque comprime bien las fotografías y ocupa poco.</p>
  <p>Para un logo con fondo transparente: <strong>PNG (.png)</strong>, porque admite transparencia y no pierde calidad.</p>
  <p>Para un icono que se vea nítido a cualquier tamaño: <strong>SVG (.svg)</strong>, porque es vectorial y no se pixela al ampliarlo.</p>
  <p>Para una animación corta tipo meme: <strong>GIF (.gif)</strong>, porque admite animación y lo abre cualquier navegador.</p>
  <p>Para el icono de la pestaña del navegador: <strong>ICO (.ico)</strong>, el formato clásico del favicon.</p>
  <h2>Ejemplos</h2>
  <img src="imagenes/setup.jpg" alt="Ejemplo de fotografía en JPEG" style="width:240px;">
  <img src="imagenes/logo.png" alt="Ejemplo de logo en PNG" style="width:160px;">
  <img src="imagenes/meme.gif" alt="Ejemplo de animación en GIF" style="width:160px;">
</body>
</html>
```

### Recordatorio
 
| Necesidad | Formato |
|-----------|---------|
| Fotografía con muchos colores | JPEG (`.jpg`) |
| Fondo transparente | PNG (`.png`) |
| Nítido a cualquier tamaño | SVG (`.svg`) |
| Animación | GIF (`.gif`) o APNG (`.apng`) |
| Icono de la pestaña (favicon) | ICO (`.ico`) |

# B4. Mis enlaces favoritos

> Tres enlaces a webs reales, cada uno en su `<p>`: uno a https://www.w3.org/ en la **misma ventana**, uno a https://www.google.com/ en **ventana nueva** y uno a tu elección en ventana nueva. Cambia el **color** de uno con `style`. **Pregunta:** ¿de qué color se ve por defecto un enlace por visitar y uno ya visitado?

### Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B4. Mis enlaces favoritos</title>
</head>
<body>
  <h1>Mis enlaces favoritos</h1>
  <p><a href="https://www.w3.org/">W3C, el organismo que crea los estándares web</a></p>
  <p><a href="https://www.google.com/" target="_blank">Google, en una pestaña nueva</a></p>
  <p><a href="https://developer.mozilla.org/es/" target="_blank" style="color:darkorange;">MDN, documentación de HTML y CSS</a></p>
</body>
</html>
```

### Pregunta:

¿de qué color se ve por defecto un enlace por visitar y uno ya visitado?

### Respuesta:

Por defecto un enlace **por visitar** se ve **azul y subrayado**, y uno **ya visitado**, **morado**. Mientras se pulsa (enlace activo), se ve **rojo**.

### Recordatorio

| Atributo | Para qué sirve |
|----------|----------------|
| `href` | Destino del enlace |
| sin `target` (o `target="_self"`) | Se abre en la misma ventana |
| `target="_blank"` | Se abre en una pestaña nueva 

#  B5. Enlaces con imagen

> Un enlace cuyo **rótulo es solo una imagen** (a una web externa, en pestaña nueva) y otro cuyo rótulo es **una imagen y un texto a la vez**. En un comentario, identifica el **destino**, el **rótulo** y el **objetivo** de cada enlace.

### Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B5. Enlaces con imagen</title>
</head>
<body>
  <h1>Enlaces con imagen</h1>
  <p><a href="https://www.w3.org/" target="_blank"><img src="imagenes/logo.png" alt="Ir a la web del W3C" style="width:150px;"></a></p>
  <p><a href="https://developer.mozilla.org/es/"><img src="imagenes/icono.svg" alt="Icono de MDN" style="width:32px;"> Documentación de MDN</a></p>
  <!--
    Enlace 1: destino https://www.w3.org/, rótulo la imagen logo.png, objetivo _blank (pestaña nueva).
    Enlace 2: destino https://developer.mozilla.org/es/, rótulo la imagen icono.svg y el texto
    "Documentación de MDN", objetivo la misma ventana (no lleva target).
  -->
</body>
</html>
```

### Partes de un enlace
 
| | Enlace 1 | Enlace 2 |
|---|--------|----------|
| **Destino** (`href`) | https://www.w3.org/ | https://developer.mozilla.org/es/ |
| **Rótulo** (lo que se pulsa) | La imagen `logo.png` | La imagen `icono.svg` y el texto "Documentación de MDN" |
| **Objetivo** (`target`) | `_blank`: pestaña nueva | Sin `target`: misma ventana |


### Recordatorio
 
- El rótulo es todo lo que va entre `<a>` y `</a>`: un texto, una imagen o las dos cosas
- Si el rótulo es solo una imagen, su `alt` debe decir adónde lleva el enlace ("Ir a la web del W3C")


  # B6. Mini web de tres páginas

  > Crea `index.html`, `sobre-mi.html` y `contacto.html`, cada una con un `<h1>` distinto y un menú con **enlaces relativos** a las otras dos. En `index.html`, una imagen de la subcarpeta `imagenes`; en `contacto.html`, un enlace **absoluto** a una web externa. **Pregunta:** ¿qué enlaces dejarían de funcionar si movieras `contacto.html` a otra carpeta


 ### Código : `index.html`
 
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Inicio</title>
</head>
<body>
  <h1>Bienvenido a mi web</h1>
  <p><a href="sobre-mi.html">Sobre mí</a> | <a href="contacto.html">Contacto</a></p>
  <img src="imagenes/logo.png" alt="Logo de mi web" style="width:200px;">
  <p>Esta es la página principal de mi mini web.</p>
</body>
</html>
```

### Código: `sobre-mi.html`
 
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Sobre mí</title>
</head>
<body>
  <h1>Sobre mí</h1>
  <p><a href="index.html">Inicio</a> | <a href="contacto.html">Contacto</a></p>
  <p>Estudio 2.º de SMR, me gusta el Jazz, aprender sobre IA en distintos foros y la fotografía.</p>
</body>
</html>
```

### Código: `contacto.html`
 
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Contacto</title>
</head>
<body>
  <h1>Contacto</h1>
  <p><a href="index.html">Inicio</a> | <a href="sobre-mi.html">Sobre mí</a></p>
  <p>Puedes ver mis proyectos en <a href="https://github.com/" target="_blank">GitHub</a>.</p>
</body>
</html>
```

### Pregunta:

¿Qué enlaces dejarían de funcionar si movieras `contacto.html` a otra carpeta?

Si `contacto.html` se mueve a otra carpeta (por ejemplo `paginas/`), dejan de funcionar:
- Los enlaces de `index.html` y `sobre-mi.html` que apuntan a `contacto.html` porque ya no está en la misma carpeta (habría que poner `paginas/contacto.html`).
- Los enlaces del menú de `contacto.html` a `index.html` y `sobre-mi.html`, porque ahora tendrían que subir una carpeta (`../index.html`).


# B7. Tu propia chuleta

> Haz una chuleta de una página con lo aprendido hasta ahora y guárdala en **PDF**. Crea `chuleta.html` con un `<h1>` y tres enlaces: al PDF local en la misma ventana, al PDF local en **pestaña nueva** y a un recurso con **URL externa**. **Pregunta:** ¿qué pasa si borras el PDF de la carpeta?
 
`chuleta.pdf` va en la misma carpeta que `chuleta.html`.

### Código: 

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B7. Mi chuleta</title>
</head>
<body>
  <h1>Mi chuleta de HTML</h1>
  <p><a href="chuleta.pdf">Abrir la chuleta en esta ventana</a></p>
  <p><a href="chuleta.pdf" target="_blank">Abrir la chuleta en una pestaña nueva</a></p>
  <p><a href="https://developer.mozilla.org/es/docs/Web/HTML" target="_blank">Documentación de HTML en MDN</a></p>
</body>
</html>
```

### Pregunta

¿Qué pasa si borras el PDF de la carpeta?

### Respuesta

Si se borra `chuleta.pdf`, los dos enlaces locales dejan de funcionar: el navegador muestra un error de **archivo no encontrado** (en un servidor web, el error **404**). El enlace externo a MDN sigue funcionando, porque no depende de tu carpeta.

### Recordatorio:

- Un enlace puede llevar a cualquier archivo, no solo a páginas: PDF, imágenes, documentos...
- El navegador abre el PDF en su propio visor


# Parte C. Práctica 2. Las estaciones (enlaces e imágenes)

> Crea una página `estaciones.html` con **4 imágenes de 300 × 300 píxeles** que sean enlaces a `otono.html`, `invierno.html`, `primavera.html` y `verano.html`. Estas páginas también las creas tú, con la estructura base, un `<h1>` con el nombre de la estación, la foto en grande (**600 × 600**) y un enlace de vuelta a `estaciones.html`.
>
> - `estaciones.html`: `<h1>` con el texto ESTACIONES; después, un `<h2>` con el título de cada estación y su foto a 300 × 300 (**no recortes** la imagen). Cada foto lleva un **borde de 5 píxeles de un color distinto**. Al hacer clic en la foto se abre la página de la estación en la **misma ventana**.
> - Cada página de estación: título, foto a 600 × 600 con **borde del mismo color** que en la página principal y, debajo, un enlace con el texto "Volver a la página principal".
> - Todas las imágenes llevan atributo `alt`.


### Reflexión previa
 
**1. ¿Qué ruta relativa usará `estaciones.html` para cargar `primavera.jpg`?**
 
`imagenes/primavera.jpg`: desde la carpeta de `estaciones.html` se entra en `imagenes` y se coge el archivo.
 
**2. ¿Qué pasaría si movieras las páginas de cada estación a una carpeta `paginas/`?**
 
Se romperían las rutas. Esas páginas tendrían que subir una carpeta para encontrar las fotos (`../imagenes/primavera.jpg`) y para volver (`../estaciones.html`), y `estaciones.html` tendría que enlazar a `paginas/primavera.html`.
 
**3. Si las fotos miden 600 × 600 y deben verse a 300 × 300, ¿las recortas o cambias el tamaño con HTML/CSS?**
 
Cambio el tamaño con CSS (`width:300px; height:300px;`). Así se usa la misma foto en las dos páginas, no se pierde ninguna parte y, como es cuadrada, no se deforma.

### Estructura de ficheros
 
```text
estaciones/
├── imagenes/
│   ├── primavera.jpg
│   ├── verano.jpg
│   ├── otono.jpg
│   └── invierno.jpg
├── estaciones.html
├── primavera.html
├── verano.html
├── otono.html
└── invierno.html
```

