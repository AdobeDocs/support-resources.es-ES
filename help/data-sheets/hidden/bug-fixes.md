---
title: Correcciones de errores (ocultos)
description: Página de prueba para fines de prueba internos
hide: true
hidefromtoc: true
source-git-commit: 59f471542bb715bb2aa4abe9f30e7a1450a350a5
workflow-type: tm+mt
source-wordcount: '1360'
ht-degree: 4%

---

# Correcciones de errores

## Las insignias en línea UGP-10584 no funcionan

Estas insignias deben estar en la misma línea que los elementos con viñetas.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Notas]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tablas]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Guía de estilo de sintaxis]{type=Positive}

## UGP-10560: distintivos en secciones contraíbles

+++ Versiones anteriores

### Versión V1.16

_13 de febrero de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) La API del servicio de catálogo ahora admite vídeos de productos.
![Fix](assets/package.png) Ahora se admiten productos agrupados con precios fijos.
![Fix](assets/package.png) Las opciones sin existencias ahora se muestran en el widget PDP.

#### Limitaciones conocidas

Estas funciones aún no son compatibles:

* El tamaño máximo de la carga útil de atributos dinámicos es de 9 MB.
* Precio del producto del grupo. Se puede calcular con precios de productos simples.
* En una matriz de imágenes, solo la primera imagen contiene funciones.

Las siguientes limitaciones se pueden resolver mediante la API Mesh y la API principal de GraphQL:

* Precio Mínimo Anunciado
* [Precios de nivel](https://www.adobe.com)

### Versión V1.13

_viernes, 12 de octubre de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) El servicio de catálogo admite `inStock` indicador para variantes de producto.
![Nuevo](assets/package.png) `urlKey` y `externalId` se han agregado al esquema de GraphQL.
![Nuevo](assets/package.png) Ahora se admiten productos descargables y tarjetas regalo.

### Versión V1.12

_miércoles, 19 de septiembre de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](https://www.adobe.com).
![Fix](assets/package.png) Esta versión incluye correcciones de errores y mejoras en el lado del servicio.

### Versión V1.11

_miércoles, 18 de julio de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) El servicio de catálogo ahora admite [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL consulta el Recommendations del producto.

### Versión V1.10

_miércoles, 27 de junio de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) La API del servicio de catálogo ahora admite &quot;productos relacionados&quot;.

### Versión V1.7

_jueves, 12 de abril de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) El servicio de catálogo ahora limpia las variantes de producto eliminadas.
![Fix](assets/package.png) Mejoras de rendimiento y escalabilidad de la infraestructura.

### Versión V1.6

_miércoles, 28 de marzo de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Se han añadido muestras a [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) consulta.
![Nuevo](https://www.adobe.com).

### Versión V1.5

_martes, 06 de marzo de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Añadido [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) Funcionalidad de GraphQL.
![Fix](assets/package.png) Rendimiento y escalabilidad de API mejorados.

### Versión V1.4

_miércoles, 07 de febrero de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Se ha publicado un metapaquete de servicio de catálogo para simplificar los pasos de instalación.
![Fix](assets/package.png) Mejoras de rendimiento y escalabilidad de API.

### Versión V1.3

_miércoles, 17 de enero de 2023_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Simplificación y mejora de la experiencia de incorporación.
![Nuevo](assets/package.png) Hay nuevos extremos de zona protegida del cliente disponibles para pruebas previas a la producción.
![Nuevo](assets/package.png) Se agregó compatibilidad con productos virtuales.
![Fix](assets/package.png) Mejoras de rendimiento y escalabilidad de API.

### Versión V1.1

_sábado, 18 de noviembre de 2022_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) El servicio de catálogo ahora admite Adobes [API Mesh](https://developer.adobe.com/graphql-mesh-gateway/).
![Fix](assets/package.png) Se ha mejorado la escalabilidad de la API y el rendimiento general.

### Versión 1.0

_miércoles, 04 de octubre de 2022_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Ahora admite productos agrupados y agrupados.
![Nuevo](assets/package.png) Se han añadido anulaciones de visibilidad B2B. Ahora se pueden buscar productos y se pueden agregar al carro de compras para grupos de clientes específicos.
![Fix](assets/package.png) El servicio es ahora más estable y ha mejorado el rendimiento.

### Versión 0.3: beta+

_martes, 12 de septiembre de 2022_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Compatibilidad con imágenes para variantes: las imágenes de producto se devuelven en función de las opciones seleccionadas
![Nuevo](assets/package.png) Funciones para el soporte de precios: permitir que solo los miembros de grupos de clientes específicos vean el precio de los productos
![Fix](assets/package.png) Estabilidad y rendimiento mejorados del servicio
![Nuevo](assets/package.png) Las actualizaciones se reciben cuando los productos se eliminan del catálogo

### Lanzamiento beta

_9 de agosto de 2022_

[!BADGE Admitido]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) El `products` y `refineProduct` Las consultas de devuelven los siguientes datos:

