# B1. Tu plantilla para todo el curso

Crea `plantilla.html` con la estructura básica y, en `<head>`, la codificación utf-8, un `<title>` ("Plantilla de 2.º SMR") y dos `<meta>:` descripción y autor. En el `body>` escribe un comentario que diga Aquí va el contenido. La usarás como punto de partida en el resto del boletín.

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
