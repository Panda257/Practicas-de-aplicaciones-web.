# Parte A. Comprobación y reflexión
## A1. Verdadero  o falso (corregir las falsas)

| N.º | Afirmación | V / F | Respuesta y corrección |
|-----|------------|-------|------------------------|
| 1 | "HTML es un lenguaje de programación como Python: sirve para hacer cálculos y tomar decisiones." | **F** | HTML es un lenguaje de **marcado**: describe la estructura y el contenido de una página (títulos, párrafos, imágenes...). No hace cálculos ni toma decisiones. |
| 2 | "La etiqueta `<br>` no necesita etiqueta de cierre." | **V** | Es una etiqueta vacía: no envuelve contenido, así que no se cierra. |
| 3 | "El valor de un atributo siempre se escribe entre comillas." | **V** | Es la norma que seguimos: `<a href="inicio.html">`. Son obligatorias si el valor lleva espacios. (HTML5 tolera valores simples sin comillas, pero conviene ponerlas siempre.) |
| 4 | "Los atributos de una etiqueta se escriben en la etiqueta de cierre." | **F** | Los atributos se escriben en la etiqueta de **apertura**: `<p style="color:red;">texto</p>`. La de cierre solo lleva el nombre: `</p>`. |
| 5 | "El texto de `<title>` aparece en la pestaña del navegador." | **V** | Es el título que se ve en la pestaña y en los resultados de los buscadores. |
| 6 | "`<strong>` y `<b>` se visualizan igual." | **V** | Los dos se ven en negrita. La diferencia es de significado: `<strong>` indica importancia fuerte y `<b>` es solo un estilo visual. |
| 7 | "Todo lo que escribimos dentro de `<head>` se ve en la página." | **F** | `<head>` contiene información sobre la página (codificación, título, autor, estilos). Lo que se ve en la página va dentro de `<body>`. |
| 8 | "La etiqueta `<hr>` se cierra con `</hr>`." | **F** | `<hr>` es una etiqueta vacía (línea horizontal) y no se cierra: se escribe solo `<hr>`. |
| 9 | "Un comentario HTML (`<!-- ... -->`) se muestra en pantalla como una nota gris." | **F** | Los comentarios **no se muestran** en pantalla. Solo se ven en el código fuente. |
| 10 | "`<span>` crea un bloque de texto que siempre empieza en una línea nueva." | **F** | `<span>` es un elemento **en línea**: marca un trozo de texto dentro de una línea sin saltar a otra. El que crea un bloque es `<p>` (o `<div>`). |


## A2 Relacionar etiqueta y efecto
Une cada etiqueta con lo que hace (por ejemplo: 1-C).


| Etiqueta | Efecto | Respuesta |
|----------|--------|-----------|
| 1. `<mark>` | B. Texto remarcado, como con un fosforito | **1-B** |
| 2. `<del>` | A. Texto tachado (precio antiguo de una oferta) | **2-A** |
| 3. `<sub>` | E. Texto en subíndice (como en H₂O) | **3-E** |
| 4. `<sup>` | F. Texto en superíndice (como en m²) | **4-F** |
| 5. `<small>` | D. Texto más pequeño que el normal | **5-D** |
| 6. `<em>` | C. Texto enfatizado (se ve como cursiva) | **6-C** |
| 7. `<ins>` | G. Texto insertado (se ve subrayado) | **7-G** |

## A3. Caza los errores
Un compañero ha entregado este código para la web de una tienda de gadgets y tiene fallos. Encuéntralos, anótalos y escribe la versión corregida. (Pista: hay al menos 5.)

```
<html>
<head>
<title>Mi tienda de gadgets
</head>
<body>
<h1>Ofertas de otoño</h2>
<p>Auriculares con <b>cancelación de ruido</p></b>
</body>
</html>
```

Conteo de fallos:
| N.º | Error | Por qué está mal | Corrección |
|-----|-------|------------------|------------|
| 1 | Falta `<!DOCTYPE html>` al principio | Sin él, el navegador no sabe qué versión de HTML usar y puede mostrar la página en modo de compatibilidad. | Añadir `<!DOCTYPE html>` en la primera línea. |
| 2 | `<title>` no está cerrado | Falta `</title>`. El navegador toma como título **todo lo que sigue**: la pestaña muestra código y la página se ve en blanco. | `<title>Mi tienda de gadgets</title>` |
| 3 | Falta `<meta charset="utf-8">` en `<head>` | Sin la codificación, letras como la **ñ** de "otoño" pueden verse mal. | Añadir `<meta charset="utf-8">`. |
| 4 | `<h1>` se cierra con `</h2>` | La etiqueta de cierre debe ser la del mismo nivel que la de apertura. | `<h1>Ofertas de otoño</h1>` |
| 5 | Etiquetas mal anidadas: `<b>...</p></b>` | `<b>` se abre dentro de `<p>`, pero se cierra fuera. Las etiquetas se cierran en **orden inverso** al de apertura (la última en abrirse es la primera en cerrarse). | `<p>Auriculares con <b>cancelación de ruido</b></p>` |
| 6 | Falta `<meta name="author">` | Las normas del boletín piden autor en el `<head>` de todas las páginas. | Añadir `<meta name="author" content="Tu nombre">`. |
| 7 | Falta el idioma en `<html>` | Es recomendable para buscadores y lectores de pantalla. | `<html lang="es">` |

