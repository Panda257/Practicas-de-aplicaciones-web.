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
  <p>Pantalla de <b>6,59 pulgadas<sup>1</sup></b></p>
  <p>Batería de <mark>7025 mAh</mark> con carga rápida (<i>fast charging</i>) de 80 W.</p>
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
