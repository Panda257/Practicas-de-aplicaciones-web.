## Parte C.  Formato de texto

> Crea un documento HTML con la estructura básica, copia el texto de la tarea (`SMR-2-AWE-UD02-T1.txt`) y dale formato:
> - El **título** con encabezado de tamaño 2, **centrado** y con un **borde sólido** de 1 píxel.
> - Los **8 párrafos**, cada uno con su etiqueta de párrafo y alineación **justificada**.
> - Los **comentarios de los personajes** (lo que va entre comillas dobles) en **cursiva**.
> - Cada **sentimiento o cualidad humana** en un color distinto y en **negrita** (el mismo sentimiento, siempre del mismo color).
> - La **última frase**, en mayúsculas, en negrita, con color de letra y de fondo distintos, **el doble de grande** y empezando en una **línea nueva**.
> - Un **color de fondo** para toda la página.


### Preguntas de reflexión previas
 
**1. El texto tiene 8 párrafos y debe verse justificado. ¿Qué etiqueta usarás para cada uno y qué propiedad CSS consigue la justificación?**
 
Cada párrafo va en su propia etiqueta `<p>`, y se justifica con la propiedad `text-align: justify;` en el `style` de cada uno.
 
**2. Los comentarios irán en cursiva y los sentimientos, en color y negrita. ¿Qué etiquetas sirven para marcar solo una parte de un párrafo?**
 
Las etiquetas **en línea**, que no saltan de línea: `<i>` (o `<em>`) para la cursiva de los comentarios, y `<b>` (o `<strong>`/`<span>`) con `style="color:...;"` para los sentimientos.
 
**3. Un mismo sentimiento debe tener siempre el mismo color. ¿Cómo evitas equivocarte?**
 
Haciendo antes una lista con cada sentimiento y su color (en este texto hay 27) y usándola siempre. Para no dejarme ninguno, busco cada palabra con **Ctrl+F** en el Visual Studio Code.

