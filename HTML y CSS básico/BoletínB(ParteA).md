# Parte A. Comprobación y reflexión

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

**Recordatorio**
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
