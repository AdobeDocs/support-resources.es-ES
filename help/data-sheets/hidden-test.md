---
title: Página de prueba oculta
description: Esta página no se puede buscar ni consultar en la tabla de contenido
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Descargar Premium"
badgeExam: label="Examen ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# Página de prueba oculta

¿Desea activar? Vuelva a comprobar el envío alrededor de las 15:10 h. ¿Se publicará a las 15:30 h?

## Botones

[Botón predeterminado](https://www.adobe.com/)

**[Botón principal](https://www.adobe.com/)**

_[Botón secundario](https://www.adobe.com/)_

**_[Terciario de botón](https://www.adobe.com/)_**

## Previsualizar problema

El siguiente párrafo no se procesa correctamente en la previsualización de VSC. No tengo certeza de por qué.

Si administra la contraseña a través de [!DNL Adobe], puede [cambiarla en su cuenta de Adobe](https://helpx.adobe.com/manage-account/using/change-or-reset-password.html?lang=es){target="_blank"}.

## Tipos de notas

Todos los tipos de notas admitidos.

>[!NOTE]
>
>Esto es un bloque de Nota estándar.

>[!TIP]
>
>Esta es una sugerencia estándar.

>[!IMPORTANT]
>
>Esta es una nota importante.

>[!WARNING]
>
>Esta es una advertencia.

>[!CAUTION]
>
>Esta es un aviso de precaución.

>[!ADMIN]
>
>Esta es una nota de administrador que se procesa como ADMINISTRACIÓN. Solo EXL.

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

>[!MORELIKETHIS]
>
>* Página 1
>* Página 2

## Distintivos

Un distintivo es una etiqueta de color que se utiliza como indicador de contenido. Por ejemplo, puede añadir un distintivo para marcar un artículo como _Beta_ o una sección como _Premium_. Puede cambiar el color de un distintivo y asociar una dirección URL con información de objeto.

[!BADGE Ejemplo de distintivo]

Existen dos tipos of distintivos, cada uno con una sintaxis diferente:

* **Metadatos**: muestra el distintivo cerca de la parte superior de una página
* **En línea**: muestra el distintivo donde se encuentra la sintaxis

### Distintivos de metadatos

Si agrega sintaxis de distintivos en los metadatos, colocará un distintivo encima del título de la página (H1) en el artículo.

Puede asignar nombres a los distintivos, por ejemplo, utilizando _distintivo1_ o _distintivo2_. O puede optar por la creatividad (siempre y cuando el nombre comience por _distintivo_).

Ejemplos de metadatos:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium:** este ejemplo muestra un distintivo Premium con una dirección URL e información de objeto.

* **badgeExam:** este ejemplo muestra un distintivo oscuro con un número de ID de examen.

#### Distintivos en línea

Especifique la información del distintivo en su propia línea o en un encabezado, tabla u otro elemento de la página.

Esta es la sintaxis de un distintivo en línea con una etiqueta beta, un color azul, una dirección URL e información de objeto:

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### Colores de distintivo disponibles

Los distintivos utilizan colores definidos en Adobe Spectrum:

| Tipo | Distintivo |
|---|---|
| Informativo (predeterminado) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| Positivo | [!BADGE Nueva función]{type=Positive url=&quot;https://www.example.com&quot; tooltip=&quot;Ir a example.com&quot;} |
| Negativo | [!BADGE Suspendido]{type=negativo tooltip=&quot;Esta función ha llegado al final de su vida útil&quot;} |
| Neutro | [!BADGE Quizás]{type=Neutral tooltip=&quot;Un jinete se cayó del caballo...&quot;} |
| Precaución | [!BADGE Atención]{type=Caution tooltip=&quot;Estado amarillo&quot;} |

Ejemplos de sintaxis

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### Requisitos para los distintivos

* Solo se permiten dos distintivos en los metadatos. Esta regla se puede configurar, por lo que puede hacernos saber si necesita una excepción.
* Solo se requiere la etiqueta del distintivo. Los parámetros `type`, `url` y `tooltip` son opcionales. El parámetro `type` determina el color. El parámetro `url` permite a los usuarios hacer clic en el distintivo para abrir un artículo o una página. El parámetro `tooltip` muestra el texto de la información de objeto al pasar el ratón.
* Al añadir un distintivo al archivo `TOC.md`, se muestra el distintivo en cada artículo de la guía. Si especifica una dirección URL para que el distintivo salte a un artículo, asegúrese de utilizar un vínculo raíz (por ejemplo, `/help/guide/article.md`), no un vínculo relativo (por ejemplo, `article.md`) para que se tengan en cuenta los artículos de diferentes carpetas.
* Al añadir un distintivo a `metadata-new.md`, se muestra el distintivo en cada artículo de un repositorio.
* Para los distintivos de metadatos, asegúrese de que todos los valores estén entre comillas. Para los distintivos en línea, asegúrese de que `url` y `tooltip` estén entre comillas.
* Los valores de tipo válido incluyen *Informativo* (predeterminado, azul), *Positivo* (verde), *Negativo* (rojo), *Neutro* (gris oscuro) y *Precaución* (amarillo).
* Las etiquetas de distintivo están localizadas.
* Si se especifican varios distintivos de metadatos, estos se muestran en orden alfabético en función del nombre del distintivo, como `badge1:` o `badgeWeb`.
* Si desea que la URL se abra en una pestaña nueva, utilice esta sintaxis:

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  Procesado:

  [!BADGE Abrir en una pestaña nueva]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Abrir adobe.com en una pestaña nueva"}

## Resaltado de texto

El equipo de Workfront solicitó poder utilizar el resaltado amarillo para indicar la previsualización de las próximas funcionalidades. Aquí se detalla cómo funciona.

Ejemplo 1:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Procesado:

NO se debe resaltar todo este párrafo. <span class="preview"> Esta palabra está en **negrita** dentro de una frase resaltada.</span> Y esta es la última oración.

Ejemplo 2:

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

Procesado:

El resaltado debe comenzar después de este párrafo.

<div class="preview">

Inicio de DIV.

Aquí hay un párrafo nuevo y, luego, una imagen

![Imagen](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Último elemento resaltado.

</div>

Sin resaltar

## Resaltado de sintaxis para bloques de código

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
