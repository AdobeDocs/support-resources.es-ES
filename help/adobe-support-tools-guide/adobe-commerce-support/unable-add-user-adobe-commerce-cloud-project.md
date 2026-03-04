---
title: No se puede agregar el usuario al proyecto en la nube de Adobe Commerce
description: Este artículo proporciona una solución para los casos en los que no pueda agregar un usuario a un proyecto en la nube de Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# No se puede agregar el usuario al proyecto en la nube de Adobe Commerce

Este artículo proporciona una solución para cuando intente agregar un usuario a un proyecto en la nube, pero se produce un error: *El usuario XXX no existe*.

## Productos y versiones afectados

* Adobe Commerce en la infraestructura de nube, [todas las versiones compatibles](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problema

Este artículo proporciona una solución para los casos en los que no pueda agregar un usuario a un proyecto en la nube de Adobe Commerce.

## Causa

La cuenta del usuario debe crearse primero en [https://accounts.magento.cloud](https://accounts.magento.cloud) y vincularse a su SSO de Adobe para poder agregarse como usuario al proyecto. Si el usuario tiene una cuenta de Adobe pero no una cuenta de Commerce (magento.com), primero debe crear una.

## Solución

1. Pida al usuario que inicie sesión en [https://accounts.magento.cloud](https://accounts.magento.cloud). El usuario ya debe estar registrado en Adobe con la misma dirección de correo electrónico.
   >[!NOTE]
   >Crear o tener una cuenta en [https://account.adobe.com](https://account.adobe.com) no significa automáticamente que el usuario tenga una cuenta en [https://accounts.magento.cloud](https://accounts.magento.cloud). El usuario debe [crear primero su cuenta de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Si el usuario ya tiene una cuenta de Adobe pero no puede iniciar sesión, pídele que envíe una [solicitud de asistencia](https://experienceleague.adobe.com/home#support) con el [!UICONTROL Motivo del problema] establecido en *Administración de usuarios*.

1. Una vez que el usuario inicie sesión correctamente en [https://accounts.magento.cloud](https://accounts.magento.cloud), puede agregarlo al proyecto. Para obtener pasos detallados, consulte [Agregar usuarios y administrar el acceso](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) en la Guía de infraestructura de Commerce en la nube.

## Lectura relacionada:

* [Administrar el acceso de usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) en nuestra Guía de infraestructura de Commerce en la nube.
* [No se puede iniciar sesión en la cuenta en la nube o en la asistencia de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
