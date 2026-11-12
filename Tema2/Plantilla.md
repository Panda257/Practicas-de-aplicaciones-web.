
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
|---|---|---|
| `<!DOCTYPE html>` | Indica que el documento es HTML5 | No |
| `<html lang="es">` | Etiqueta raíz; el idioma ayuda a buscadores y lectores de pantalla | No |
| `<meta charset="utf-8">` | Sin esto las tildes y la ñ salen como `Ã±` | No |
| `<meta name="description">` | Texto que muestra Google debajo del enlace | No |
| `<meta name="author">` | Autor de la página (lo exige el boletín en **todas** las páginas) | No |
| `<title>` | Texto de la **pestaña** del navegador | Solo en la pestaña |
| `<!-- ... -->` | Comentario: nota para el programador | **No**, nunca |

## Atajo en VS Code
Escribe `!` en un archivo `.html` vacío y pulsa **Tab**: VS Code genera la estructura básica (Emmet). Después solo añades las dos `<meta>` y cambias el `<title>` y el `lang` (Emmet pone `en`).

## Para el examen
- `<meta>` **no tiene cierre** (es una etiqueta vacía, como `<br>` o `<hr>`).
- Los `<meta>` van **siempre en el `<head>`**, nunca en el `<body>`.
- `name` dice qué tipo de dato es y `content` es el valor.
- Lo que hay en `<head>` no se ve en la página, salvo el `<title>` en la pestaña.
