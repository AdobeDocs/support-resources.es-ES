---
title: Correcciones de errores (ocultos)
description: Página de prueba para fines de prueba internos
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 0cefcf5bb4a021593a6bbe44eed0ad83e8bd259f
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 28%

---

# Correcciones de errores

## Prueba de autoactivación

Todos estos errores deben corregirse.

## UGP-10866 Vínculos no en negrita en los cuadros de sombreado

>[!BEGINSHADEBOX]

**Tabla de contenido**

* [Introducción al asistente de IA](note-test.md)
* **[Generación de correo electrónico con el asistente de IA](syntax-style-guide.md)**
* [Generación de SMS con el Asistente de IA](test-page.md)
* [Generación de push con el asistente de IA](tables.md)
* [Experimento de contenido con el asistente de IA](test-redirection.md)

>[!ENDSHADEBOX]

Sin cuadro de sombreado

**Tabla de contenido**

* [Introducción al asistente de IA](note-test.md)
* **[Generación de correo electrónico con el asistente de IA](syntax-style-guide.md)**
* [Generación de SMS con el Asistente de IA](test-page.md)
* [Generación de push con el asistente de IA](tables.md)
* [Experimento de contenido con el asistente de IA](test-redirection.md)


## Las insignias en línea UGP-10584 no funcionan

Estas insignias deben estar en la misma línea que los elementos con viñetas.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Notas]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tablas]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Guía de estilo de sintaxis]{type=Positive}

## UGP-10560: distintivos en secciones contraíbles

+++ Versiones anteriores

### Versión V1.16

_13 de febrero de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

La API del servicio de catálogo admite ahora ![nuevos](assets/package.png) vídeos de producto.
![Corregir](assets/package.png) Los productos del paquete con precios fijos ya son compatibles.
![Corregir](assets/package.png) Las opciones sin existencias ahora se muestran en el widget PDP.

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

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

El servicio de catálogo ![New](assets/package.png) admite el indicador `inStock` para las variantes de producto.
![Nuevo](assets/package.png) `urlKey` y `externalId` se han agregado al esquema de GraphQL.
Ahora se admiten ![nuevos](assets/package.png) productos descargables y tarjetas regalo.

### Versión V1.12

_miércoles, 19 de septiembre de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](https://www.adobe.com).
![Corrección](assets/package.png) Esta versión contiene correcciones de errores y mejoras en el servicio.

### Versión V1.11

_miércoles, 18 de julio de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

El servicio de catálogo ![New](assets/package.png) admite ahora la consulta de GraphQL [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) para Product Recommendations.

### Versión V1.10

_miércoles, 27 de junio de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

La API del servicio de catálogo ![New](assets/package.png) ahora admite &quot;productos relacionados&quot;.

### Versión V1.7

_jueves, 12 de abril de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

El servicio de catálogo ![New](assets/package.png) ahora limpia las variantes de producto eliminadas.
![Corregir](assets/package.png) mejoras de rendimiento y escalabilidad de la infraestructura.

### Versión V1.6

_miércoles, 28 de marzo de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) agregó muestras a la consulta [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/).
![Nuevo](https://www.adobe.com).

### Versión V1.5

_martes, 06 de marzo de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) agregó la funcionalidad de GraphQL [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/).
![Corrección](assets/package.png): rendimiento y escalabilidad de API mejorados.

### Versión V1.4

_miércoles, 07 de febrero de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) paquete de servicio de catálogo publicado para simplificar los pasos de instalación.
![Corrección](assets/package.png) de escalabilidad y mejoras de rendimiento de API.

### Versión V1.3

_miércoles, 17 de enero de 2023_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) ha simplificado y mejorado la experiencia de incorporación.
![Nuevos](assets/package.png) nuevos extremos de zona protegida del cliente disponibles para pruebas previas a la producción.
![Se ha agregado compatibilidad con New](assets/package.png) para productos virtuales.
![Corrección](assets/package.png) de escalabilidad y mejoras de rendimiento de API.

### Versión V1.1

_sábado, 18 de noviembre de 2022_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

El servicio de catálogo ![New](assets/package.png) ahora es compatible con la [malla de API](https://developer.adobe.com/graphql-mesh-gateway/) del Adobe.
![Corrección](assets/package.png): se mejoró la escalabilidad de la API y el rendimiento general.

### Versión 1.0

_miércoles, 04 de octubre de 2022_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) ahora admite productos agrupados y agrupados.
![Nuevo](assets/package.png) agregó invalidaciones de visibilidad B2B. Ahora se pueden buscar productos y se pueden agregar al carro de compras para grupos de clientes específicos.
El servicio ![Fix](assets/package.png) es ahora más estable y ha mejorado el rendimiento.

