---
title: Cómo incluir un miembro del equipo en las notificaciones de asistencia
description: Este artículo explica cómo incluir un miembro del equipo en las notificaciones de asistencia.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2: id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# Cómo incluir un miembro del equipo en las notificaciones de asistencia

Este artículo explica cómo incluir a un miembro del equipo para que reciba automáticamente las actualizaciones de soporte a través de las notificaciones por correo electrónico.

## Productos y versiones afectados

* Adobe Commerce en la infraestructura en la nube, todas [versiones compatibles](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Causa

* El miembro del equipo no se ha agregado a [!DNL cloud project] con los privilegios necesarios.
* El miembro del equipo no tiene una cuenta de soporte técnico.

## Solución

1. Vaya a **[!DNL Cloud Project URL]** (ejemplo: `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Compruebe si el miembro del equipo se ha agregado al proyecto y es un [!DNL Project Admin].

Si no se han agregado al proyecto, deberá agregarlos como [!DNL Project Admin] y conceder a [!DNL Shared Access]:

* [Administrar el acceso de los usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) en nuestra guía del usuario.
* [No se puede agregar un usuario al proyecto de nube de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=es) en nuestra Base de conocimiento de Commerce.
* [Guía del usuario del Centro de ayuda de Adobe Commerce: Acceso compartido](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#shared-access) en nuestra Base de conocimiento de Commerce.

Si se han agregado a [!DNL cloud project], pero no tienen [!DNL Project Admin role], actualice [!DNL role] según corresponda en [Administrar acceso de usuario](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).

Si desea permitir que un miembro del equipo supervise todos los casos abiertos para su organización, envíe un [ticket de asistencia](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support).

## Lectura relacionada

[Los antiguos integrantes del equipo reciben correos electrónicos de notificación de Adobe Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)
