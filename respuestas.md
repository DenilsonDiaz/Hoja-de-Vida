# Respuestas de la tarea

## Parte 2 — Medición de la imagen

La imagen original tiene dimensiones de 716 píxeles de ancho por 987 píxeles de alto.

| Formato | Peso en KB | ¿Se ve peor? | ¿Dónde exactamente? |
|---|---:|---|---|
| Original JPEG | 44.34 KB | No | Es la imagen original usada como referencia. |
| JPG | 82.84 KB | No | Mantiene buena calidad y los detalles del rostro se observan claramente. |
| PNG | 492.19 KB | No | Se observa con buena calidad, pero ocupa mucho más espacio. |
| WebP | 42.39 KB | No de forma evidente | Puede existir una diferencia mínima en algunos detalles del cabello y el fondo, pero casi no se nota. |
| AVIF | 23.67 KB | No de forma evidente | La imagen conserva buena calidad; las pequeñas diferencias pueden notarse en el cabello, la piel o las zonas oscuras al ampliar la fotografía. |

### 5. ¿Cuál elegí para mi hoja de vida y por qué?

Elegí AVIF como primera opción para mi hoja de vida porque pesa solamente 23.67 KB y conserva una calidad visual adecuada. También incluí WebP y JPG como formatos de respaldo para los navegadores que no admitan AVIF.

### 6. ¿El resultado se parece al de la imagen de clase o salió distinto?

El resultado puede ser distinto al ejemplo de clase porque mi fotografía es un retrato y contiene detalles en el rostro, el cabello, la ropa y el fondo. El formato que ofrece el menor tamaño depende del contenido y de la cantidad de detalles presentes en la imagen.

# Parte 3 — Investigación

## Pregunta 1

### ¿Se puede cambiar de color, tamaño o tipografía el calendario del campo de fecha?

El calendario que aparece al utilizar un `<input type="date">` es proporcionado por el navegador y el sistema operativo. Por esa razón, HTML no permite modificar directamente su color, tamaño o tipografía. En algunos navegadores es posible personalizar pequeños detalles mediante CSS, pero el calendario completo no puede cambiarse de forma estándar, ya que cada navegador utiliza su propia implementación.

**Fuente:**
- https://developer.mozilla.org/es/docs/Web/HTML/Element/input/date

---

## Pregunta 2

### ¿Qué son `:valid` y `:invalid` y qué relación tienen con `required` y `min`?

`:valid` y `:invalid` son pseudoclases de CSS que indican si un campo de un formulario contiene un valor válido o no.

Por ejemplo, si un campo tiene el atributo `required` y el usuario lo deja vacío, ese campo se considera `:invalid`. Cuando el usuario escribe un valor correcto, pasa a ser `:valid`.

Lo mismo ocurre con atributos como `min`, `max`, `pattern` o `type="email"`, ya que ayudan al navegador a comprobar si la información ingresada cumple las condiciones establecidas.

**Fuente:**
- https://developer.mozilla.org/es/docs/Web/CSS/:valid
- https://developer.mozilla.org/es/docs/Web/CSS/:invalid

---





## Pregunta 3

### ¿Qué hace falta para que una imagen se adapte al ancho disponible y por qué no basta con cambiar el `width`?

Para que una imagen se adapte al tamaño de la pantalla es necesario utilizar CSS. Una técnica común es establecer un ancho máximo del 100% y una altura automática, por ejemplo:

```css
img {
    max-width: 100%;
    height: auto;
}
```

Cambiar únicamente el atributo `width` en HTML no hace que la imagen sea adaptable a diferentes tamaños de pantalla. El navegador seguirá utilizando ese valor fijo, mientras que CSS permite que la imagen cambie de tamaño según el espacio disponible.

**Fuente:**
- https://developer.mozilla.org/es/docs/Learn/CSS