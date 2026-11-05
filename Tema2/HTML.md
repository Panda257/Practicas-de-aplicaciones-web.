# Parte A. Comprobación y reflexión
## A1. Verdadero  o falso (corregir las falsas)

| Nº | Afirmación | V/F |
|----|------------|-----|
| 1  | "HTML es un lenguaje de programación como Python: sirve para hacer cálculos y tomar decisiones." | F. Es un lenguaje de marcado 
| 2  | "La etiqueta `<br>` no necesita etiqueta de cierre." | V 
| 3  | "El valor de un atributo siempre se escribe entre comillas." | V
| 4  | "Los atributos de una etiqueta se escriben en la etiqueta de cierre." | F. Los atributos se escriben en la apertura, no en el cierre.
| 5  | "El texto de `<title>` aparece en la pestaña del navegador." | V
| 6  | `<strong>` y `<b>` se visualizan igual." | V
| 7  | "Todo lo que escribimos dentro de <head> se ve en la página." | V
| 8  | "La etiqueta `<hr>` se cierra con `</hr>.`" | V
| 9  | "Un comentario HTML `(<!-- ... -->)` se muestra en pantalla como una nota gris." | F. Un comentario en HTML no se muestra en la pantalla del navegador, se verá únicamente al inspeccionar la página.
| 10 | " `<span>` crea un bloque de texto que siempre empieza en una línea nueva." | F. Span es un elemento de línea, así que no empieza una nueva ni genera saltos de línea, se mantiene en la misma fila.

## A2 Relacionar etiqueta y efecto
Une cada etiqueta con lo que hace (por ejemplo: 1-C).


| Etiqueta |  | Efecto |
| -------- |--| ------ |
| 1. `<mark>` | B | A.Texto tachado (precio antiguo de una oferta)
| 2. `<del>` | A | B.Texto remarcado, como con un fosforito
| 3. `<sub>` | E | C. Texto enfatizado (se ve como cursiva)
| 4. `<sup>` | F | D. Texto más pequeño que el normal
| 5. `<small>` | D | E. Texto en subíndice (como en H2O)
| 6. `<em>` | C | F. Texto en superíndice (como en m2)
| 7. `<ins>` | G | G.Texto insertado (se ve subrayado)

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