Los errores están del 1 al 5, los errores 6 y 7 son mejoras.

Versión corregida:

```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Tu nombre">
  <title>Mi tienda de gadgets</title>
</head>
<body>
  <h1>Ofertas de otoño</h1>
  <p>Auriculares con <b>cancelación de ruido</b></p>
</body>
</html>
```
## A4. Estilos rotos
El community manager de un streamer ha escrito estas líneas para el banner de su canal. Ninguna se ve como debería. Explica qué falla en cada una y corrígela.

```
<h1 style="color:red font-size:40px;">Directo esta noche</h1>
<p style="text-align=center;">Estreno de temporada</p>
<p style="background-color:yellow;">Sorteo de una tarjeta gráfica<p>
```
### ¿Qué falla en cada línea?

| Línea | Qué falla | Qué se ve | Corrección |
|-------|-----------|-----------|------------|
| 1. `<h1>` | Falta el `;` que separa `color:red` de `font-size:40px`. El navegador lee `red font-size:40px` como un solo valor, no lo entiende y **ignora las dos propiedades**. | El título sale en negro y con el tamaño normal. | `style="color:red; font-size:40px;"` |
| 2. `<p>` centrado | Entre propiedad y valor se usa `=` en lugar de `:`. | El texto queda alineado a la izquierda. | `style="text-align:center;"` |
| 3. `<p>` amarillo | El párrafo se "cierra" con `<p>` en lugar de `</p>`: falta la barra. | Se abre un párrafo nuevo y vacío que añade un hueco de más. | `...tarjeta gráfica</p>` |

### Código corregido

```
<h1 style="color:red; font-size:40px;">Directo esta noche</h1>
<p style="text-align:center;">Estreno de temporada</p>
<p style="background-color:yellow;">Sorteo de una tarjeta gráfica</p>
```

## A5. Comentarios y anidación
Un aviso de ciberseguridad tiene dos errores. Encuéntralos y corrígelos.

```
<!- Revisar el texto antes de publicar ->
<p>Tu contraseña debe tener <strong><em>al menos 12 caracteres</strong></em>.</p>
```
## Errores encontrados

| N.º | Error | Explicación | Corrección |
|-----|-------|-------------|------------|
| 1 | El comentario está mal escrito | Un comentario HTML se abre con `<!--` y se cierra con `-->` (dos guiones en cada lado). Aquí solo hay uno. El navegador lo tolera, pero no es un comentario válido y el validador del W3C lo marca como error. | `<!-- Revisar el texto antes de publicar -->` |
| 2 | Las etiquetas `<strong>` y `<em>` se cruzan | Se abre `<strong>` y luego `<em>`, pero se cierra primero `</strong>`. Hay que cerrar en orden inverso: la última en abrirse es la primera en cerrarse. | `<strong><em>...</em></strong>` |

### Código corregido

```
<!-- Revisar el texto antes de publicar -->
<p>Tu contraseña debe tener <strong><em>al menos 12 caracteres</em></strong>.</p>
```

## A6. ¿Qué verá el usuario?
Sin abrir el navegador, dibuja o describe lo que se mostrará. Después compruébalo y anota si acertaste.

```
<h1>Resumen de la jornada</h1>
<p>Ha ganado el equipo local.<br>El rival se despide del torneo.</p>
<hr>
<h4>Próximo partido</h4>
<p>Sábado a las 18:00</p>
```

El usuario verá:


# RESUMEN DE LA JORNADA
ha ganado el equipo local

El rival se despide del torneo

### Próximo partido
Sábado a las 18:00

--------------------------------------------------------

### De arriba abajo, el navegador mostrará:

1. **"Resumen de la jornada"** en letra muy grande y en negrita (es un encabezado de nivel 1).
2. Un párrafo de **dos líneas** seguidas, sin hueco entre ellas, porque `<br>` hace un salto de línea sin abrir un párrafo nuevo:
   - Ha ganado el equipo local.
   - El rival se despide del torneo.
3. Una **línea horizontal** gris que ocupa todo el ancho de la página.
4. **"Próximo partido"** en negrita y con un tamaño mucho menor que el título (encabezado de nivel 4, casi del tamaño del texto normal).
5. Un párrafo con **"Sábado a las 18:00"** en letra normal.




# Parte B. Ejercicios guiados

## B1. Tu plantilla para todo el curso
Crea plantilla.html con la estructura básica y, en <head>, la codificación utf-8, un <title> ("Plantilla de 2.º SMR") y dos <meta>: descripción y autor. En el <body> escribe un comentario que diga Aquí va el contenido. La usarás como punto de partida en el resto del boletín.


