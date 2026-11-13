# B1. Tu plantilla para todo el curso

### Crea `plantilla.html` con la estructura básica y, en `<head>`, la codificación utf-8, un `<title>` ("Plantilla de 2.º SMR") y dos `<meta>:` descripción y autor. En el `body>` escribe un comentario que diga Aquí va el contenido. La usarás como punto de partida en el resto del boletín.

```html
<!DOCTYPE html>                <!-- Le dice al navegador que es HTML5 -->
<html lang="es">               <!-- Raíz de la página; lang = idioma -->
<head>                         <!-- Información SOBRE la página (no se ve) -->
  <meta charset="utf-8">       <!-- Codificación: tildes y ñ bien -->
  <meta name="description" content="...">  <!-- Resumen para Google -->
  <meta name="author" content="TU NOMBRE"> <!-- Autor -->
  <title>Plantilla de 2.º SMR</title>      <!-- Texto de la pestaña -->
</head>
<body>                         <!-- Todo lo que SÍ se ve -->
  <!-- Aquí va el contenido -->
</body>
</html>
```

| Pieza | Para qué sirve | ¿Se ve en la página? |
|-------|----------------|----------------------|
| `<!DOCTYPE html>` | Indica que el documento es HTML5 | No |
| `<html lang="es">` | Etiqueta raíz; el idioma ayuda a buscadores y lectores de pantalla | No |
| `<meta charset="utf-8">` | Sin esto las tildes y la ñ salen como `Ã±` | No |
| `<meta name="description">` | Texto que muestra Google debajo del enlace | No |
| `<meta name="author">` | Autor de la página (lo exige el boletín en **todas** las páginas) | No |
| `<title>` | Texto de la **pestaña** del navegador | Solo en la pestaña |
| `<!-- ... -->` | Comentario: nota para el programador | **No**, nunca |

# B2. La noticia del día: ¿la IA te quitará el trabajo?
### Te toca maquetar la primera noticia del periódico digital de tu instituto:
1. Un `<h1>` con el titular y un `<h2>`
2. Tres párrafos  `<p>`, entre el segundo y el tercero, una **línea horizontal**.
3. Al final, un bloque de tres líneas (autor, fecha y fuente) separadas solo con `<br>`, sin `<p>`.
4. Una sección aparte titulada "Prueba de tamaños" con los **seis niveles de encabezado** (h1 a h6)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B2. La noticia del día</title>
</head>
<body>
  <h1>¿La IA te quitará el trabajo?</h1>
  <h2>Entradilla de la noticia...</h2>
  <p>Primer párrafo...</p>
  <p>Segundo párrafo...</p>
  <hr>
  <p>Tercer párrafo...</p>
  Autor: CLAUDIO<br>
  Fecha: 11 de noviembre de 2026<br>
  Fuente: Periódico digital del instituto
  <h2>Prueba de tamaños</h2>
  <h1>Encabezado de nivel 1</h1>
  <h2>Encabezado de nivel 2</h2>
  <h3>Encabezado de nivel 3</h3>
  <h4>Encabezado de nivel 4</h4>
  <h5>Encabezado de nivel 5</h5>
  <h6>Encabezado de nivel 6</h6>
</body>
</html>
```

# B3. Ficha de oferta: el Black Friday de tu tienda
> Crea la ficha de un producto tecnológico usando **todas** estas etiquetas al menos una vez y en frases con sentido: `<b>` · `<strong>` · `<i>` · `<em>` · `<mark>` · `<small>` · `<del>` · `<ins>` · `<u>` · `<sub>` · `<sup>`.

> **Pregunta (en un comentario del código):** ¿qué diferencia visual hay entre `<b>` y `<strong>`? ¿Y entre `<i>` y `<em>`? ¿Para qué crees que existen dos etiquetas distintas?

### Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B3. Ficha de oferta</title>
</head>
<body>
  <h1>Black Friday: Oppo X9  X</h1>
  <p><strong>¡Oferta válida solo durante 24 horas!</strong></p>
  <p>Precio: <del>999 €</del> <ins>759 €</ins></p>
  <p>Pantalla de <b>6,59 pulgadas<sup>1</sup></b> con una superficie de 123,30 cm<sup>2</sup>.</p>
  <p>Batería de <mark>7025 mAh</mark> con carga rápida (<i>fast charging</i>) de 80 W.</p>
  <p>Su carcasa de aluminio reciclado genera <em>un 30 % menos</em> de CO<sub>2</sub>.</p>
  <p><u>Envío gratis</u> a toda España.</p>
  <p><small><sup>1</sup>Oferta válida hasta fin de existencias.</small></p>
  <!--
    Pregunta: ¿qué diferencia visual hay entre <b> y <strong>? ¿Y entre <i> y <em>? ¿Por qué existen dos etiquetas?
    Respuesta: visualmente no hay diferencia. <b> y <strong> se ven en negrita, e <i> y <em> en cursiva.
    La diferencia es el significado: <strong> marca algo importante y <em> un énfasis, mientras que
    <b> e <i> solo cambian el aspecto. Existen las dos para separar significado y aspecto: los lectores
    de pantalla y los buscadores entienden <strong> y <em>.
  -->
</body>
</html>
```
### Qué hace cada etiqueta
| Etiqueta | Se ve | Uso en la ficha |
|----------|-------|-----------------|
| `<b>` | Negrita | "6,59 pulgadas" (dato destacado) |
| `<strong>` | Negrita | Aviso importante de la oferta |
| `<i>` | Cursiva | Palabra en inglés (*fast charging*) |
| `<em>` | Cursiva | Énfasis en "un 30 % menos" |
| `<mark>` | Fondo amarillo | Resaltar la batería |
| `<small>` | Letra pequeña | Frase legal |
| `<del>` | Tachado | Precio antiguo |
| `<ins>` | Subrayado | Precio nuevo |
| `<u>` | Subrayado | "Envío gratis" |
| `<sub>` | Subíndice | El 2 de CO₂ |
| `<sup>` | Superíndice | Nota¹ y cm² 