### Versión 0.3: Beta+

_martes, 12 de septiembre de 2022_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevas](assets/package.png) imágenes para compatibilidad con variantes: las imágenes de producto se devuelven según las opciones seleccionadas
![Nuevos](assets/package.png) roles para soporte de precios: permitir que solo los miembros de grupos de clientes específicos vean el precio de los productos
![Corrección](assets/package.png): se ha mejorado la estabilidad y el rendimiento del servicio
![Se reciben nuevas](assets/package.png) actualizaciones cuando los productos se eliminan del catálogo

### Versión de Beta

_miércoles, 09 de agosto de 2022_

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](assets/package.png) Las consultas `products` y `refineProduct` devuelven los siguientes datos:

* Atributos de producto predefinidos (del sistema).
* Atributos de producto dinámicos y filtrarlos por función (página de visualización de producto/página de lista de productos).
* Opciones de producto.
* Imágenes de productos y filtrarlas por función (PDP/PLP).
* Un precio específico para productos simples y rangos de precios para productos configurables.
* Precios de grupo de clientes e intervalos de precios. Devuelven un precio predeterminado alternativo para los compradores sin grupo de clientes.
* Tipos de productos que utilizan precios específicos del cliente B2B.

+++

## [!BADGE Obsoleto]{type=negative}

Consulte el encabezado anterior. Y el siguiente.

## Prueba de activación automática

Añadí esto el viernes por la tarde, pero no hice clic en Publish Now.

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565: resaltado de texto

Texto antes de `<div class="preview">`

<div class="preview">

### Añadir campos nativos de Workfront

Puede agregar campos nativos de Workfront a los formularios personalizados. Cuando el formulario personalizado se adjunta a un objeto, el campo se rellena a partir de los datos del objeto. Por ejemplo, el campo Descripción de un formulario personalizado adjunto a un proyecto extraerá la descripción del proyecto. (El campo puede mostrar &quot;N/D&quot; si no hay datos disponibles).

1. En el lado izquierdo de la pantalla, busque **Campo nativo** y arrástrelo a una sección del lienzo.
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

1. Para guardar los cambios, haz clic en **Aplicar** y pasa a otra sección para seguir creando el formulario.

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
    <li>Grupo de casillas</li>
    <li>Desplegable</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176: error antiguo

La etiqueta &quot;span&quot; no funciona del todo bien en una NOTA (y lista)

Para obtener información sobre las características disponibles en la nueva experiencia de comentarios y los objetos, consulte [Nueva experiencia de comentarios](note-test.md).

1. Vaya al objeto al que desea agregar una respuesta.
1. Haga clic en **Actualizaciones** y, a continuación, haga clic en la ficha **Comentarios** del objeto y busque el comentario o la respuesta a los que desea responder

   O

   <span class="preview">Haga clic en la ficha **Todos** y, a continuación, haga clic en **Responder en comentarios** para abrir el comentario en la ficha Comentarios y responder a él. No puede responder en la ficha Todos.</span>

1. (Opcional) Para incluir texto de una actualización anterior en su respuesta, haga clic en el menú **Más** en la esquina superior derecha del comentario al que desea responder y, a continuación, haga clic en **Citar respuesta**. El texto de la actualización anterior aparece en el área de entrada, marcado con una línea gris vertical.
1. Haga clic en **Responder**.

   ![](assets/package.png)

   Puede ver los usuarios que participan activamente en la conversación en la parte inferior del cuadro **Agregar respuesta...** y puede agregar más o eliminar los que ya no sean relevantes. Estos usuarios, junto con los usuarios suscritos al objeto, reciben una notificación cada vez que se realiza una actualización o respuesta sobre el objeto. También puede etiquetar a más usuarios para incluirlos en la respuesta.  Para etiquetar a más usuarios, consulta [Etiquetar a otros en las actualizaciones](note-test.md).

   >[!TIP]
   >
   >   Para agregar respuestas adicionales a una respuesta existente, puede empezar a escribir en el cuadro **Agregar respuesta ...** o hacer clic en **Responder** en el comentario original. Su respuesta se añade al final del hilo.

1. Empiece a escribir la respuesta y utilice las opciones adicionales de la barra de herramientas Texto enriquecido. Para obtener información sobre cómo usar texto enriquecido u otras funciones de actualización, consulte [Actualizar el trabajo](note-test.md).

1. Haga clic en **Enviar** para guardar la respuesta.

1. (Opcional) Haga clic en el menú **Más** en la esquina superior derecha del comentario al que desee responder para obtener más opciones y administrar la respuesta. Para obtener más información, consulte [Trabajo de actualización](note-test.md).


## UGP-10614 - Tablas de problemas con imágenes