### Código
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Práctica 1. Formato de texto</title>
</head>
<body style="background-color:oldlace;">
  <h2 style="text-align:center; border:1px solid gray;">EL AMOR Y LA LOCURA</h2>
  <p style="text-align:justify;">Cuentan que una vez se reunieron en un lugar de la Tierra todos los sentimientos y cualidades de los hombres. Cuando el <b style="color:gray;">aburrimiento</b> había bostezado por tercera vez, la <b style="color:darkorange;">locura</b>, como siempre tan loca, les propuso: <i>"¿Jugamos al escondite?"</i>. La <b style="color:indigo;">intriga</b> levantó la ceja intrigada y la <b style="color:teal;">curiosidad</b>, sin poder contenerse, preguntó: <i>"¿Al escondite? ¿Y cómo es eso?"</i>. <i>"Es un juego -explicó la <b style="color:darkorange;">locura</b>- en el que yo me tapo la cara y comienzo a contar desde uno hasta un millón mientras ustedes se esconden. Y, cuando yo haya terminado de contar, el primero de ustedes al que encuentre ocupará mi lugar para continuar el juego"</i>.</p>
  <p style="text-align:justify;">El <b style="color:orangered;">entusiasmo</b> bailó secundado por la <b style="color:deeppink;">euforia</b>. La <b style="color:goldenrod;">alegría</b> dio tantos saltos que terminó por convencer a la <b style="color:slateblue;">duda</b> e, incluso a la <b style="color:rosybrown;">apatía</b>, a la que nunca le interesaba nada. Pero no todos quisieron participar; la <b style="color:navy;">verdad</b> prefirió no esconderse, ¿para qué?, si, al final, siempre la hallaban; y la <b style="color:purple;">soberbia</b> opinó que era un juego muy tonto, pero en el fondo, lo que le molestaba es que la idea no hubiese sido suya. Y la <b style="color:olive;">cobardía</b>... la <b style="color:olive;">cobardía</b> prefirió no arriesgarse. <i>"Uno, dos, tres..."</i>, comenzó a contar la <b style="color:darkorange;">locura</b>.</p>
  <p style="text-align:justify;">La primera en esconderse fue la <b style="color:sienna;">pereza</b> que, como siempre, se dejó caer en la primera piedra del camino. La <b style="color:steelblue;">fe</b> subió al cielo y la <b style="color:green;">envidia</b> se escondió tras la sombra del <b style="color:darkcyan;">triunfo</b> que con su propio esfuerzo había logrado subir a la copa del árbol más alto. La <b style="color:seagreen;">generosidad</b> casi no alcanzaba a esconderse, cada sitio que hallaba le parecía maravilloso para alguno de sus amigos: que si un lago cristalino, ideal para la <b style="color:palevioletred;">belleza</b>; que si una rendija de un árbol, perfecto para la <b style="color:cadetblue;">timidez</b>; que si el vuelo de una mariposa, lo mejor para la <b style="color:mediumvioletred;">voluptuosidad</b>; que si una ráfaga de viento, magnífico para la <b style="color:dodgerblue;">libertad</b>. Así que terminó por ocultarse en un rayito de sol. El <b style="color:saddlebrown;">egoísmo</b>, en cambio, encontró un sitio muy bueno desde el principio; lo encontró ventilado, cómodo... pero eso sí, sólo para él. La <b style="color:darkslategray;">mentira</b> se escondió en el fondo de los océanos, ¡<b style="color:darkslategray;">mentira</b>! en realidad se escondió detrás del arco iris. Y la <b style="color:red;">pasión</b> y el <b style="color:firebrick;">deseo</b> en el centro de los volcanes. El <b style="color:maroon;">olvido</b>... ¡se me olvidó dónde se escondió! pero, bueno, eso no es lo importante.</p>
  <p style="text-align:justify;">Cuando la <b style="color:darkorange;">locura</b> contaba 999.999, el <b style="color:crimson;">amor</b> aún no había encontrado sitio para esconderse, pues todo se encontraba ocupado, hasta que divisó un rosal y, enternecido, decidió esconderse entre sus flores.</p>
  <p style="text-align:justify;"><i>"Un millón"</i> contó la <b style="color:darkorange;">locura</b>, y comenzó a buscar. La primera en aparecer fue la <b style="color:sienna;">pereza</b>, sólo a tres pasos de la piedra. Después escuchó a la <b style="color:steelblue;">fe</b> discutiendo con Dios en el cielo sobre teología. Y la <b style="color:red;">pasión</b> y el <b style="color:firebrick;">deseo</b> los sintió en el vibrar de los volcanes. En un descuido encontró al <b style="color:darkcyan;">triunfo</b> y, claro, pudo deducir dónde estaba la <b style="color:green;">envidia</b>. Al <b style="color:saddlebrown;">egoísmo</b> no tuvo ni que buscarlo, él solito salió disparado desde su escondite, que había resultado ser un nido de avispas.</p>
  <p style="text-align:justify;">De tanto caminar sintió sed y, al acercarse al lago, descubrió a la <b style="color:palevioletred;">belleza</b>. Y con la <b style="color:slateblue;">duda</b> resultó más fácil todavía, pues la encontró sentada sobre una cerca sin decidir aún en qué lado esconderse.</p>
  <p style="text-align:justify;">Así fue encontrando a todos: la <b style="color:darkslategray;">mentira</b> detrás del arco iris, ¡<b style="color:darkslategray;">mentira</b>! estaba en el fondo del océano; y hasta el <b style="color:maroon;">olvido</b>, al que ya se le había olvidado que estaba jugando al escondite. Pero, sólo el <b style="color:crimson;">amor</b> no aparecía por ninguna parte. La <b style="color:darkorange;">locura</b> buscó detrás de cada árbol, bajo cada rolluelo del planeta, en la cima de las montañas; y, cuando estaba por darse por vencida, divisó un rosal y sus rosas, y tomó una horquilla y comenzó a mover sus ramas bruscamente. Cuando, de pronto... un doloroso grito se escuchó. Las espinas habían herido en los ojos al <b style="color:crimson;">amor</b>. La <b style="color:darkorange;">locura</b> no sabía qué hacer para disculparse: lloró, rogó, imploró, pidió perdón y hasta prometió ser su Lazarillo.</p>
  <p style="text-align:justify;">Y desde entonces, desde que por primera vez se jugó al escondite en la Tierra:<br>
    <b style="color:white; background-color:black; font-size:200%;">EL AMOR ES CIEGO Y LA LOCURA SIEMPRE LE ACOMPAÑA.</b></p>
</body>
</html>
```

### Tabla de sentimientos y colores:

| Sentimiento o cualidad | Color |
|------------------------|-------|
| Amor | `crimson` |
| Locura | `darkorange` |
| Aburrimiento | `gray` |
| Intriga | `indigo` |
| Curiosidad | `teal` |
| Entusiasmo | `orangered` |
| Euforia | `deeppink` |
| Alegría | `goldenrod` |
| Duda | `slateblue` |
| Apatía | `rosybrown` |
| Verdad | `navy` |
| Soberbia | `purple` |
| Cobardía | `olive` |
| Pereza | `sienna` |
| Fe | `steelblue` |
| Envidia | `green` |
| Triunfo | `darkcyan` |
| Generosidad | `seagreen` |
| Belleza | `palevioletred` |
| Timidez | `cadetblue` |
| Voluptuosidad | `mediumvioletred` |
| Libertad | `dodgerblue` |
| Egoísmo | `saddlebrown` |
| Mentira | `darkslategray` |
| Pasión | `red` |
| Deseo | `firebrick` |
| Olvido | `maroon` |

### Recordatorio
| Qué se tiene que hacer | Cómo se hace |
|------------------------|--------------|
| Título centrado con borde | `<h2 style="text-align:center; border:1px solid gray;">` |
| Párrafos justificados | `<p style="text-align:justify;">` en cada párrafo |
| Comentarios en cursiva | `<i>"..."</i>` alrededor de cada frase entre comillas |
| Sentimiento en color y negrita | `<b style="color:crimson;">amor</b>` |
| Última frase en línea nueva | `<br>` justo antes de la frase |
| Última frase el doble de grande | `font-size:200%;` |
| Fondo de toda la página | `<body style="background-color:oldlace;">` |