# B4. El banner del streamer
> Con el atributo `style`: un `<h1>` con fondo `lightblue`; un `<h2>` **centrado**; un `<h3>` **a la derecha** con fondo `limegreen` (las dos propiedades en el mismo `style`); un párrafo en rojo y otro en azul; y un párrafo con tamaño de letra al **150 %**. Recuerda: propiedad y valor se separan con `:` y cada par termina con `;`.

## Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B4. El banner del streamer</title>
</head>
<body>
  <h1 style="background-color:lightblue;">Directo esta noche</h1>
  <h2 style="text-align:center;">Estreno de temporada</h2>
  <h3 style="text-align:right; background-color:limegreen;">Sorteo de una tarjeta gráfica</h3>
  <p style="color:red;">Empezamos a las 21:00.</p>
  <p style="color:blue;">Invitados sorpresa durante el directo.</p>
  <p style="font-size:150%;">¡No te lo pierdas!</p>
</body>
</html>
```

# B5. Paleta de colores de tu marca
> Una startup te pide cuatro titulares `<h2>` con **el mismo color escrito de cuatro formas**: nombre estándar, rgb, hex y hsl. Los cuatro deben verse exactamente igual.

> **Parte 1.** Hazlo con estos colores:
>
> | Color | rgb | hex | hsl |
> |---|---|---|---|
> | Rojo | rgb(255, 0, 0) | #ff0000 | hsl(0, 100%, 50%) |
> | Naranja | rgb(255, 165, 0) | #ffa500 | hsl(39, 100%, 50%) |
>
> **Parte 2.** Averigua el nombre estándar de `#3cb371` y el código hex de `rgb(238, 130, 238)` y compruébalo en pantalla.
>
> **Parte 3 (reflexión, en un comentario).** ¿Qué significa `rgb(0, 0, 255)`? ¿Qué valor de *hue* corresponde en hsl al rojo, al verde y al azul?

### Código(paleta de colores):

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B5. Paleta de colores</title>
</head>
<body>
  <h1>Paleta de colores de la marca</h1>
  <h2 style="color:red;">Rojo con nombre: red</h2>
  <h2 style="color:rgb(255, 0, 0);">Rojo en rgb: rgb(255, 0, 0)</h2>
  <h2 style="color:#ff0000;">Rojo en hex: #ff0000</h2>
  <h2 style="color:hsl(0, 100%, 50%);">Rojo en hsl: hsl(0, 100%, 50%)</h2>
  <h2 style="color:orange;">Naranja con nombre: orange</h2>
  <h2 style="color:rgb(255, 165, 0);">Naranja en rgb: rgb(255, 165, 0)</h2>
  <h2 style="color:#ffa500;">Naranja en hex: #ffa500</h2>
  <h2 style="color:hsl(39, 100%, 50%);">Naranja en hsl: hsl(39, 100%, 50%)</h2>
  <h2 style="color:mediumseagreen;">#3cb371 se llama mediumseagreen</h2>
  <h2 style="color:#3cb371;">El mismo color en hex: #3cb371</h2>
  <h2 style="color:rgb(238, 130, 238);">rgb(238, 130, 238)</h2>
  <h2 style="color:#ee82ee;">En hex es #ee82ee (violet)</h2>
  <!--
    Reflexión: rgb(0, 0, 255) significa rojo 0, verde 0 y azul 255 (el máximo): es el azul puro.
    En hsl, el hue (tono) es un ángulo de la rueda de color: rojo = 0, verde = 120 y azul = 240.
  -->
</body>
</html>
```

### Respuestas 2 y 3
**Parte 2** (comprobado en el navegador):
- `#3cb371` se llama **mediumseagreen**.
- `rgb(238, 130, 238)` en hex es **`#ee82ee`**, que corresponde al color **violet**.

**Parte 3:** `rgb(0, 0, 255)` significa rojo 0, verde 0 y azul 255 (el máximo): es el **azul puro**. En hsl el *hue* (tono) es un ángulo de la rueda de color: **rojo = 0**, **verde = 120** y **azul = 240**.

