# Reto CSS: da estilo a una guía de fundamentos

Trabaja sobre `ejercicio.html`. Es el archivo del alumnado: conserva toda la estructura, los textos y los IDs de navegación, pero no tiene clases ni una hoja de estilos conectada.

Tu tarea es conectar tu hoja de estilos y construir el resultado paso a paso. No intentes terminarlo todo de una vez: haz un cambio, míralo en el navegador y explica qué ha cambiado.

## Antes de empezar

Revisa la estructura de `ejercicio.html` e identifica:

- `body`, `header`, `main`, `section` y `footer`
- `figure` e imágenes
- `h1`, `h2`, `h3` y párrafos
- `nav` y enlaces
- listas, `details` y `summary`
- cajas de contenido

Antes de elegir un selector, pregúntate:

> ¿Quiero modificar todos los elementos de este tipo o solamente algunos?

| Si quieres cambiar… | Elige primero… |
| --- | --- |
| Todos los elementos de un tipo | Un selector de etiqueta |
| Varios elementos con el mismo papel visual | Una clase reutilizable |
| El destino de un enlace interno | Un ID; en este reto no necesita estilos |

## 1. Configuración general

### Variables CSS

Declara una paleta global de ocho colores en `:root`. Los valores están disponibles en la ayuda del HTML: fondo, principal, secundario, acento, blanco, suave, destacado y aviso.

| Función | Valor |
| --- | --- |
| Fondo general | `#e8edf1` |
| Texto principal | `#30343F` |
| Títulos oscuros | `#1A1B41` |
| Acento | `#C62E65` |
| Blanco | `#FFFFFF` |
| Fondo suave | `#F0E9FF` |
| Destacado | `#FFF0B8` |
| Aviso | `#E3F2FD` |

Usa las variables cuando un color se repita. Si un color aparece una sola vez en una caja decorativa, puede escribirse directamente en esa regla.


### `body`

Elimina el margen predeterminado y define el fondo general, color de texto, tipografía del sistema, tamaño de lectura cómodo e interlineado.

Usa `1.6rem` para el texto de lectura y `1.6` como interlineado. Configura también el tamaño base para que `1rem` equivalga aproximadamente a `10px`, y aplica `box-sizing: border-box` de forma general.

## 2. Estructura principal

### `header`

Debe diferenciarse del resto con el degradado que aparece en la ayuda desplegable del HTML, `3rem` de espacio interior y el color de texto principal.

### `figure` y logo del encabezado

Centra el contenido de todos los `figure`. Añade una clase específica a la imagen/logo del `header`: ancho y alto de `8rem`, borde blanco de `3px` y radio al `50%`. La imagen original es cuadrada, por lo que no necesitas fijar ninguna propiedad adicional para recortarla.

### `h1`

El único título principal debe tener color secundario, tamaño `4rem`, grosor destacado, alineación centrada y márgenes verticales pequeños.

### Navegación y enlaces

Haz que `nav` sea un bloque independiente dentro del `header`: añade separación, `padding`, borde, esquinas redondeadas, fondo ligeramente transparente y contenido centrado.

En los enlaces, elimina el subrayado, hereda el color del contenedor y añade separación. Para esta versión no necesitas Flexbox.

### `main`

El contenido principal debe ocupar el `90%` del ancho de su contenedor padre y no superar `100rem`. Un porcentaje en `width` se calcula respecto al ancho disponible del padre: por eso se adapta a pantallas pequeñas. Centra el bloque con márgenes automáticos a izquierda y derecha y añade `2rem` de margen vertical.

### Secciones, títulos y párrafos

Todas las `section` comparten fondo claro, borde, esquinas ligeramente redondeadas, `padding` y margen inferior.

- Los `h2` usan el color secundario, tamaño `2.8rem` y sin margen superior.
- Los `h3` usan el color de acento y tamaño `2rem`.
- Todos los párrafos necesitan `1.5rem` de separación inferior.

## 3. Las nueve clases principales

Usa clases solo cuando un elemento deba diferenciarse de otros del mismo tipo. No inventes una clase por elemento.

Estas son las nueve clases reutilizables principales de la página.

| Clase | Uso | Características principales |
| --- | --- | --- |
| Imagen/logo | Imagen del `header` | Cuadrada, circular y con borde |
| Destacado | Llamar la atención | Fondo amarillo, borde izquierdo naranja y `padding` |
| Recordatorio | Avisos reutilizables | Fondo azul, borde completo, esquinas y `padding` |
| Ejemplo | Zona de experimentación | Fondo verde claro, borde discontinuo, margen y `padding` |
| Caja de ejemplo | Visualizar el Box Model | Fondo rosa, borde grueso fucsia, margen y `padding` |
| Caja formativa | Agrupar explicaciones | Fondo lila, borde morado, margen y `padding` |
| Caja auto | Explicar `margin: auto` | Ancho limitado y centrado |
| Caja desbordamiento | Mostrar contenido que no cabe | Altura limitada y `overflow: auto` |
| Imagen del tema | Imagen del contenido | Flexible, ancho máximo, borde y sin deformación |

