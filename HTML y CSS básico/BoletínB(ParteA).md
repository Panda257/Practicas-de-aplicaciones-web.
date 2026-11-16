# Parte A1. Comprobación y reflexión

## A1. Verdadero o falso
| N.º | Afirmación | V / F | Respuesta y corrección |
|-----|------------|-------|------------------------|
| 1 | "La etiqueta `<img>` se cierra con `</img>`." | **F** | `<img>` es una etiqueta vacía y **no se cierra**. |
| 2 | "El atributo `alt` muestra un texto si la imagen no se puede cargar." | **V** | Además, lo leen los lectores de pantalla y los buscadores. |
| 3 | "Para dar ancho y alto a una imagen se recomienda usar `style` en lugar de `width` y `height`." | **V** | Así el tamaño es CSS y no lo cambia sin querer una hoja de estilos. |
| 4 | "La propiedad `float` permite que una imagen flote a la izquierda o a la derecha del texto, o que no flote." | **V** | Valores `left`, `right` y `none`. |
| 5 | "El rótulo de un enlace solo puede ser un texto." | **F** | El rótulo puede ser un **texto, una imagen o las dos cosas**. |
| 6 | "`target="_blank"` hace que el enlace se abra en una ventana (pestaña) nueva." | **V** | Sin `target`, se abre en la misma ventana. |
| 7 | "Por defecto, un enlace ya visitado se ve azul y uno por visitar, morado." | **F** | Es al revés: **por visitar, azul** y subrayado; **visitado, morado**. |
| 8 | "Un enlace relativo escribe la URL completa, incluido el dominio." | **F** | Eso es un enlace **absoluto**. El relativo indica la ruta desde la página actual (`paginas/contacto.html`). |

### **Recordatorio**
> **Enlace absoluto:** lleva la dirección completa (protocolo + dominio + ruta). Funciona desde cualquier sitio.
>
> `https://github.com/usuario/practicas-AppsWebs/blob/main/Tema2/html-y-css.md`
>
> **Enlace relativo:** solo indica la ruta desde el archivo en el que estoy.
>
> ```text
> practicas-AppsWebs/
> ├── README.md
> ├── Tema1/
> │   ├── mariadb-y-wordpress.md
> │   └── img/
> │       └── captura.png
> └── Tema2/
>     └── html-y-css.md
> ```
>
> Desde `Tema1/mariadb-y-wordpress.md`:
>
> | Quiero ir a | Enlace relativo |
> |-------------|-----------------|
> | La captura | `img/captura.png` |
> | El README | `../README.md` |
> | Los apuntes de HTML | `../Tema2/html-y-css.md` |
>
> `../` = subir una carpeta.

forma más sencilla de entenderlo:

- **Absoluto** = la dirección completa de una casa, con ciudad y calle: llegas desde cualquier sitio.
- **Relativo** = "la puerta de al lado" o "el piso de arriba": solo funciona según dónde estés

# ParteA2 Relaciona atributo y función

| Elemento | Descripción | Respuesta |
|----------|-------------|-----------|
| 1. `src` | D. Ruta del archivo de imagen | **1-D** |
| 2. `alt` | G. Texto que se muestra si la imagen no carga | **2-G** |
| 3. `href` | B. Indica el destino del enlace | **3-B** |
| 4. `target` | F. Indica dónde se abrirá el destino del enlace | **4-F** |
| 5. `id` | A. Crea un marcador (bookmark) dentro de la página | **5-A** |
| 6. `float` | E. Propiedad CSS para que la imagen flote junto al texto | **6-E** |
| 7. `_blank` | C. Valor de `target` que abre una pestaña nueva | **7-C** |

# ParteA3. ¿Absoluto o relativo?

| N.º | Dirección | Tipo | Por qué |
|-----|-----------|------|---------|
| 1 | `https://www.w3.org/` | **Absoluto** | Lleva protocolo y dominio. |
| 2 | `paginas/contacto.html` | **Relativo** | Ruta desde la carpeta de la página actual. |
| 3 | `/css/default.asp` | **Relativo** (a la raíz) | Empieza por `/`: se busca desde la carpeta raíz del sitio web, pero sin dominio. |
| 4 | `https://www.google.com/` | **Absoluto** | Lleva protocolo y dominio. |
| 5 | `./apuntes.pdf` | **Relativo** | `./` significa "la carpeta actual". |
| 6 | `imagenes/logo.png` | **Relativo** | Entra en la subcarpeta `imagenes`. |

## A4. Formatos de imagen

| Abreviatura | Nombre completo | Extensión |
|-------------|-----------------|-----------|
| GIF | Graphics Interchange Format | `.gif` |
| JPEG | Joint Photographic Experts Group | `.jpg`, `.jpeg` |
| PNG | Portable Network Graphics | `.png` |
| SVG | Scalable Vector Graphics | `.svg` |
| ICO | Microsoft Icon | `.ico` |
| APNG | Animated Portable Network Graphics | `.apng` |

# A5. Caza los errores de la galería

### Código original (con fallos)
 
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Mi galería</title>
</head>
<body>
<h1>Mi viaje de fin de curso</h1>
<img>src="playa.jpg" alt="Playa al atardecer"</img>
<img src="monte.jpg" style="width=300px; height=200px;">
<a href=https://www.wikipedia.org target="_blank">Más información sobre el destino
</body>
</html>
```

### Errores encontrados
 
| N.º | Error | Explicación | Corrección |
|-----|-------|-------------|------------|
| 1 | `<img>src="playa.jpg" ...` | Los atributos están **fuera** de la etiqueta: se cierra `<img>` y luego se escriben como texto. | `<img src="playa.jpg" alt="Playa al atardecer">` |
| 2 | `</img>` | `<img>` no se cierra. | Quitar `</img>`. |
| 3 | `width=300px; height=200px;` | En CSS, propiedad y valor se separan con `:`, no con `=`. | `width:300px; height:200px;` |
| 4 | Segunda imagen sin `alt` | Todas las imágenes deben llevar `alt`. | `alt="Vista del monte"` |
| 5 | Enlace sin cerrar | Falta `</a>`: el enlace no termina nunca. | Añadir `</a>`. |
| 6 | `href=https://...` sin comillas | Las normas del curso piden poner siempre los valores entre comillas. | `href="https://www.wikipedia.org"` |
| 7 | Falta `lang` y `meta author` | Mejora y norma del boletín. | `<html lang="es">` y `<meta name="author">` |

### Versión corregida

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Mi galería</title>
</head>
<body>
  <h1>Mi viaje de fin de curso</h1>
  <img src="playa.jpg" alt="Playa al atardecer">
  <img src="monte.jpg" alt="Vista del monte" style="width:300px; height:200px;">
  <a href="https://www.wikipedia.org" target="_blank">Más información sobre el destino</a>
</body>
</html>
```

## A6. Rutas que no funcionan
> proyecto/
> ├── index.html
> ├── contacto.html
> ├── apuntes.pdf
> └── imagenes/
>   ├── logo.png
>   └── equipo.jpg

Suponiendo que el código está en index.html, indica **cuáles funcionan y cuáles no**, y corrige las que fallen:

>```
> <img src="logo.png" alt="Logo">
> <img src="imagenes/equipo.jpg" alt="Equipo">
> <a href="Contacto.html">Contacto</a>
> <a href="apuntes.pdf">Apuntes</a>
> <a href="imagenes/apuntes.pdf">Apuntes</a>
> <img src="imagenes/equipo.png" alt="Equipo">
>```
