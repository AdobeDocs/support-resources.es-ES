---
title: Guía de formato y sintaxis de la documentación colaborativa de Self Service Excellence
description: Introducción básica al estilo Markdown
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Guía de estilo de sintaxis de Markdown

Esta página ilustra el componente Markdown para la creación de documentación técnica de Digital Experience con el formato markdown (.md). Esta página incluye detalles para los empleados de Adobe.

EDS

Ver aquí: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Vea este [vídeo de AdobeDocs Markdown](https://video.tv.adobe.com/v/26165).

En su mayor parte, seguimos la sintaxis estándar de Git-flavored markdown (GFM) para dar formato al texto. Sin embargo, algunas sintaxis (como las líneas horizontales) no son compatibles y hemos ampliado Markdown de varias formas para adaptarlo a nuestras necesidades de documentación.

## Formato de texto básico

Un párrafo no requiere sintaxis especial en Markdown. Agregue una línea en blanco entre cada párrafo.

Para dar formato de **negrita** al texto, se escribe entre dos asteriscos:

```
This text is **bold**.
```

Para aplicar *cursiva* al texto, se escribe entre un solo asterisco:

```
This text is *italic*.
```

Para aplicar formato de ***negrita y cursiva*** al texto, se escribe entre tres asteriscos:

```
This is text is both ***bold and italic***.
```

Para omitir los caracteres de formato de Markdown, use `\` antes del carácter:

`This is not \*italicized\* type.`

Procesado: no es del tipo \*cursiva\*.

## Distintivos

En curso. Esperando a Loc.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Comillas de bloque

Nuestro sistema de creación utiliza la sintaxis de citas de bloque (`>` al principio de las líneas) para identificar las extensiones de markdown personalizadas para sugerencias, notas y vídeos. Puede crear citas de bloque reales agregando un carácter `>` delante de un párrafo.

>Esta es una cita.

```
>This is a blockquote quotation.
```

## Bloque de código (en línea){#code-block}

**Cuándo usar**

Se utiliza para procesar un fragmento de código en línea en una frase. Ideal para llamar a un nombre de cookie, nombre de archivo, valor o comando que no requiera un bloque de código delimitado por completo.

El contenido de los bloques de código se procesa tal cual y no está localizado. (La única excepción a esta regla es la sintaxis `` y ``, que se elimina durante el empaquetado para su publicación).

Utilice también bloques de código para direcciones URL de ejemplo que no deban validarse: `https://www.example.com`

**Sintaxis**

Un bloque de código utiliza comillas invertidas simples para incluir el elemento de código que desee resaltar.

```
This is `inline code` within a paragraph of text.
```

**Ejemplo**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>También puede ajustar el texto en comillas dobles (&grave;&grave;&amp;&grave;) para crear un bloque de código en línea. Esto resulta especialmente útil cuando necesita hacer referencia a un carácter de acento grave dentro de un bloque de código en línea. Por ejemplo:
>
>&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&amp;

## Bloque de código (delimitado)

**Cuándo usar**

Utilice un bloque de código para mostrar la sintaxis del código. Un bloque de código delimitado utiliza comillas triples para encerrar el elemento de código que desea resaltar. Agregue líneas en blanco encima y debajo del bloque de código delimitado.

Tenga en cuenta que los bloques de código no están localizados.

>[!TIP]
>
>Especifique un idioma al crear un bloque de código delimitado. Especificar un idioma permite resaltar la sintaxis específica de ese idioma y muestra un botón **Copiar** para los usuarios. También puede mostrar números de línea si especifica un idioma.

**Sintaxis**

Utilice tres acentos graves ( &grave;&grave;&grave; ) antes y después de las líneas de código. Asegúrese de que las comillas de apertura y cierre tienen la misma sangría de espacios. Para una representación óptima, especifique un lenguaje de código.

&grave;&grave;&grave;`javascript`

**Ejemplo**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### Resaltado de sintaxis para bloques de código

Experience League admite el resaltado de sintaxis para bloques de código. Asegúrese de especificar un idioma como `java` después del conjunto de comillas invertidas de apertura para asegurarse de que la sintaxis se resalte correctamente. Para ver una lista de idiomas válidos, consulte [https://prismjs.com](https://prismjs.com/#supported-languages). Si falta algún idioma, registre una incidencia Jira.

### Numeración de líneas en bloques de código

Añadir `{line-numbers="true"}` después del idioma para habilitar la numeración de líneas.

Ejemplo con números de línea (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Iniciar numeración en línea _**

Añada `start-number="n"` después de la sintaxis del número de línea para iniciar la numeración en un número distinto de 1.

Ejemplo con nueva línea de inicio (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Resaltado de líneas en bloques de código

Añada `highlight="n"` después de la sintaxis del número de línea para resaltar filas dentro de un bloque de código. Al especificar `11-13, 16`, se resaltarán las líneas 11 a 13 y 16.

Ejemplo con resaltado de líneas (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Formato de variables en bloques de código

La sintaxis de variables como `<i>italic</i>` no se admite en bloques de código. Para indicar texto de variable, una opción es usar corchetes angulares `< >`.

## Secciones contraíbles

Puede crear una sección contraíble (a veces denominada **acordeón**) que está oculta de forma predeterminada. El usuario puede hacer clic en el título para expandir o contraer la sección.

El texto contraíble se puede utilizar para simplificar el contenido complejo, como simplificar una página de preguntas frecuentes o eliminar el desorden de un procedimiento complejo con listas anidadas. Por ejemplo, en lugar de mostrar un conjunto de subpasos, puede contraerlos en una sección &quot;Ver detalles&quot;.

**Sintaxis**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**Ejemplo**

+++Ver detalles
Es texto dentro de una sección contraíble.

* Viñeta uno
* Viñeta dos
* Viñeta tres

+++

**Notas**

+++* No anide secciones contraíbles dentro de secciones contraíbles. Las secciones contraíbles anidadas no se representan correctamente. Sin embargo, no provocan errores en la validación, por lo que los usuarios verán la sintaxis `` de la sección anidada.
* Asegúrese de agregar líneas en blanco encima y debajo de elementos como listas de viñetas y bloques de código dentro de la sección contraíble; de lo contrario, se producirá un error de validación.
* Puede agregar encabezados dentro de secciones contraíbles, pero no es recomendable.
* [Los acordeones no siempre son la respuesta para contenido complejo en escritorios](https://www.nngroup.com/articles/accordions-complex-content/)
* Un inconveniente histórico de las secciones contraíbles es que **Buscar en la página** (Ctrl/Cmd+F) omite el texto contraído. Aunque esto sigue siendo así en Safari, ya no es así en Chrome; Buscar en página detecta el texto contraído en Chrome.
* Ejemplo de una página [actualizaciones de mantenimiento](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) que usa secciones contraíbles.

## Comentarios y observaciones

Los comentarios no aparecen en el sistema de ayuda procesado. Use comentarios para dejar notas para usted u otros escritores. También puede utilizar comentarios para secciones de texto de borrador.

Para los comentarios, tenga en cuenta que aunque no se representan en el sistema de ayuda, son visibles para los usuarios que editan archivos Markdown en GitHub.com. No incluya información confidencial en los comentarios.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

No debería poder ver el texto debajo de esto (&quot;No puede verme&quot;) a menos que esté editando el documento.

<!--
You can't see me (unless you're editing in Git).
-->

**Recordatorio:** Los comentarios (observaciones) no aparecen en los artículos de ayuda públicos. Sin embargo, los comentarios aparecen en los archivos públicos de Markdown que los usuarios pueden ver y editar.

>[!IMPORTANT]
>
>Evite añadir comentarios dentro de los componentes de bloque, como listas de viñetas, especialmente listas de viñetas anidadas. El comentario puede cambiar la forma en que se representa la lista con viñetas.
>
>En el archivo TOC.md, no comente las líneas en medio de la lista de TDC. Esto podría dividir la lista de índice y provocar errores de validación. En su lugar, mueva los comentarios del índice al final del archivo.

## CONTEXTUALHELP

Los autores pueden trabajar con los equipos de productos para agregar fuentes de ayuda en la interfaz de usuario del producto del Experience Cloud o el Experience Platform. Por ejemplo:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Listas de definición

Para las listas de definición, todavía no se admite la sintaxis estándar de Markdown. En su lugar, utilice un formato manual como este:

```
**Frog** - An amphibious green creature. Likes flies.
```

Procesado:

**Rana** - Una criatura verde anfibia. Le gustan las moscas.

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## Descargar archivos

Cargue el archivo .zip u otro archivo descargable en el directorio de recursos y, a continuación, vincúlelo. Si se trata de un archivo .zip, al hacer clic en el vínculo, se descargará el archivo. Si es un tipo de archivo como PDF o PNG que se puede abrir en un explorador, al hacer clic en el vínculo se abrirá una nueva pestaña. Para estos archivos, considere la posibilidad de comprimirlos o proporcionar instrucciones para hacer clic con el botón derecho en el vínculo y descargarlos.

`Download` &brack;`download-test.zip`&brack;`(assets/download-test.zip)`

Procesado:

Descargar [zip de prueba de descarga](assets/download-test.zip)

>[!NOTE]
>
>El tamaño máximo de archivo para archivos e imágenes de descarga es de 100 MB. Ese es el límite de github.com. El límite de git.corp.adobe.com es mayor (250 MB), pero necesitamos poder copiar archivos en el espejo de github.com.

## Encabezados {#headings}

En Markdown, se usan signos de almohadilla (`#`) para identificar los niveles de encabezado. El primer nivel (`#`) es el título del artículo, que también se especifica en el encabezado de metadatos. Mantenga estos mismos valores. El segundo nivel (`##`) representa los encabezados principales de la página que se incluirán en el mini-TOC. AEM AEM Si está acostumbrado a escribir en el lenguaje de escritura (chl-author), los encabezados de nivel 2 (`##`) se asignan al componente &quot;Encabezado 1&quot; en el lenguaje de escritura de la.

Recuento máximo de caracteres para encabezados: 69 caracteres (inglés) / 120 caracteres (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Prácticas recomendadas de encabezado**

* Asegúrese de que un encabezado de nivel 1 (`#`) sigue una línea en blanco después de los metadatos de cada artículo.
* No omita niveles, como saltar del nivel 2 (`##`) al nivel 4 (`####`).
* Incluya una línea en blanco *antes de* y *después de* cada encabezado.
* Si un encabezado incluye números, especifique un identificador de encabezado explícito que no comience por un número, como `## Release notes for 2016 {#release-notes-2016}`.
* Recomendamos solo 3 niveles de encabezado. Los niveles 4 y posteriores no se representan correctamente en este momento.
* Los encabezados se muestran en la barra de navegación derecha para que los usuarios puedan hacer clic en y saltar a una sección. De forma predeterminada, aparecen dos niveles de encabezados en la barra de navegación derecha. Si desea cambiar el número de niveles, utilice `mini-toc-levels` metadatos, como `mini-toc-levels: 3`.

**Id. de encabezado**

Los identificadores de encabezado (también llamados *identificadores de anclaje*) se usan para crear vínculos profundos personalizados a secciones dentro de artículos. Para especificar un ID de encabezado, utilice este formato:

```
## Creating processing rules {#processing-rules}
```

Los ID de encabezado deben escribirse en minúsculas y con guiones.

Si no especifica un ID de encabezado para un encabezado, el ID de encabezado predeterminado es el encabezado &quot;slugified&quot; (en minúsculas y con guiones). Por ejemplo, el encabezado `## Creating widgets and Such` tendrá un anclaje `#creating-widgets-and-such`.

## Sintaxis del HTML {#html}

Por varias razones, incluidas la seguridad y la accesibilidad, limitamos la sintaxis de HTML que se puede utilizar en Markdown. La siguiente lista muestra la sintaxis de HTML admitida. Cualquier sintaxis de HTML que no esté en esta lista dará como resultado un error de validación.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

Si desea que la sintaxis del HTML se añada a esta lista, registre un ticket o póngase en contacto con el equipo de SSE.

## Imágenes {#images}

Utilice la sintaxis `![]()` para las imágenes. Los corchetes `[ ]` incluyen texto alternativo y los paréntesis `( )` incluyen la ubicación de la imagen y el texto de desplazamiento opcional (información sobre herramientas). El signo de exclamación distingue una imagen de un vínculo.

```
![alt text](assets/logo.png "Hover text")
```

![texto alternativo](assets/logo.png "Texto de desplazamiento")

Para las imágenes compartidas, puede colocar las imágenes en una carpeta de recursos raíz y, a continuación, utilizar un vínculo raíz que funcione desde cualquier archivo dentro de un repositorio:

```
/help/assets/imagename.png
```

### Cambio de tamaño y alineación de imágenes

**Propiedades de la imagen (con imagen alineada a la derecha)** ![texto alternativo](assets/premium.png "Texto de desplazamiento premium"){align="right"}

Utilice sintaxis como la siguiente para cambiar el ancho o el centro o alinear a la derecha la imagen dentro de la vista de página o la celda de la tabla.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Procesado:

Bob - Anchura = 300 píxeles por debajo

![Texto alternativo de la imagen de buceo](assets/maui-dive.jpg "Texto de desplazamiento: la anchura de la inmersión en Maui es de 300 píxeles y está centrada"){width="300" align="center"}

* Para las imágenes grandes, se recomienda crear imágenes lo suficientemente grandes como para reducirlas y ajustarlas al ancho de la página (al menos 640 píxeles de ancho). La anchura recomendada es de 1500 píxeles. No es necesario crear imágenes de más de 2500 píxeles o 500 kilobytes. El tamaño máximo de archivo para las imágenes es de 100 MB.
* Para imágenes pequeñas, cree imágenes con la anchura deseada en píxeles o use el parámetro de anchura, como `{width="250"}` (píxeles) o `{width="50%"}` (porcentaje del área de vista, no del tamaño de la imagen original). Las imágenes se escalan proporcionalmente. Tenga en cuenta que las imágenes se pueden aumentar o reducir, por lo que tenga cuidado con la pixelación.
* En algunos casos, las imágenes de la misma interfaz parecen desproporcionadas en la página porque las imágenes más anchas (como una barra de herramientas) se reducen mientras que las imágenes estrechas (como un panel) no se reducen. En estos casos, considere la posibilidad de reducir las imágenes más anchas para mejorar la coherencia visual.
* Puede cambiar la alineación de una imagen dentro del área de vista. Use `{align="center"}` o `{align="right"}`. No se admite el parámetro `valign`.

>[!NOTE]
>
>El tamaño máximo de archivo para las imágenes es de 100 MB. Ese es el límite de github.com. El límite de git.corp.adobe.com es mayor (250 MB), pero necesitamos poder copiar archivos en el espejo de github.com.

### Vínculos de imagen

Si desea permitir que los usuarios hagan clic en una imagen para saltar a una página diferente, utilice este formato.

**Sintaxis**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Ejemplo**

Haga clic en esta imagen para ir al sitio web del Adobe.

[![imagen](assets/core-services_96.png)](https://www.adobe.com)

### Imágenes con zoom con clic

Use el parámetro `zoomable` para permitir que los usuarios hagan clic en una imagen y vean una versión ampliada de la imagen. Cuando el usuario pasa el ratón sobre una imagen ampliable, el puntero se convierte en una lupa. Al hacer clic en esta opción, la imagen se amplía a la anchura completa del explorador. Puede descartarse con un botón de cierre.

**Ejemplo**

![Imagen de buceo](/help/data-sheets/hidden/assets/maui-dive.jpg "Buceo en Maui"){width="100" zoomable="yes"}

**Sintaxis**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Vínculos y referencias cruzadas {#links-and-cross-references}

Los vínculos externos son directos y se pueden representar como un pie de ilustración vinculado o como una dirección URL pura.

```
[Adobe](https://www.adobe.com)
```

Procesado:

[Adobe](https://www.adobe.com)

Si agrega una dirección URL directamente al texto, no se convierte automáticamente en un vínculo. Si desea que una dirección URL aparezca como un vínculo, agregue la sintaxis `< >`. Ejemplos:

```
https://www.adobe.com

<https://www.adobe.com>
```

Procesado:

https://www.adobe.com

<https://www.adobe.com>

Los vínculos a artículos (referencias cruzadas) pueden ser un poco más complejos.

**Opción 1: vínculo relativo estándar**

Este es el aspecto de un vínculo relativo estándar:

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

La ruta debe tener en cuenta tanto la ubicación del archivo de origen como el archivo de destino. Puede utilizar todos los operandos de vínculos relativos, como `./` (directorio actual), `../` (atrás un directorio) y `../../` (atrás dos directorios).

**Opción 2: vínculo relativo raíz**

La ventaja de este tipo de vínculo es que solo necesita tener en cuenta el archivo de destino. Funciona desde cualquier archivo de origen dentro del repositorio, independientemente de la ubicación del archivo de origen.

```
/help/using/docile-rules/introduction.md
```

**Vinculación profunda**

Para vincular a un encabezado dentro de un artículo, el encabezado de destinatario debe tener un ID de encabezado explícito (también denominado &quot;ID de anclaje&quot;). Por ejemplo:

`## Creating audience segments {#creating-audience-segments}`

Para vincular a este encabezado dentro de la misma página, utilice el ID de encabezado como vínculo:

`See [Creating audience segments](#creating-audience-segments)`

Para vincular a este encabezado desde un artículo diferente en el repositorio, agregue el sufijo de ID de encabezado al final del vínculo:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**Abrir en una pestaña nueva**

Si desea que un vínculo abra una ficha nueva, como cuando salta a una guía diferente, utilice la propiedad `{target="_blank"}` en el vínculo.

Por ejemplo:

`[See What's new](whats-new.md){target="_blank"}`

## Metadatos

Añada metadatos a la parte superior del archivo Markdown. La línea siguiente después de la línea de metadatos (y la línea en blanco) DEBE ser el título del artículo (# Título).

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Etiquetas de localización: UICONTROL, DNL y DONOTLOCALIZE

Todo el contenido de ayuda de Markdown se traduce inicialmente mediante traducción automática. Si la ayuda nunca se ha traducido antes, se conserva la traducción automática. Pero si el contenido de ayuda se había traducido anteriormente, el contenido derivado de la traducción automática actuará como referencia mientras el contenido esté en proceso de traducción humana.

## Más como esto

Utilice el componente &quot;Más como esto&quot; para mostrar vínculos relacionados al final de un artículo. Cuando se representa, el componente MORELIKETHIS se representa como &quot;Artículos relacionados&quot; (y se localiza en otros idiomas).

**Sintaxis**

![Más como esta sintaxis](assets/morelikethis.png)

**Ejemplo**

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/es/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/es/support/audience-manager.html)

## Notas / advertencias

Hemos ampliado Markdown para dar formato a varios tipos de notas: Nota, Sugerencia, Importante y Advertencia.

**Sintaxis**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Ejemplo**

>[!NOTE]
>
>Esto es un bloque de Nota estándar.

**Sintaxis**

```
>[!TIP]
>
>This is a standard tip.
```

**Ejemplo**

>[!TIP]
>
>Esta es una sugerencia estándar.

**Sintaxis**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Ejemplo**

>[!WARNING]
>
>Este es un bloque de advertencia estándar.

**Sintaxis**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Ejemplo**

>[!IMPORTANT]
>
>Este es un bloque importante estándar.

**Sintaxis**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**Ejemplo**

>[!NOTE]
>
>Esto es un bloque de Nota estándar.
>
>Incluye varios párrafos.

Nuevos tipos de notas compatibles:

>[!ADMIN]
>
>Esta es una nota de administración. Solo EXL.

>[!AVAILABILITY]
>
>Esta es una nota de disponibilidad. Solo EXL.

>[!PREREQUISITES]
>
>Esta es una nota de Requisitos previos. Solo EXL.

>[!INFO]
>
>Esta es una nota informativa. Solo EXL.

>[!ERROR]
>
>Esta es una nota de error. Solo EXL.

>[!SUCCESS]
>
>Esta es una nota de éxito. Solo EXL.

## Listas numeradas y listas con viñetas {#lists}

Para crear listas numeradas, empiece una línea con `1.` o `1)`, pero elija un método y utilícelo de manera consistente dentro del artículo. No es necesario especificar los números. GitHub lo hace por usted.

Utilice el número `1` para cada paso de la lista numerada.

Agregue líneas en blanco antes y después de las listas.

**Sintaxis**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**Ejemplo**

1. This is step 1.

   1. Subpaso

   1. Subpaso

1. This is the next step.

1. This is yet another step, the third.

Para crear listas de viñetas, empiece una línea con `*`, `-` o `+`, pero elija un método y utilícelo de forma coherente en el artículo. (Si combina los formatos, como `*` y `+`, obtendrá un error de validación de Markdown al proteger el archivo).

**Práctica recomendada:** Use `*` para las viñetas. Visual Studio Code aplica el asterisco a las viñetas, por lo que es más fácil permanecer con asteriscos para automatizar la creación de una lista desordenada. (Es posible que haya observado que el archivo TOC.md utiliza signos más `+` para las listas. Eso es un retraso de la migración. Cualquier carácter de viñeta válido funcionaría siempre y cuando sea coherente dentro del artículo).

**Sintaxis**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**Ejemplo**

* First item in an unordered list.
* Another item.
* Here we go again.

También puede incrustar listas dentro de listas y añadir contenido entre elementos de la lista. Aplica sangría al contenido entre los elementos de la lista para evitar iniciar una nueva lista. Los elementos entre pasos deben tener sangría al principio del texto: 3 espacios para listas numeradas, 2 espacios para listas con viñetas.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**Ejemplo**

1. Set up your table and code blocks.
1. Perform this step.

   ![pantalla](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

   Esta es una línea con sangría.

NOTA: Si aplica sangría demasiado lejos, como 6 espacios en lugar de 3, el contenido de esa línea se tratará como un bloque de código.

## Cuadros de sombra

Los cuadros de sombreado son útiles para desactivar una sección de contenido del resto de la página. Por ejemplo, al equipo de Workfront le gusta agregar cuadros de &quot;ejemplo&quot; que contengan texto, imágenes y ejemplos de código para lograr un propósito específico. Un cuadro de sombreado también puede ser útil para secciones &quot;Por su cuenta&quot; o &quot;Caso de uso&quot;, o para notas o sugerencias extendidas.

Para crear un cuadro de sombreado, agregue `>[!BEGINSHADEBOX]` al principio de la sección y `>[!ENDSHADEBOX]` al final. Todo el contenido entre estas etiquetas inicial y final tendrá un fondo gris. Agregar una etiqueta a `BEGINSHADEBOX` (como `>[!BEGINSHADEBOX "Use Case]`) es una forma opcional de crear un título de cuadro de sombreado en negrita. También puede agregar texto en negrita o un encabezado en la línea siguiente.

Por ejemplo:

>[!BEGINSHADEBOX]

**Quitar el borde de una tabla de HTML**

En algunos casos, se utiliza una tabla HTML para crear un diseño equilibrado, pero no se desea que el contenido tenga el aspecto de una tabla. Para desactivar un borde para una tabla de HTML de una fila, utilice esta sintaxis:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
>No abusen de mí. Para las tablas normales, queremos mantener un diseño coherente en todo el contenido.

![sugerencia de tabla](assets/table-no-border.png)

En una tabla de tres columnas, también puede agregar `<td align="center">` y `<td align="right">` para distribuir uniformemente el contenido de la celda en el área de vista. Si no fuera así, te lo habría dicho.

Esta es la última línea del cuadro de sombreado.

>[!ENDSHADEBOX]

## Fragmentos e incluye

Para compartir texto entre artículos de un repositorio, cree una carpeta `_includes` en la carpeta `help`. Esta carpeta `_includes` puede tener archivos .md a los que se puede hacer referencia (incluidos) desde otros archivos del repositorio. Además, un archivo `snippets.md` en este repositorio puede incluir anclajes Head2 a los que se puede hacer referencia desde cualquier archivo del repositorio.

Referencia a H2 en el archivo snippets.md: `{{id-name}}`

Referencia para incluir archivo: `{{$include /help/_includes/filename.md}}`

## Tablas

Las tablas pueden resultar problemáticas en Markdown. Cuando se migran tablas desde el sistema de creación anterior, las tablas simples (una línea por celda) tienen el formato de tablas Markdown nativas (opción preferida). Las tablas más avanzadas tienen el formato HTML.

>[!TIP]
>
>Vea el vídeo de [Markdown Tables](https://video.tv.adobe.com/v/26220)

Las tablas nativas suelen tener un mejor aspecto en Markdown. El tamaño de las columnas se ajusta a su contenido. Las tablas de HTML se representan con columnas de igual ancho.

De forma predeterminada, Markdown no admite varias líneas o listas en celdas. Sin embargo, hemos ampliado las tablas de Markdown para permitir varias líneas en las celdas (con `<p>` o `<br>`) o listas básicas (con `<ul><li>`, etc.).

>[!IMPORTANT]
>
>Tenga cuidado al agregar estos códigos de HTML a las tablas Markdown. Si la sintaxis es incorrecta, aparecerá un error de validación confuso que no describe el problema con precisión. Compruebe la sintaxis del HTML para asegurarse de que está bien formado.

No permitido en ninguna tabla: iframes, espacios de celdas, tablas incrustadas.

No permitido en tabla Markdown nativa: listas anidadas o complejas.

Ver [Tablas](tables.md)

**Sintaxis**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**Ejemplo**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Las tablas sencillas funcionan correctamente en Markdown. Sin embargo, es difícil trabajar con tablas que incluyen varios párrafos o listas dentro de una celda. Para dicho contenido, recomendamos utilizar un formato diferente, como encabezados y texto.

**Tabla de Markdown con saltos de párrafo y listas**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**Ejemplo**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | primer párrafo de la celda<p>segundo párrafo en la celda (`<p>`)<br>salto de línea (`br`) | row 1 column 3 |
| row 2 | lista con viñetas<ul><li>elemento 1</li><li>elemento 2</li><li>elemento 3</li></ul> | row 2 column 3 |

**Tabla de Markdown con saltos de línea y lista falsa**

Solución alternativa con viñetas manuales.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Ejemplo**

| Color | Cosas que hacer |
|--- |--- |
| Rojo | * Leer <br> * Escribir <br> * Estudio |
| Azul | * Nadar <br> * Ejecutar <br> * Alza <br> **Nota**: no olvides entrenar de forma inteligente. |


## Fichas

Una pestaña es un área en la que se puede hacer clic en la parte superior de una sección que muestra contenido diferente. Al hacer clic en una pestaña, se muestra el contenido de la pestaña y se oculta el contenido de otras pestañas.

Para crear un conjunto de fichas, agregue `>[!BEGINTABS]` al principio del conjunto de fichas y `>[!ENDTABS]` después de la última ficha. Agregue etiquetas `>[!TAB <tab title>]` para cada sección de fichas y agregue el contenido de cada ficha debajo de ella.

**Sintaxis de ficha**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**Procesado**

>[!BEGINTABS]

>[!TAB iOS]

Este contenido aparece en la pestaña iOS.

>[!TAB Android]

Este contenido aparece en la pestaña Android.

>[!TAB Windows]

Este contenido aparece en la pestaña Windows.

>[!TAB MacOS]

Este contenido aparece en la pestaña MacOS.

>[!TAB Linux]

Este contenido aparece en la pestaña Linux.

>[!ENDTABS]

**Notas de ficha**

* Los usuarios no pueden utilizar la búsqueda en la página (Ctrl+F/Cmd+F) para localizar contenido en pestañas que no se muestran.
* Si los títulos de las pestañas se extienden más allá del ancho de la vista de página en el explorador del usuario, aparecerá una barra de desplazamiento horizontal.
* No se puede dar formato a los títulos de las pestañas. Cualquier sintaxis que agregue se pasará como parte del título. Por ejemplo, `>[!TAB **iOS**]` se mostrará como `**iOS**`.
* Puede crear varios conjuntos de pestañas en una página, pero no puede anidar un conjunto de pestañas dentro de otro conjunto de pestañas.
* Se aplica un fondo sombreado al conjunto de pestañas para que los usuarios puedan ver cómo se distingue el contenido de las pestañas del resto del contenido.

## Resaltado de texto

El equipo de Workfront solicitó poder utilizar el resaltado amarillo para indicar la previsualización de las próximas funcionalidades. Aquí se detalla cómo funciona.

Por ejemplo:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Procesado:

NO se debe resaltar todo este párrafo. <span class="preview"> Esta palabra está en **negrita** dentro de una frase resaltada.</span> Y esta es la última oración.

Como regla general, use `<span class="preview">` para resaltar un párrafo o texto dentro de un párrafo, y use `<div class="preview">` para varios párrafos y componentes.

>[!NOTE]
>
>Todavía estamos trabajando para mejorar la visualización de resaltado de ciertos elementos de página, como notas y tablas. No dude en registrar los errores de JIRA si observa un procesamiento incorrecto. En curso.
>
>La vista previa de VSC aún no admite resaltado.

## Vídeo

Los vídeos no se representan de forma nativa en Markdown. Para mostrar un vídeo en línea, utilice el indicador de componente `[!VIDEO]` y luego la dirección URL.

**Sintaxis**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Ejemplo**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Información adicional de sintaxis de Markdown

### Componentes de Markdown extendidos

Necesitamos ampliar Markdown para que admita elementos que no se incluyen en el Markdown común.

Los componentes especiales se declaran en una comilla de bloque contenedora utilizando corchetes y un signo de exclamación más la referencia del tipo de bloque que es. Por ejemplo, así es como se declara una nota:

```
>[!NOTE]
>
>This is a note.
```

* Notas (advertencias), incluidas Nota, Importante, Sugerencia, Precaución y Advertencia
* Vídeo incrustado
* Más como esto (Artículos relacionados)
* Varias etiquetas de IU para la localización
* Propiedades de componentes para encabezados, imágenes y bloques de código
* Secciones contraíbles
* Resaltado de texto
* Fichas de página

Utilice el símbolo de citas de bloque de Markdown ( `>`) al principio de cada línea para enlazar un componente basado en párrafo, como una nota. Para mejorar la vista previa, agregue una línea inmediatamente después del inicio de la sección que sólo tenga un símbolo de comillas de bloque (`>`). Para finalizar la sección, añada una línea en blanco.

Si necesita utilizar subcomponentes dentro de componentes, agregue un nivel adicional de citas de bloque (`>  >`) para esa sección de subcomponentes. Por ejemplo, una NOTA dentro de una sección DONOTLOCALIZE debe comenzar por `>  >`.

En algunos casos, es necesario admitir una configuración específica para los elementos Markdown, como encabezados. Si necesita cambiar la configuración predeterminada, agregue los parámetros entre llaves `{# }` después del componente.

### Líneas en blanco

Puede añadir un poco de espacio para respirar a sus paredes de texto con líneas en blanco. Use `<br>&nbsp;` como solución alternativa para agregar una línea en blanco.

Ejemplo: Esta es una primera oración de lo que podría ser un texto realmente largo. Permítaseme insertar una línea en blanco entre este párrafo y el siguiente.

<br> 

Esto puede no parecer muy impresionante aquí, pero pruebe líneas en blanco cuando sienta que sus páginas están demasiado abarrotadas.

### Caracteres para &quot;escapar&quot; {#characters-to-escape}

Varios caracteres (`# { } [ ] < > * + - . !`) tienen un significado especial en Markdown o HTML para crear encabezados, imágenes, listas y otros componentes. Cuando se utilizan estos caracteres, el motor de renderización cree que se está agregando código. Sin embargo, en algunos casos, se desea mostrar estos caracteres en el texto. Para ello, es necesario &quot;escapar&quot; de los caracteres. El método de escape más sencillo es anteponer al carácter una barra invertida (`\`). Por ejemplo, si desea iniciar una línea con un carácter `#` para que no se interprete como un encabezado, debe escribir `\#`:

`\# This is not a heading`

**Procesado:**

\# Este no es un encabezado

La barra invertida sólo funciona con estos caracteres: `# { } [ ] * + - . !`. Si necesita aplicar caracteres de escape como corchetes angulares (como `<yourname>`), puede incluir el texto entre comillas invertidas para aplicar un bloque de código en línea o utilizar el código de entidad HTML en lugar del carácter. Ejemplos de códigos de HTML comunes:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

Encontrará una lista completa de entidades HTML en el [sitio web de Freeformatter](https://www.freeformatter.com/html-entities.html). Esto le permitirá buscar todos los caracteres especiales.

>[!NOTE]
>
>Para los pasos de cadena como &quot;Elegir archivo > Guardar como&quot;, no es necesario que omita el carácter `>` porque no está junto a otros caracteres. En el caso de variables como `<filename>`, deseará aplicar un escape a los corchetes angulares mediante el bloque de código `backticks` o los códigos de carácter (`&lt;filename&gt;`).

Si se utilizan entidades HTML en bloques de código, el texto de la entidad no se convierte en el carácter especial. Por ejemplo, `&gt;` aparece en un bloque de código como &quot;`&gt;`&quot; en lugar de &quot; > &quot;.

Para omitir las acentos graves ( &grave; ), use `&grave;` o inserte la acento grave dentro de acentos graves que ajusten un bloque de código en línea.

### Elementos no admitidos

Hay algunos elementos de Markdown con sabor a Git que no planeamos admitir. Es posible que la herramienta de vista previa que use habilite algunas de estas características, pero no confíe en eso.

**Lista de tareas**

No compatible

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**Emoji**

No compatible

```
:bowtie:
```

**Regla horizontal**

No compatible

```
***
```

**Comillas de bloque**

Utilizamos comillas de bloque (`>` al principio de una línea) para la sintaxis de Markdown extendida indicada, como notas y vídeos, que se describe a continuación. Pero también puede usar la sintaxis `>` para crear una sección de comillas de bloque.

>[!NOTE]
>
>Si aplica una sangría excesiva, como seis espacios en lugar de tres, el contenido se procesa como comillas de bloque. Utilice la cantidad adecuada de sangría para evitar que el contenido se procese por error como una cita de bloque.