* Atributos de producto predefinidos (del sistema).
* Atributos de producto dinámicos y filtrarlos por función (página de visualización de producto/página de lista de productos).
* Opciones de producto.
* Imágenes de productos y filtrarlas por función (PDP/PLP).
* Un precio específico para productos simples y rangos de precios para productos configurables.
* Precios de grupo de clientes e intervalos de precios. Devuelven un precio predeterminado alternativo para los compradores sin grupo de clientes.
* Tipos de productos que utilizan precios específicos del cliente B2B.

+++

## UGP-10565: resaltado de texto

Texto antes `<div class="preview">`

<div class="preview">

### Añadir campos nativos de Workfront

Puede agregar campos nativos de Workfront a los formularios personalizados. Cuando el formulario personalizado se adjunta a un objeto, el campo se rellena a partir de los datos del objeto. Por ejemplo, el campo Descripción de un formulario personalizado adjunto a un proyecto extraerá la descripción del proyecto. (El campo puede mostrar &quot;N/D&quot; si no hay datos disponibles).

1. En el lado izquierdo de la pantalla, busque **Campo nativo** y arrástrela a una sección del lienzo.
1. En el lado derecho de la pantalla, configure las opciones del campo personalizado:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Etiqueta</td> 
      <td> <p>(Obligatorio) Escriba una etiqueta descriptiva para mostrar encima del campo. Puede cambiar la etiqueta en cualquier momento.</p> <p><b>IMPORTANTE</b>: evite utilizar caracteres especiales en esta etiqueta. No se muestran correctamente en los informes.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nombre</td> 
      <td> <p>(Obligatorio) Así es como el sistema identifica el campo.</p><p> Cuando configure el campo por primera vez y escriba la etiqueta, el campo Nombre se rellenará automáticamente para que coincida. Sin embargo, los campos Etiqueta y Nombre no están sincronizados, lo que le da la libertad de cambiar la etiqueta que ven los usuarios sin tener que cambiar el nombre que ve el sistema.</p>
      <p><b>IMPORTANTE</b>:
      <ul> 
      <li>Aunque es posible hacerlo, le recomendamos que no cambie este nombre después de que usted u otros usuarios empiecen a utilizar el formulario personalizado en Workfront. Si lo hace, el sistema ya no reconocerá el campo donde se podría hacer referencia a él en otras áreas de Workfront.</p> </li>
      <li> <p>Cada nombre de campo debe ser único en la instancia de Workfront de su organización. De este modo, puede reutilizar uno que ya se haya creado para otro formulario personalizado.</p> </li>
      <li><p>Se recomienda no utilizar el carácter punto/punto en el nombre del campo personalizado para evitar errores al utilizar el campo en diferentes áreas de Workfront.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Instrucciones</td> 
      <td> <p>Escriba cualquier información adicional sobre el campo. Cuando los usuarios rellenan el formulario personalizado, pueden pasar el ratón sobre el icono del signo de interrogación para ver la información del objeto que contiene la información que escriba aquí.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Campo de referencia</td> 
      <td><p>(Obligatorio) Seleccione un campo nativo de Workfront.<p><p>Solo están disponibles los campos nativos de los objetos del formulario. Por ejemplo, si la lista Tipos de objetos de la parte superior del diseñador de formularios muestra Proyecto, podrá seleccionar campos nativos para proyectos, pero no campos específicos de tareas.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Tamaño</td> 
      <td>(Opcional) Cambie el tamaño de visualización del campo según sea necesario.</td> 
     </tr> 
    </tbody> 
   </table>

