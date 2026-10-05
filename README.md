# Reto CSS: da estilo a la página

El archivo `index.html` ya está preparado, pero la página todavía necesita su hoja de estilos.

Tu tarea es crear `styles.css`. El objetivo no es copiar un CSS terminado: observa el HTML, identifica qué elementos necesitan estilo y construye el diseño paso a paso.

## Antes de empezar

Revisa la estructura de `index.html` e identifica:

- `body`, `header`, `main`, `section` y `footer`
- `figure` e imágenes
- `h1`, `h2`, `h3` y párrafos
- `nav` y enlaces
- listas, `details` y `summary`
- cajas de contenido

Antes de elegir un selector, pregúntate:

> ¿Quiero modificar todos los elementos de este tipo o solamente algunos?

## 1. Configuración general

### Variables CSS

Declara la paleta global en `:root`. Los valores están disponibles en la ayuda del HTML. Usa nombres que describan la función del color, por ejemplo: fondo, principal, secundario, acento, botón, blanco, fondo suave y fondo destacado.


### `body`

Elimina el margen predeterminado y define el fondo general, color de texto, tipografía del sistema, tamaño de lectura cómodo e interlineado.

## 2. Estructura principal

### `header`

Debe diferenciarse del resto con un degradado, espacio interior y el color de texto correspondiente. Consulta la ayuda desplegable del HTML para el degradado.

### `figure` y logo del encabezado

Centra el contenido de todos los `figure`. Añade una clase específica a la imagen/logo del `header` para que sea pequeña, cuadrada, circular, con borde visible y sin deformación. Investiga `width`, `height`, `border-radius` y `object-fit`.

### `h1`

El único título principal debe tener color secundario, tamaño y grosor destacados, alineación centrada y márgenes verticales controlados.

### Navegación y enlaces

Haz que `nav` sea un bloque independiente dentro del `header`: añade separación, `padding`, borde, esquinas redondeadas, fondo ligeramente transparente y contenido centrado.

En los enlaces, elimina el subrayado, hereda el color del contenedor y añade separación. Para esta versión no necesitas Flexbox.

### `main`

El contenido principal debe ocupar la mayor parte del ancho disponible, tener un ancho máximo, adaptarse a pantallas pequeñas, centrarse horizontalmente y mantener margen vertical. Combina ancho relativo, `max-width` y `margin: auto`.

### Secciones, títulos y párrafos

Todas las `section` comparten fondo claro, borde, esquinas ligeramente redondeadas, `padding` y margen inferior.

- Los `h2` usan el color secundario, destacan claramente y controlan el margen superior.
- Los `h3` usan el color de acento y son menos importantes que los `h2`, pero mayores que un párrafo.
- Todos los párrafos necesitan una pequeña separación inferior.

## 3. Las ocho clases

Usa clases solo cuando un elemento deba diferenciarse de otros del mismo tipo. No inventes una clase por elemento.

| Clase | Uso | Características principales |
| --- | --- | --- |
| Imagen/logo | Imagen del `header` | Cuadrada, circular, borde y sin deformación |
| Destacado | Llamar la atención | Fondo especial, borde izquierdo y `padding` |
| Recordatorio | Avisos reutilizables | Fondo, borde completo, esquinas y `padding` |
| Ejemplo | Zona de experimentación | Fondo suave, borde, margen y `padding` |
| Caja de ejemplo | Visualizar el Box Model | Fondo destacado, borde grueso, margen y `padding` |
| Caja formativa | Agrupar explicaciones | Reutilizable, fondo, borde, margen y `padding` |
| Caja auto | Extender una caja formativa | Ancho limitado y centrado |
| Imagen del tema | Imagen del contenido | Flexible, ancho máximo, borde y sin deformación |

### Contenido destacado

Localiza el párrafo que explica que una misma clase puede utilizarse en diferentes elementos. Añade una clase para darle un fondo distinto, un borde de acento solo a la izquierda y `padding`.

### Recordatorios

Identifica los párrafos que actúan como avisos. Todos deben compartir una clase con fondo relacionado con el fondo general, borde completo, esquinas redondeadas y `padding`.

### Ejemplo

En la sección de colores y tipografía, el párrafo destinado a experimentar necesita fondo suave, borde, esquinas redondeadas, margen vertical y `padding`.

### Listas

Aplica reglas compartidas a `ul` y `ol` mediante selectores separados por comas. Ambas listas necesitan fondo, esquinas redondeadas y espacio interior; cada `li` debe separarse del siguiente.

### Modelo de caja

El párrafo «Esta caja nos permite observar el modelo de caja» debe tener una clase con fondo destacado, borde grueso de acento, `padding` y margen exterior.

Los bloques sobre Padding, Margin, los cuatro lados y `margin: auto` deben reutilizar una misma clase: fondo suave, borde, esquinas, `padding` y margen vertical.

La caja que explica `margin: auto` debe llevar además una segunda clase que limite su ancho y la centre horizontalmente.

### Imagen del contenido

La imagen de la sección «Imágenes» debe tener su propia clase: debe adaptarse al espacio disponible, reducirse en pantallas pequeñas, tener un límite de crecimiento, mantener proporción, borde y esquinas ligeramente redondeadas. Usa especialmente `width` y `max-width`; no fijes altura si no hace falta.

### `details` y `summary`

Mantén su comportamiento nativo de abrir y cerrar; solo trabaja la presentación.

- `details`: margen vertical, `padding`, fondo suave, borde y esquinas redondeadas.
- `summary`: color, grosor, tamaño y cursor para indicar que es pulsable.

### `footer`

Selecciona directamente `footer`. Debe usar el color principal como fondo, texto claro, espacio interior y alineación centrada.

## ID, clases y etiquetas

En el HTML hay IDs como `fundamentos`, `selectores`, `colores`, `tamano`, `cajas`, `imagenes` y `recordatorio`. En este ejercicio no se usan para dar estilo: permiten que funcionen las anclas de la navegación interna, por ejemplo `href="#cajas"`.

Regla práctica:

> **ID** identifica y permite navegar a un elemento.  
> **Clase** agrupa elementos con un estilo reutilizable.  
> **Etiqueta** se usa cuando todos los elementos de ese tipo comparten estilo.

CSS permite los tres selectores, pero las clases suelen ser más fáciles de reutilizar y mantener.

## Orden recomendado

1. Variables.
2. Configuración general y `body`.
3. `header`, logo, `h1`, navegación y enlaces.
4. `main`, secciones, títulos y párrafos.
5. Clases de destacado, recordatorio y ejemplo.
6. Listas y cajas del Box Model.
7. Imagen del contenido, `details`, `summary` y `footer`.

Guarda y revisa el resultado en el navegador después de cada bloque.

## Lista de comprobación

- [ ] `styles.css` está conectado correctamente con el HTML.
- [ ] Los colores repetidos utilizan variables CSS.
- [ ] Se aplica `border-box` de forma general.
- [ ] El `body` no conserva el margen predeterminado.
- [ ] El contenido principal tiene ancho flexible y `max-width` cuando corresponde.
- [ ] Las clases se reutilizan y no hay clases innecesarias.
- [ ] Los selectores de etiqueta se emplean cuando todos los elementos comparten estilo.
- [ ] Las anclas del menú, `details` y `summary` funcionan sin JavaScript.
- [ ] Las imágenes mantienen su proporción y se adaptan al espacio.

## Objetivo final

No se trata de memorizar una hoja de estilos. Se trata de responder, para cada elemento:

> ¿Qué quiero conseguir? → ¿Qué elemento debo seleccionar? → ¿Qué propiedad CSS necesito?