### Contenido destacado

Localiza el párrafo que explica que una misma clase puede utilizarse en diferentes elementos. Añade una clase para darle un fondo amarillo, un borde naranja solo a la izquierda y `padding`. La propiedad que necesitas para ese único borde es `border-left`.

### Recordatorios

Identifica los párrafos que actúan como avisos. Todos deben compartir una clase con fondo azul, borde completo, esquinas redondeadas y `padding`.

### Ejemplo

En la sección de colores y tipografía, el párrafo destinado a experimentar necesita fondo verde claro, borde discontinuo, esquinas redondeadas, margen vertical y `padding`.

### Listas

Aplica reglas compartidas a `ul` y `ol` mediante selectores separados por comas. Ambas listas necesitan fondo, borde, esquinas redondeadas y espacio interior; cada `li` debe separarse del siguiente. Este es un buen caso para un selector de etiqueta compartido: no necesitas crear una clase.

### Modelo de caja

El párrafo que comienza «Esta es una caja real» debe tener una clase con fondo rosa, borde fucsia grueso, `padding` de `2rem` y margen exterior. Cambia una propiedad cada vez y responde: ¿ha aumentado el aire interior o la separación exterior?

Los bloques sobre Padding y Margin deben reutilizar una misma clase: fondo lila, borde morado, esquinas, `padding` de `2rem` y margen vertical. Si dos cajas tienen el mismo propósito visual, usa la misma clase.

La caja que explica `margin: auto` debe tener su propia clase, con el mismo aspecto que una caja formativa, pero con un ancho del `70%` y márgenes automáticos a izquierda y derecha. Prueba a modificar ese porcentaje: el espacio sobrante se reparte a ambos lados.

Para comparar tamaños, crea una caja content-box grande y coloca dentro otra caja border-box. Las dos clases deben declarar exactamente `width: 32rem`, `padding: 2rem` y un borde de `8px`. La única regla que debe cambiar es `box-sizing`.

Antes de mirar el resultado, responde: si el ancho solo mide el contenido, ¿qué ocurre al añadir padding y borde? Después comprueba que la caja exterior ocupa más espacio aunque ambas declaren las mismas medidas.

### Cuando el contenido no cabe

La caja de texto largo debe tener su propia clase, con el mismo aspecto que una caja formativa, una altura de `18rem` y `overflow: auto`.

Prueba, de uno en uno, los valores `visible`, `hidden`, `auto` y `scroll`. Antes de probar, predice qué ocurrirá con el texto y con la barra de desplazamiento. El objetivo final es `auto`: permite leer todo el texto sin que invada el resto de la página.

### Imagen del contenido

La imagen de la sección «Imágenes» debe tener su propia clase. Usa un ancho del `80%` respecto a su contenedor padre y limita su crecimiento a `60rem`. Añade un borde de `4px` con el color secundario y esquinas de `1rem`.

Usa esta sombra intensa para darle relieve:

```css
box-shadow: 0 22px 38px #1a1b41;
```

No declares `height`: así la imagen conserva su proporción natural.

### `details` y `summary`

Mantén su comportamiento nativo de abrir y cerrar; solo trabaja la presentación.

- `details`: margen vertical, `padding`, fondo suave, borde y esquinas redondeadas.
- `summary`: color secundario, grosor destacado y tamaño de `1.8rem`.

### `footer`

Selecciona directamente `footer`. Debe usar el color principal como fondo, texto blanco, `3rem` de espacio interior y alineación centrada.

## ID, clases y etiquetas

En el HTML hay IDs como `fundamentos`, `selectores`, `colores`, `tamano`, `cajas`, `desbordamiento`, `imagenes` y `recordatorio`. En este ejercicio no se usan para dar estilo: permiten que funcionen las anclas de la navegación interna, por ejemplo `href="#cajas"`.

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
7. La caja de contenido que desborda.
8. Imagen del contenido, `details`, `summary` y `footer`.

Guarda y revisa el resultado en el navegador después de cada bloque.

## Lista de comprobación

- [ ] La hoja de estilos está conectada correctamente con `ejercicio.html`.
- [ ] Los colores repetidos utilizan variables CSS.
- [ ] Se aplica `border-box` de forma general.
- [ ] El `body` no conserva el margen predeterminado.
- [ ] El contenido principal tiene ancho flexible y `max-width` cuando corresponde.
- [ ] Las clases se reutilizan y no hay clases innecesarias.
- [ ] Ningún elemento usa dos clases al mismo tiempo.
- [ ] Los selectores de etiqueta se emplean cuando todos los elementos comparten estilo.
- [ ] Las anclas del menú, `details` y `summary` funcionan sin JavaScript.
- [ ] Las imágenes mantienen su proporción y se adaptan al espacio.
- [ ] La caja larga permite leer todo el texto mediante scroll.

## Objetivo final

No se trata de memorizar una hoja de estilos. Se trata de responder, para cada elemento:

> ¿Qué quiero conseguir? → ¿Qué elemento debo seleccionar? → ¿Qué propiedad CSS necesito?
