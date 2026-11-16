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
