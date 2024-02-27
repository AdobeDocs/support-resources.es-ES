---
title: Tablas
description: Uso de tablas de markdown y tablas de HTML.
hide: true
hidefromtoc: true
source-git-commit: 3779d588f21da83928bf0c71357afa90fd5f7179
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 3%

---

# Tablas

Matt estuvo aquí una y otra vez -

EDS

El Markdown estándar solo admite tablas básicas. Para AdobeDocs Markdown, tiene las siguientes opciones:

* Tablas de Markdown básicas
* tablas de HTML
* Tablas de Markdown con sintaxis de HTML limitada para saltos de párrafo (`<p>`), saltos de línea (`<br>`) y listas básicas (`<ul>`, `<ol>`).

## Conversión de tablas de HTML a tablas de Markdown

En algunos casos, deseará convertir una tabla de HTML en una tabla de Markdown o en texto de Markdown. Tal vez necesite mejorar el aspecto, resolver un error de validación o facilitar la edición en adelante.

Desafortunadamente, no hemos podido encontrar una sola herramienta que convierta bien las tablas de HTML. Normalmente utilizamos una combinación de herramientas para improvisar una mesa Markdown decente.

| Herramienta | Qué hace |
|--- |--- |
| [Generador de tablas de Markdown](https://www.tablesgenerator.com/markdown_tables) | Ideal para crear tablas de Markdown desde cero. |
| [Conversor de tablas avanzado](https://tableconvert.com/html-to-markdown) | Convierta tablas de cualquier formato a cualquier formato. <p>**Nota:** Los vínculos y las imágenes se acoplan cuando se convierten. |
| [Tabla básica html > Conversor de markdown](https://jmalarcon.github.io/markdowntables/) | Convertidor de HTML simple <p>**Nota:** Los vínculos y las imágenes se acoplan cuando se convierten. |
| [HTML no de tabla > Conversor de Markdown](https://codebeautify.org/html-to-markdown) | Convierte las tablas de HTML en sintaxis Markdown no de tabla. Se utiliza en combinación con las herramientas anteriores para copiar vínculos, imágenes y cualquier otro elemento aplanado. |

## Tablas de Markdown básicas

* Asegúrese de agregar al menos tres guiones en la segunda fila que determina las propiedades de la tabla. Ejemplo: `|--- |--- |--- |` para una tabla de 3 columnas.
* Las tablas de Markdown deben tener al menos una fila de encabezado y una fila de cuerpo. No se puede crear una tabla de markdown de una fila o de una celda (use el HTML en su lugar).
* Asegúrese de que cada fila tenga el mismo número de caracteres de barra vertical ( &amp;vert; ). Si necesita incluir un carácter de barra vertical dentro de una celda de tabla, escape precediéndolo de una barra invertida (`\|`) o utilizando el código de entidad HTML (`&vert;`).
* Tenga cuidado al utilizar bloques de código en las tablas. Los bloques de código en línea pueden causar anchos de columna desproporcionados.
* Puede cambiar el modo en que se representa la tabla especificando Auto o Fixed. Consulte [Cambio del modo en que se representan las tablas](#table-rendering).

## Creación de tablas de Markdown con HTML de bonus

Para facilitar la migración, hemos ampliado las tablas de Markdown para que admitan saltos de párrafo HTML (`<p>`), saltos de línea (`<br>`) y listas de HTML básicas (`<ul>` y `<ol>`) en las tablas de Markdown.

**Tabla de Markdown con saltos de línea y listas**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Ejemplo**

| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|--- |--- |--- |
| Fila normal | row 1 column 2 | row 1 column 3 |
| Salto de línea | primera línea de la celda<br>segunda línea de la celda | row 1 column 3 |
| Lista con viñetas | Lista con viñetas:<ul><li>Elemento 1</li><li>Elemento 2</li><li>Elemento 3</li></ul> | row 2 column 3 |
| Lista con viñetas con salto de línea | Lista con viñetas:<ul><li>Elemento 1</li><li>Elemento 2</li><li>Elemento 3</li></ul><br>Esta es una nueva línea después de la lista con viñetas | row 2 column 3 |

>[!IMPORTANT]
>
>Si decide utilizar HTML en tablas nativas, asegúrese de utilizar la sintaxis de HTML adecuada. Los errores en la sintaxis del HTML dan como resultado errores de validación difíciles de entender. Revise su trabajo.

## Uso de tablas de HTML

La herramienta de migración intentó conservar el mayor formato posible de la tabla original. La mayor parte de esta sintaxis del HTML se omite, mientras que parte de esta sintaxis provoca errores de validación.

**Ejemplo de tabla de HTML migrada**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**Procesado**

<table> 
 <tbody>
  <tr>
   <th>Propiedad</th> 
   <th>Tipo</th> 
   <th>Descripción del valor</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>Cadena[]</td> 
   <td><p><i>(Obligatorio)</i> Una cadena de varios valores de imágenes de distintivo hasta el número de badgingLevels. Las rutas de imagen del distintivo deben ordenarse para que la primera se asigne al experto más alto. Si hay menos distintivos que los indicados por badgingLevels, el último distintivo de la matriz rellena el resto de la matriz. Ejemplo de entrada:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Largo</td> 
   <td><p><i>(Opcional)</i> Especifica los niveles de experiencia que se van a otorgar. Por ejemplo, si debe haber un <code>expert </code>y un <code>almost expert</code> (dos distintivos), el valor debe establecerse en 2. badgingLevel debe corresponder al número de imágenes de distintivo relacionadas con expertos que aparecen en la propiedad badgingPath. El valor predeterminado es 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Cadena</td> 
   <td><p><i>(Obligatorio)</i> Identifica el motor de puntuación como "básico" o "avanzado". Configúrelo como "avanzado"; de lo contrario, el valor predeterminado es "básico".</p></td> 
  </tr>
 </tbody>
</table>

**Cuándo utilizar las tablas de HTML**

* Para equilibrar las columnas.
* Para omitir encabezados de tabla (las tablas de markdown deben tener una fila de encabezado).
* Para quitar el borde de una tabla de una fila (`<tr style="border: 0;">`).
* Para agregar espacios de columna o fila.
* Para alinear texto dentro de una celda de tabla.

**Notas para trabajar con tablas de HTML**

* No utilice la sintaxis Markdown en tablas de HTML. Por ejemplo, si agrega lo siguiente `[!NOTE]` en una tabla de HTML, se procesará tal cual (`[!NOTE]`). En su lugar, utilice la sintaxis del HTML para elementos como notas e imágenes.

  Las etiquetas Loc son una excepción a esta regla, ya que las etiquetas UICONTROL y DNL se eliminan antes de que se representen las páginas.

* No toda la sintaxis del HTML es compatible con las tablas. Los elementos de anchura, altura, color y otros elementos de sintaxis de HTML se omiten cuando se representan en EXL. Puede dejar estos valores en a menos que se produzcan errores de validación.
* Para alinear el texto, utilice `align: "left|center|right"` en HTML. Por ejemplo, para centrar el contenido de una celda de la tabla, utilice `<td align="center">`.
* Las tablas de HTML no pueden incluir tablas anidadas.

>[!TIP]
>
>Si desea desactivar un borde para una tabla de HTML de una fila, utilice esta sintaxis:
>
>```
><table>
><tr style="border: 0;">
>```

## Especificar cómo se representan las tablas {#table-rendering}

Podemos procesar tablas de dos maneras:

* **Fijo** (actualmente el valor predeterminado): incluye reglas personalizadas para procesar tablas, incluidas tablas de HTML con imágenes. Las tablas se representan como tablas de ancho completo sin desplazamiento, lo que a veces provoca que el texto se superponga.
* **Automático** - Similar a Git-flavored Markdown (GFM). Las tablas pueden desplazarse, por lo que el texto no se superpone.

En la mayoría de los casos, las tablas se representan con el mismo aspecto. Sin embargo, si la tabla incluye texto superpuesto, es recomendable que aplique la variable `auto` etiqueta. O bien, si la tabla del HTML con tarjetas de imagen no se está representando correctamente, puede que desee aplicar la variable `fixed` etiqueta.

Estamos considerando cambiar el valor predeterminado de `fixed` hasta `auto`.

## Edición de tablas de Markdown

Si desea especificar cómo se representa una tabla Markdown nativa, agregue una de estas líneas de sintaxis DESPUÉS de la tabla, con líneas en blanco antes y después de:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![renderización de tablas](assets/table-render.png)

### Edición de tablas de HTML

Si desea especificar cómo se representa una tabla de HTML, utilice una de estas líneas de sintaxis en la primera línea de la tabla:

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Cuándo usar Automático o Fijo

**Texto superpuesto**

Uso `auto` para tablas con bloques de código largos o texto que causa texto superpuesto cuando `fixed` (valor predeterminado) está seleccionado.

*Fijo (predeterminado)*

| Métrica de perspectivas | Descripción | Parámetro de consulta de ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Número total de mensajes de &quot;tipo&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.range.count** | Número total de mensajes de &quot;intervalo&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.format.count** | Número total de mensajes de &quot;formato&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.pattern.count** | Número total de mensajes de &quot;patrón&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.presence.count** | Número total de mensajes de &quot;presencia&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.enum.count** | Número total de mensajes &quot;enum&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |

{style="table-layout:fixed"}

*Automático*

| Métrica de perspectivas | Descripción | Parámetro de consulta de ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Número total de mensajes de &quot;tipo&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.range.count** | Número total de mensajes de &quot;intervalo&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.format.count** | Número total de mensajes de &quot;formato&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.pattern.count** | Número total de mensajes de &quot;patrón&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.presence.count** | Número total de mensajes de &quot;presencia&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |
| **timeseries.data.collection.validation.category.enum.count** | Número total de mensajes &quot;enum&quot; no válidos para un conjunto de datos o para todos ellos. | ID de conjunto de datos |

{style="table-layout:auto"}

**Tablas de HTML con imágenes equilibradas**

Uso `fixed` para tablas de HTML que requieren imágenes equilibradas que se desequilibran al `auto` está seleccionado. En este ejemplo, las imágenes tienen tamaños idénticos, pero hay más texto en la columna central.

*Automático*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Posible cliente" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Flujo de trabajo para posibles clientes de Adobe</strong></a>
    </div>
    <em>Flujo de trabajo de edición principal para redactores principales.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Poco frecuente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Flujo de trabajo para usuarios poco frecuentes</strong></a>
    </div>
    <em>¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validación" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validación</strong></a>
    </div>
    <em>Aprenda a resolver los errores de validación.</em>
    <br>
  </td>
</tr>
</table>

*Fijo (de más de una manera)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Posible cliente" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Flujo de trabajo para posibles clientes de Adobe</strong></a>
    </div>
    <em>Flujo de trabajo de edición principal para redactores principales.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Poco frecuente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Flujo de trabajo para usuarios poco frecuentes</strong></a>
    </div>
    <em>¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones. ¿No es un guionista? Aprenda las formas más sencillas de realizar contribuciones.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validación" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validación</strong></a>
    </div>
    <em>Aprenda a resolver los errores de validación.</em>
    <br>
  </td>
</tr>
</table>