### RECORDATORIO (se me olvida siempre)
 
| Forma | Cómo se lee | Ejemplo |
|-------|-------------|---------|
| Nombre | Nombre en inglés | `red` |
| rgb | Rojo, verde y azul, de 0 a 255 | `rgb(255, 0, 0)` |
| hex | Lo mismo que rgb, en hexadecimal (`#RRGGBB`) | `#ff0000` |
| hsl | Tono (0-360), saturación (%) y luminosidad (%) | `hsl(0, 100%, 50%)` |

# B6. El menú del ramen con tipografías de repuesto

> Define `font-family` con **varias fuentes en cascada** (si falta la primera, se usa la siguiente): un título en una fuente `cursive`, una descripción en `sans-serif`, los precios en `monospace` y un párrafo con una fuente **inventada** como primera opción y otra real de repuesto.

> **Pregunta:** ¿por qué debe ser fácil de leer el tipo de letra de un sitio web?

### Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B6. Menú del ramen</title>
</head>
<body>
  <h1 style="font-family:'Brush Script MT', 'Comic Sans MS', cursive;">Ramen del Barrio</h1>
  <p style="font-family:Verdana, Arial, sans-serif;">Caldo cocinado durante 12 horas, fideos frescos hechos a mano y huevo marinado.</p>
  <p style="font-family:'Courier New', Courier, monospace;">Ramen de miso ........ 11,50 €</p>
  <p style="font-family:'Courier New', Courier, monospace;">Ramen de shoyu ....... 10,90 €</p>
  <p style="font-family:FuenteQueNoExiste, Georgia, serif;">Este párrafo pide una fuente inventada; como no existe, el navegador usa Georgia.</p>
</body>
</html>
```
### Respuesta a la pregunta:

Porque el objetivo de una web es comunicar y si cuesta leer, el usuario se cansa y se marcha. Además una letra clara es más accesible para personas con dificultades de visión o de lectura y se lee mejor en pantallas pequeñas.

# B7. Cartel de festival con `<span>` y bordes

> 1. Un `<h1>` con **borde de 5 px, línea continua y verde**.
> 2. Un párrafo con **borde punteado azul de 3 px**.
> 3. Un párrafo con fondo `lightpink` y **borde doble rojo de 5 px**.
> 4. Una frase con los nombres de dos artistas destacados con `<span>`: uno en azul y otro en verde al **200 %**.

> **Pregunta:** ¿qué diferencia hay entre `<span>` y `<p>` para destacar parte de un texto?

### Código: 

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B7. Cartel de festival</title>
</head>
<body>
  <h1 style="border:5px solid green;">Festival de Otoño 2026</h1>
  <p style="border:3px dotted blue;">Tres días de música al aire libre en el parque central.</p>
  <p style="background-color:lightpink; border:5px double red;">Entradas a la venta desde el lunes.</p>
  <p>Este año actúan <span style="color:blue;">Los Satélites</span> y <span style="color:green; font-size:200%;">Luna Roja</span>.</p>
</body>
</html>
```

### Respuesta a la pregunta

`<p>` es un elemento de **bloque** siempre empieza en una línea nueva y ocupa todo el ancho, así que no sirve para destacar una palabra dentro de una frase porque la partiría. `<span>` es un elemento **en línea**: no cambia de línea y no tiene aspecto propio, así que permite aplicar un estilo solo a un trozo del texto sin romper la frase.

# B8. Etiquetas anidadas: el mensaje urgente

> Una alerta del servicio de ciberseguridad debe verse **subrayada, en negrita y en cursiva a la vez**. Escribe la frase abriendo en la secuencia `<b>` `<i>` `<u>` y cerrando en el orden correcto; anota en un comentario cuál es la secuencia de cierre y por qué. Después prueba una versión **mal cerrada** y observa qué hace el navegador.

### Código:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>B8. Mensaje urgente</title>
</head>
<body>
  <p><b><i><u>Alerta: se ha detectado un acceso no autorizado a tu cuenta.</u></i></b></p>
  <!--
    Secuencia de cierre: </u></i></b>, el orden inverso al de apertura (<b><i><u>).
    Las etiquetas se anidan como cajas dentro de cajas: la última que se abre es la primera que se cierra.
  -->
</body>
</html>
```

### Versión mal cerrada

```html
<p><b><i><u>Cambia tu contraseña ahora.</b></i></u></p>
<p><b><i>Revisa tu correo</b> y tus mensajes</i> hoy mismo.</p>
```

**Qué hace el navegador** (comprobado):
- La primera frase se ve **igual que el código bien escrito**, el navegador corrige el error por su cuenta.
- En la segunda, el navegador deja " y tus mensajes" en **cursiva** aunque ya se había cerrado `<b>` el formato "se escapa" a texto que no tocaba.
- El validador del W3C marca las dos líneas como error ("End tag violates nesting rules").

Aunque se vea bien, eso no quiere decir que se dejará el código así, hay que dejarlo siempre en el orden correspondiente.
