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
1. falta cerrar el título `</title>`
2. La etiqueta H1 se cierra con H2
3. Está mal cerrada la etiqueta `<b>`
4. La etiqueta `<head>` está mal colocada, primero se cierra el `<title>` y después cerramos con el `<head>`

Versión corregida:

```
<html>
<head>
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
1. En la primera línea falta un punto y coma entre las propiedades CSS color y font size
Corregido:
`<h1 style="color:red; font-size:40px;">Directo esta noche</h1>`
2. En la segunda línea los valores de CSS se separan con dos puntos, no con un `=`
Corregido:
`<p style="text-align:center;">Estreno de temporada</p>`
3. En la tercera línea el cierre de párrafo está mal hecho
`<p style="background-color:yellow;">Sorteo de una tarjeta gráfica</p>`

## A5. Comentarios y anidación
Un aviso de ciberseguridad tiene dos errores. Encuéntralos y corrígelos.

```
<!- Revisar el texto antes de publicar ->
<p>Tu contraseña debe tener <strong><em>al menos 12 caracteres</strong></em>.</p>
```
1. La apertura de comentario está mal escrita, necesita 2 `--` y solo lleva uno
Corregido:
`<!-- Revisar el texto antes de publicar -->`
2. Las etiquetas se cierran en un orden incorrecto, primero es el cierre de `</em>` y luego el de `</strong>`
`<strong><em>al menos 12 caracteres</em></strong>`
3. En la página no se vería la letra "ñ" debido a que no está colocado el `Charset=UTF-8` 

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