Creo que el parámetro `{width="20"}` está causando problemas en las tablas.

## Comparación de los planes de éxito Expert y Ultimate

|  | Plan de éxito Expert | Plan de éxito Ultimate |
|--- |--- |--- |
|  | Con el plan de éxito Expert, puede acceder a la **asistencia de expertos de forma ininterrumpida** para solucionar problemas técnicos y obtener ayuda sobre problemas críticos para su empresa. O puede encontrar resoluciones rápidas aprovechando nuestros recursos autodirigidos, las prácticas recomendadas exclusivas y una comunidad en línea de expertos y colegas de Adobe. <p> *Incluido con todas las licencias de Adobe Experience Cloud.* | Con el plan de éxito Ultimate, experimentará **ayuda estratégica y asistencia técnica proactiva para ofrecer experiencias digitales de alto rendimiento**. Su entorno de Adobe contará con el apoyo de un equipo de expertos familiarizados con su empresa y centrados en ejecutar una hoja de ruta alineada con sus objetivos y prioridades para el impacto empresarial. |
| **Equipo de éxito** | Equipo conjunto de ingenieros de soporte | Incluye: <ul><li> Administrador técnico de cuentas designado </li><li> Customer Success Manager designado </li><li> Administrador de servicios de soporte designado</li><li> Equipo conjunto de ingenieros técnicos y expertos estratégicos que ofrecen aceleradores de éxito </li><li> Equipo conjunto de ingenieros de soporte </li></ul> |
| **Asistencia técnica y operativa proactiva** | ![icono no incluido](../assets/Cross_red_circle.svg){width="20"} No incluido | Incluye: <ul><li>Revisiones de actualización y migración, preparación de versiones </li><li>Revisiones de hoja de ruta de productos</li><li> Hojas de ruta técnicas y estratégicas alineadas</li><li>Preparación y planificación de eventos clave</li><li>Planificación de la capacitación relevante y oportuna</li><li>Prácticas técnicas recomendadas y directrices del sector</li><li>Defender/alinearse con los equipos de productos</li><li>Plan unificado para lograr los objetivos empresariales clave - Plan de Acción Mutua (MAP)</li></ul> |
| **Asistencia técnica** | Incluye: <ul><li>**P1**: asistencia ininterrumpida de problemas</li><li>**P2, P3, P4**: asistencia en horario laboral</li><li>Administración de interrupciones estándar</li><li>Administración de la escalabilidad agrupada</li></ul> | Incluye: <ul><li>**P1**: asistencia ininterrumpida de problemas</li><li>**P2/P3**: asistencia ininterrumpida de problemas</li><li>**P4**: asistencia en horario laboral</li><li>Administración prioritaria de las interrupciones</li><li>Administración de la escalabilidad de expertos designados</li></ul> |
| **Aceleradores de éxito** | ![icono no incluido](../assets/Cross_red_circle.svg){width="20"} No incluido | Aceleradores de éxito programados periódicamente por TAM y CSM<p>*(consulte Catálogo del acelerador de éxito para obtener más información)* |
| **Canales de soporte** | En línea, teléfono, Experience League, foros | Portal en línea personalizado, teléfono priorizado, Experience League, foros |

{style="table-layout:fixed"}

## Complementos de soporte

| Complementos | Plan de éxito Expert | Plan de éxito Ultimate |
|--- |--- |--- |
| **Complemento de administración de eventos**<br> Proporciona el liderazgo y la asistencia integrales necesarios para administrar todo el ciclo de vida de los eventos clave | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Complemento de director de cuenta técnica**<br> Su recurso técnico principal que realiza la supervisión, asume el compromiso ejecutivo y garantiza la gobernanza para maximizar los resultados de su empresa | ![icono no disponible](../assets/Cross_red_circle.svg){width="20"} No disponible | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Complemento de asistencia avanzada en la nube**<br> Asistencia y garantía de valor de nivel superior para clientes de Adobe Experience Manager as a Cloud Service | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Complemento de sesiones de mentor**<br> Proporciona aprendizaje basado en habilidades en un método de formación justo a tiempo | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icono disponible](../assets/green_checkmark.svg){width="20"} Incluido |
| **Complemento de impulso del desarrollador**<br> Proporciona acceso a expertos de servicios de ingeniería en el terreno que pueden ayudarle con el trabajo de reparación de averías | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icono incluido](../assets/green_checkmark.svg){width="20"} Incluido |
| **Complemento de Paquete de cola de prioridad**<br> Omita la línea para que sus tickets se procesen primero con acceso adicional a Sesiones de mentor y a Impulso del desarrollador | ![icono disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icono incluido](../assets/green_checkmark.svg){width="20"} Incluido |

{style="table-layout:fixed"}
