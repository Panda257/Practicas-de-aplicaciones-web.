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
<p>Segundo párrafo...</p>
<hr>
<p>Tercer párrafo...</p>

Autor: TU NOMBRE<br>
Fecha: 11 de noviembre de 2026<br>
Fuente: Periódico digital del instituto
```

```
<hr>
<h2>Prueba de tamaños</h2>
<h1>Encabezado de nivel 1</h1>
<h2>Encabezado de nivel 2</h2>
<h3>Encabezado de nivel 3</h3>
<h4>Encabezado de nivel 4</h4>
<h5>Encabezado de nivel 5</h5>
<h6>Encabezado de nivel 6</h6>
```
