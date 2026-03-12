---
title: Crear informes de asignación de licencias para varias organizaciones y productos
description: Generar, ver y descargar informes de asignación de licencias en varias organizaciones y productos desde Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: dbbd971e57265e1651f44f834e56d461159ab4fc
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Crear informes de asignación de licencias para varias organizaciones y productos

Descubra cómo los administradores globales pueden generar y descargar informes de licencias detallados para varias organizaciones y productos para intervalos de fechas específicos a fin de facilitar un seguimiento preciso del aprovisionamiento de licencias.

>[!NOTE]
>
>Para crear, ver y exportar un informe de asignación de licencia, inicia sesión en [Global Admin Console](https://global-admin-console.adobe.com/) y ve a **[!UICONTROL Información]** > **[!UICONTROL Informes]** > **[!UICONTROL Asignación de licencia]**.

## Creación de un informe

Los informes de asignación de licencias le ayudan a supervisar de forma proactiva el aprovisionamiento de licencias y reducir el seguimiento manual. Los administradores globales pueden crear un informe de asignación de licencias para productos seleccionados para cualquier número de organizaciones secundarias con el fin de supervisar los datos de aprovisionamiento de licencias de software en todos los departamentos.

1. Vaya a la ficha **[[!UICONTROL Información]](https://global-admin-console.adobe.com/insights)** de Global Admin Console.
1. En la página **[!UICONTROL Asignación de licencias]**, seleccione **[!UICONTROL Crear informe]**.
1. Seleccione las organizaciones y seleccione **[!UICONTROL Siguiente]**. Puede elegir individualmente cada organización o seleccionar todas las organizaciones secundarias dentro de una principal mediante el botón **[!UICONTROL Seleccionar todo]**.

>[!NOTE]
>
>**Sepa por qué no puede seleccionar ciertas organizaciones**:
>Si una organización secundaria no tiene un contrato o tiene un contrato empresarial independiente con el mismo producto que la organización principal, se desactiva la creación de un informe de asignación de licencias. Por ejemplo, si el contrato de la organización principal tiene Adobe Acrobat y la organización secundaria tiene el mismo como parte de otro contrato, el producto está limitado para su asignación. Como resultado, también es limitado para la creación de informes en Global Admin Console. [Aprenda a realizar el seguimiento del aprovisionamiento para estas organizaciones mediante sus respectivas Admin Console](https://helpx.adobe.com/enterprise/using/assignment-reports.html).
>
>[!NOTE]
>
>Sólo se pueden crear informes de asignación para organizaciones con un contrato activo.

1. Seleccione los productos que desea incluir en el informe y seleccione **[!UICONTROL Siguiente]**.

>[!NOTE]
>
>**Sepa por qué no puede seleccionar determinados productos**:
>Los productos que no se pueden asignar en Global Admin Console no se incluyen en la creación de informes. Actualmente, esto incluye algunos productos de Digital Experience como [!DNL Workfront], [!DNL Adobe Experience Manager] y [!DNL Adobe Experience Platform], así como productos como [!DNL Adobe Firefly Services], [!DNL Acrobat Sign] y [!DNL Adobe Stock]. [Utiliza Adobe Admin Console para buscar los datos de aprovisionamiento de licencias de estos productos](https://helpx.adobe.com/enterprise/using/assignment-reports.html).

1. Seleccione si desea agregar el informe por mes o año.
1. Seleccione un intervalo de fechas personalizado o elija entre las opciones preestablecidas. Puede elegir cualquier fecha de inicio desde el 18 de junio de 2020 hasta el día anterior, siempre que no sea anterior a la fecha de inicio del contrato.
1. Seleccione **[!UICONTROL Descargar]** para exportar el informe como archivo CSV.

El informe comienza a procesarse y aparece en la página **[!UICONTROL Asignación de licencias]** con detalles como nombre, creador, hora de creación, intervalo de fechas y estado. Una vez listo, recibirá una notificación por correo electrónico y el informe se descargará automáticamente.

Cualquier administrador global puede descargar el informe en cualquier momento después de estar listo, usando el icono **[!UICONTROL Descargar]** junto al nombre del informe.

>[!NOTE]
>
>- Para asegurarse de que se reflejen los datos más recientes, genere informes 48 horas después de cualquier asignación.
>- Los informes se conservan durante 90 días después de su generación.

## Ver y descargar informes generados anteriormente

Los administradores globales pueden ver y descargar los informes de asignación de licencias generados por cualquier otro administrador global de su organización. Sin embargo, los visores globales solo pueden ver la lista de informes de asignación de licencias.

1. Vaya a la ficha **[[!UICONTROL Información]](https://global-admin-console.adobe.com/insights)** de Global Admin Console.
1. En la página **[!UICONTROL Asignación de licencias]**, todos los informes se muestran con los siguientes detalles:

   | Campo | Descripción |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Nombre | Se genera automáticamente y no se puede editar. |
   | Creador | El administrador global que generó el informe. |
   | Hora de creación | Hora del sistema en la que se creó el informe. |
   | Intervalo de fechas | El intervalo de fechas seleccionado para el informe. |
   | Estado | **Éxito** si el informe está listo para descargar o **Procesando** si aún se está generando. |

1. Para exportar el informe como archivo CSV, seleccione el icono **[!UICONTROL Descargar]** que hay junto al informe.

## Conocer el informe de asignación de licencias

El informe que descargue contiene la siguiente información para cada evento:

| Campo | Descripción |
| -------------------------------- | -------------------------------------------------------- |
| ID de la organización | ID único vinculado a la organización principal |
| Nombre de organización | Nombre de la organización principal |
| ID de organización secundaria | Identificador único de la organización secundaria seleccionada |
| Nombre de la organización secundaria | Nombre de la organización secundaria |
| ID de licencia | ID único de la licencia del producto |
| Nombre del producto | Nombre del producto seleccionado |
| Fecha | Selección de fecha |
| Cantidad total de licencias | Número total de licencias en el nivel de organización principal |
| Licencias secundarias | Recuento de licencias asignado a la organización secundaria |
| Cant. asignada máxima mensual/anual | Valor agregado del aprovisionamiento de licencias (mensual/anual) |
