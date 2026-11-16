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

