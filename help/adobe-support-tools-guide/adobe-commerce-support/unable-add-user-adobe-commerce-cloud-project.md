---
title: No se puede agregar el usuario al proyecto de nube de Adobe Commerce
description: Este artículo proporciona una solución para los casos en los que no pueda agregar un usuario a un proyecto de nube de Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 00451af3-7b97-5414-9992-3a6c269e413f
    internal-label: Paas
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# No se puede agregar el usuario al proyecto de nube de Adobe Commerce

Este artículo proporciona una solución para cuando intenta agregar un usuario a un proyecto en la nube, pero falla con un error: *El usuario XXX no existe*.

## Productos y versiones afectados

* Adobe Commerce en la infraestructura en la nube, [todas las versiones compatibles](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problema

Este artículo proporciona una solución para los casos en los que no pueda agregar un usuario a un proyecto de nube de Adobe Commerce.

## Causa

La cuenta del usuario debe crearse primero en [https://accounts.magento.cloud](https://accounts.magento.cloud) y vincularse a su SSO de Adobe para poder agregarse como usuario al proyecto. Si el usuario tiene una cuenta de Adobe pero no una cuenta de Commerce (magento.com), primero debe crear una.

## Solución

1. Pida al usuario que inicie sesión en [https://accounts.magento.cloud](https://accounts.magento.cloud). El usuario ya debe estar registrado en Adobe con la misma dirección de correo electrónico.
   >[!NOTE]
   >Crear o tener una cuenta en [https://account.adobe.com](https://account.adobe.com) no significa automáticamente que el usuario tenga una cuenta en [https://accounts.magento.cloud](https://accounts.magento.cloud). El usuario debe [crear primero su cuenta de Commerce](https://experienceleague.adobe.com/es/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Si el usuario ya tiene una cuenta de Adobe pero no puede iniciar sesión, pídale que envíe una [solicitud de soporte técnico](https://experienceleague.adobe.com/home?lang=es#support) con [!UICONTROL Motivo del problema] establecido en *Administración de usuarios*.

1. Una vez que el usuario haya iniciado sesión correctamente en [https://accounts.magento.cloud](https://accounts.magento.cloud), podrá agregarlo al proyecto. Para ver los pasos detallados, consulte [Agregar usuarios y administrar el acceso](https://experienceleague.adobe.com/es/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) en la Guía de infraestructura en la nube de Commerce.

## Lectura relacionada:

* [Administrar el acceso de los usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=es) en nuestra Guía de infraestructura de Commerce en la nube.
* [No se puede iniciar sesión en la asistencia de Adobe Commerce o en la cuenta de la nube](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=es)