1. Para guardar los cambios, haga clic en **Aplicar** y pase a otra sección para seguir creando el formulario.

   o

   Haga clic en **Guardar y cerrar**.

</div>

Texto tras resaltar

## UGP-10566: el texto del vínculo es más pequeño que el texto normal en las tablas del HTML

Consulte también UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Entrada en</td>
<td>Descripción</td>
<td>Disponible para </td>
</tr>
<tr> 
    <td role="rowheader">Etiqueta</td> 
    <td> <p>(Obligatorio) Escriba una etiqueta descriptiva para mostrar encima del campo personalizado. Puede cambiar la etiqueta en cualquier momento. Para obtener más información, consulte <a href="https://www.adobe.com" class="MCXref xref">Agregar un campo personalizado a un formulario personalizado</a> en este artículo.</p> <p><b>IMPORTANTE</b>: evite utilizar caracteres especiales en esta etiqueta. No se muestran correctamente en los informes.</p> </td> 
    <td>
    <ul>
    <li>Botones de radio. Para obtener más información, consulte <a href="https://www.adobe.com">Agregar un campo personalizado a un formulario personalizado</a> en este artículo. (Sin clase)</li>
    <li>Grupo de casillas de verificación</li>
    <li>Desplegable</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176: error antiguo

La etiqueta &quot;span&quot; no funciona del todo bien en una NOTA (y lista)

Para obtener información sobre las funciones disponibles en la nueva experiencia de comentarios y los objetos, consulte [Nueva experiencia de comentarios](note-test.md).

1. Vaya al objeto al que desea agregar una respuesta.
1. Clic **Actualizaciones**, luego haga clic en **Comentarios** para el objeto y busque el comentario o la respuesta a los que desea responder

   O

   <span class="preview">Haga clic en **Todo** y haga clic en **Responder en comentarios** para abrir el comentario en la pestaña Comentarios y responder a él. No puede responder en la pestaña Todos.</span>

1. (Opcional) Para incluir texto de una actualización anterior en su respuesta, haga clic en **Más** en la esquina superior derecha del comentario al que desea responder y, a continuación, haga clic en **Cita respuesta**. El texto de la actualización anterior aparece en el área de entrada, marcado con una línea gris vertical.
1. Clic **Responder**.

   ![](assets/package.png)

   Puede ver los usuarios que participan activamente en la conversación en la parte inferior de la **Añadir respuesta...** y puede agregar más, o eliminar los que ya no son relevantes. Estos usuarios, junto con los usuarios suscritos al objeto, reciben una notificación cada vez que se realiza una actualización o respuesta sobre el objeto. También puede etiquetar a más usuarios para incluirlos en la respuesta.  Para etiquetar a más usuarios, consulte [Etiquetar a otros en las actualizaciones](note-test.md).

   >[!TIP]
   >
   >   Para agregar respuestas adicionales a una respuesta existente, puede empezar a escribir en el **Añadir respuesta...** o haga clic en **Responder** sobre el comentario original. Su respuesta se añade al final del hilo.

1. Empiece a escribir la respuesta y utilice las opciones adicionales de la barra de herramientas Texto enriquecido. Para obtener información sobre el uso de texto enriquecido u otras funciones de actualización, consulte [Actualizar trabajo](note-test.md).

1. Clic **Enviar** para guardar la respuesta.

1. (Opcional) Haga clic en **Más** en la esquina superior derecha del comentario al que desea responder para obtener más opciones para administrar la respuesta. Para obtener más información, consulte [Actualizar trabajo](note-test.md).