---
title: Descargar registros de auditoría e informes de exportación
description: Obtenga información sobre cómo los administradores globales ven, filtran y exportan registros e informes de auditoría en Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d9dd4958b09ab10c4755671c0956698223c0a7b0
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 2%

---


# Descargar registros de auditoría e informes de exportación

Se aplica a la empresa.

Obtenga información sobre cómo los administradores globales ven, filtran y exportan registros e informes de auditoría mediante Global Admin Console.

Para empezar, inicia sesión en [Global Admin Console](https://global-admin-console.adobe.com/). A continuación, vaya a la pestaña **[!UICONTROL Insights]** y seleccione **[!UICONTROL Registros de auditoría]** para rastrear todos los cambios realizados en las organizaciones.

## Ver y descargar registros de auditoría

Como administrador global, tiene visibilidad total de los cambios realizados en Global Admin Console. Puede buscar en los registros de auditoría de todas las organizaciones las acciones realizadas en los últimos 90 días, incluso cuándo se produjeron y quién las realizó.
- Los registros de auditoría ayudan a garantizar el cumplimiento continuo mediante la protección contra el acceso inapropiado al sistema y la auditoría de comportamientos sospechosos dentro de su organización.
- Los registros disponibles en Global Admin Console incluyen solo eventos a los que un administrador global tiene acceso. No incluyen asignaciones de usuarios ni eventos de usuarios. [Más información](https://helpx.adobe.com/es/enterprise/using/admin-console.html) sobre las diferentes funcionalidades que ofrece cada consola.
- Los registros cubren los eventos de todas las organizaciones de la jerarquía, lo que permite buscar registros de auditoría en todas las organizaciones a la vez.

>[!NOTE]
>
> Como administrador del sistema en una organización [Adobe Admin Console](https://adminconsole.adobe.com), puede usar el [Registro de auditoría](https://helpx.adobe.com/es/enterprise/using/audit-logs.html) para revisar las asignaciones de usuarios y los eventos de usuarios. Las acciones realizadas por los administradores de sistemas de las organizaciones secundarias de la organización seleccionada también se incluyen en los registros de auditoría. Obtenga más información sobre cómo los administradores de sistemas pueden [rastrear cambios](https://helpx.adobe.com/es/enterprise/using/audit-logs.html) realizados en Admin Console.

Para ver o descargar registros de auditoría de su organización:

1. Como administrador global, inicia sesión en [Global Admin Console](https://global-admin-console.adobe.com/insights).
1. Seleccione **[!UICONTROL Información]** > **[!UICONTROL Registros De Auditoría]**.
Los registros de auditoría muestran la siguiente información para los eventos filtrados:

   | Campo | Descripción |
   |------ |-------------|
   | Fecha | Fecha y hora del evento, que se muestra en la zona horaria local. |
   | Nombre del evento | Descripción de la acción realizada. |
   | Detalles del evento | Detalles adicionales del evento, si están disponibles. |
   | Nombre de objeto | El nombre del producto, perfil de producto o grupo de usuarios que participan en el evento, según corresponda. |
   | Usuario afectado | Dirección de correo electrónico del usuario afectado, si corresponde. |
   | Administración | Dirección de correo electrónico del administrador que realizó la acción. *System* se muestra si la acción fue realizada por un sistema backend de Adobe. |
   | Dirección IP | Dirección IP del equipo donde se realizó la acción. Normalmente refleja la ubicación física, pero podría ser un servidor proxy o una dirección VPN. |
   | Organización | Nombre de la organización afectada por el evento. |


1. Puede filtrar los registros de auditoría mediante las siguientes opciones:

   - Buscar por usuario o administrador afectado.
   - Seleccione una o varias organizaciones.
   - Defina un intervalo de fecha.
   - Filtre por nombre de evento.
   - Puede combinar filtros para reducir los resultados, como la visualización de eventos de los últimos siete días para una organización específica.

   ![registros de auditoría](assets/audit-logs.png)

   *Filtre los registros de auditoría según el nombre del evento, la organización afectada o el intervalo de fechas.*

   ![select-organization](assets/select-organizations.png)

   *Seleccione organizaciones para filtrar los registros de auditoría.*

1. Para exportar los registros de auditoría, seleccione **[!UICONTROL Exportar CSV]** para exportar los resultados filtrados. Los resultados se descargan en formato CSV.

Para obtener detalles acerca de los campos incluidos en la exportación, vea [Esquema de registro](#log-schema).

>[!NOTE]
>
>Los informes de registro de auditoría exportados se conservan durante 90 días después de su generación.


## Comprender el informe de registro de auditoría {#log-schema}

El informe de registro de auditoría exportado incluye los siguientes campos para cada organización:

| Campo | Descripción |
|------|------------|
| id | ID de evento |
| eventTime | Fecha y hora del evento (zona horaria local) |
| eventType | Nombre del evento |
| eventSubType | Detalles adicionales del evento, si están disponibles |
| actorEmail | Dirección de correo electrónico del administrador que realizó el evento. *System* se muestra si el evento lo realizó un sistema back-end de Adobe. |
| targetUserEmail | Correo electrónico del usuario afectado, si corresponde |
| targetGroupName | Grupo de usuarios afectado, si corresponde |
| targetProductName | Producto afectado, si procede |
| targetProfileName | Perfil del producto afectado, si corresponde |
| ipAddress | Dirección IP del equipo donde se realizó la acción. Normalmente refleja la ubicación física, pero podría ser un servidor proxy o una dirección VPN. |
| organizationName | Nombre de la organización afectada |

## Descargar informes de exportación

Cuando cualquier administrador global exporta datos de organización desde [Global Admin Console](https://global-admin-console.adobe.com/insights), el informe se procesa y se pone a disposición en la ficha **[!UICONTROL Información]** de **[!UICONTROL Exportar informes]**.

Todos los informes generados por cualquier administrador global están disponibles en un solo lugar. La capacidad de exportar informes es útil en los siguientes casos:

- Si tiene una jerarquía grande con muchas organizaciones, ya no tiene que esperar a que se procese el archivo de exportación. Puede utilizar los informes generados por sus compañeros administradores.
- Ya no es necesario conservar ni guardar estos informes para compararlos más adelante. Los informes se conservan durante 90 días y se pueden descargar en cualquier momento para comparar informes.


Para descargar un informe de exportación:

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/insights) y vaya a **[!UICONTROL Información]** > **[!UICONTROL Exportar informes]**.

   Se muestran los informes generados en los últimos 90 días. Una vez completados los 90 días, puede generar el informe de nuevo. Aprenda a generar informes para [Estructura de la organización](https://helpx.adobe.com/enterprise/global-admin-console/export-and-import-data.html#export-and-import-organization-structure).


   | Campo | Descripción |
   |------|------------|
   | Información general de la tienda de aplicaciones | Fecha y hora de generación del informe (zona horaria local) |
   | Formato | Formato de archivo (CSV, JSON, XLSX) |
   | Tamaño | Tamaño de archivo |
   | Creado por | Dirección de correo electrónico del administrador que generó el informe |
   | Acción | Vínculo para descargar el informe |

1. Para descargar un informe, selecciona **[!UICONTROL Descargar]**.

   Si el informe que acaba de generar no aparece en la lista, seleccione **[!UICONTROL Actualizar]**.

![informes de exportación](assets/export-reports.png)

*Descargar cualquier informe generado en los últimos 90 días.*
