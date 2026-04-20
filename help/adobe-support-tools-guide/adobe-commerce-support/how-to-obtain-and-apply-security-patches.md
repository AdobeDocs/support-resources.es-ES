---
title: Cómo obtener y aplicar [!UICONTROL parche de seguridad]
description: Este artículo contiene instrucciones sobre cómo obtener y aplicar un [!UICONTROL parche de seguridad] que se ha publicado, pero las instrucciones no están disponibles.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: eee15976f3dd402e84774ec5b769d952259c8dff
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Cómo obtener y aplicar un [!UICONTROL parche de seguridad]

>[!NOTE]
>Si tiene una instalación On-Premise y no utiliza sistemas de control de versiones como [!DNL CVS] o GitHub para administrar su código, es posible que su host web pueda ayudarle a aplicar la revisión. No dude en ponerse en contacto con ellos para obtener apoyo.

Este artículo contiene instrucciones sobre cómo obtener y aplicar un [!UICONTROL parche de seguridad] que se ha publicado, pero las instrucciones no están disponibles.

## Productos y versiones afectados

Adobe Commerce on-premise e infraestructura en la nube: todas las versiones compatibles


## Causa

La mayoría de los [!UICONTROL parches de seguridad] se han publicado sin aplicar ningún parche o revisión aislados, por lo que será necesario actualizar a la versión de [!UICONTROL parche de seguridad].

En el caso de los boletines de seguridad de Adobe Commerce, Adobe solo proporciona un parche físico o archivo de revisión independiente cuando se publica o menciona explícitamente como parte de la versión del boletín. Si el boletín no incluye (o no hace referencia) a un paquete aislado de revisión/revisión, no podemos generar ni proporcionar uno después del hecho.

Esto se debe a que las correcciones de seguridad se desarrollan, prueban y envían juntas como parte de la versión de seguridad admitida (por ejemplo, una versión de parche) y no están diseñadas para separarse o desacoplarse claramente en archivos de parches CVE individuales sin riesgo de cobertura o regresiones incompletas.

La ruta de corrección admitida sigue aplicando la actualización de seguridad oficial para la línea de versión (o actualizando a una versión que incluya las correcciones).

## Solución


### Caso I:

* Si se menciona un archivo de revisión aislado en las [Notas de la versión](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite), descargue el archivo desde la sección de descarga de [https://account.magento.com](https://account.magento.com/downloads/view/). En primer lugar, el propietario de la cuenta o el titular de la licencia deben otorgar privilegios de descarga a los usuarios con acceso compartido.

**Advertencias:**

Si su versión de Adobe Commerce es anterior (2.4.4), automáticamente habrá recibido Soporte ampliado. Su versión debe ser una de las siguientes versiones no compatibles para poder aplicar los parches de seguridad más recientes disponibles:

2.4.4 - 2.4.4-p11

Las versiones no compatibles (2.3.x, 2.4.0 - 2.4.3) no son compatibles y primero debe actualizar a una versión compatible para aprovechar las últimas correcciones de seguridad.

Si no tiene soporte ampliado, puede solicitar al soporte técnico que comparta los parches con usted, pero no podrán resolver ningún problema o error que pueda encontrar al aplicarlos.

### Caso II:

Los parches aislados solo se proporcionan en casos excepcionales y no es la forma preferida de implementar correcciones de seguridad.

Si no se menciona un archivo o revisión aislado en las Notas de la versión:

* **Nube:**

1. Es posible que algunos [!UICONTROL parches de seguridad] se incluyan o publiquen en la última versión de Cloud Tools Suite (herramientas ECE) en Cloud Patches para Commerce. Compruebe las [Notas de la versión](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) y, si se menciona una corrección de seguridad en la versión, actualice el paquete a esa versión.
1. Si en las Notas de la versión no se menciona una corrección de seguridad, continúe leyendo.

* **Infraestructura en la nube o local:**

* Si no hay disponible un archivo de revisión aislado, [actualice la versión de Adobe Commerce en la infraestructura en la nube](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X a la última versión de revisión 2.4.X-pY.
* Si no hay disponible un archivo o revisión aislado, [actualice la versión On-Premise de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X a la última versión de revisión 2.4.X-pY.

## Lectura relacionada

* Consulte [Notas de la versión del conjunto de herramientas de Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) en la *Guía de Adobe Commerce en la infraestructura de la nube*.
* Consulte [Actualizar la versión de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) en la *Guía de Adobe Commerce en la infraestructura de la nube*.
