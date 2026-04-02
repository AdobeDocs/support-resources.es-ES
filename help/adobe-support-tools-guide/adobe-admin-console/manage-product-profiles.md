---
title: Administración de perfiles de producto en Global Admin Console
description: Descubra cómo los administradores globales pueden añadir, editar y eliminar perfiles de producto en Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 1%

---

# Administración de perfiles de producto en Global Admin Console

**Se aplica a:** Empresa

Los administradores globales pueden agregar, editar y eliminar perfiles de producto en [Global Admin Console](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>En [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), seleccione una organización y vaya a **[!UICONTROL Productos]**. Puede activar todos los servicios o los servicios seleccionados para un producto mediante Perfiles de producto.

Al igual que en el Admin Console estándar, los perfiles de producto le permiten ajustar el uso de los productos dentro de una organización. También puede asignar administradores (llamados **[!UICONTROL administradores de perfil de producto]**) a perfiles de producto. Estos administradores pueden agregar usuarios finales a los perfiles de producto que administran.

Para administrar perfiles de producto, seleccione un producto. Se mostrarán los controles para agregar, editar y eliminar perfiles de producto.

>[!NOTE]
>
>En algunos productos, no se pueden crear ni editar perfiles de producto en Global Admin Console. En estos casos, use [Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) en su lugar.

## Añadir un perfil de producto

1. En [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editar y luego vaya a la pestaña **[!UICONTROL Productos]**.
1. Seleccione un producto al que añadir un perfil de producto.
1. Seleccione **[!UICONTROL Agregar perfil]**.
1. En el cuadro de diálogo **[!UICONTROL Agregar perfil]**, escriba los siguientes detalles:

   | Campo | Descripción |
   |---|---|
   | **[!UICONTROL Nombre]** | Un nombre único para el perfil de producto dentro de la organización, distinto de otros perfiles de producto y grupos de usuarios. |
   | **[!UICONTROL Cuota]** | El número de destino de licencias asignadas para este perfil. |
   | **[!UICONTROL Grupos de usuarios]** | Seleccione en el menú desplegable o escriba un nombre de grupo de usuarios. Si el grupo de usuarios aún no existe, créelo primero a través de la ficha [**[!UICONTROL Grupos de usuarios ]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Administradores]** | Seleccione en el menú desplegable o escriba una dirección de correo electrónico de administrador. Si el administrador aún no existe, créelo primero a través de la ficha [**[!UICONTROL Administradores ]**](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators). |

   Los [!UICONTROL grupos de usuarios] especificados se han asignado al perfil del producto. Los administradores especificados se convierten en los **[!UICONTROL administradores de perfil de productos]**, que pueden administrar el perfil a través de Adobe Admin Console para la organización correspondiente.

   ![Agregar perfil](./assets/manage-product-profiles_add-profile.png)

1. Utilice la opción **[!UICONTROL Notificaciones]** para habilitar o deshabilitar las notificaciones por correo electrónico. Cuando se habilita, se notifica por correo electrónico a los usuarios cuando se agregan o eliminan del perfil.
1. Use las opciones individuales de **[!UICONTROL Servicios]** para habilitar o deshabilitar servicios específicos para el perfil del producto. Para obtener más información, consulte [Habilitar o deshabilitar servicios para un perfil de producto](https://helpx.adobe.com/enterprise/using/enable-disable-services.html).
1. Seleccione **[!UICONTROL Guardar]**.
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** una vez que haya terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Edición de un perfil de producto

1. Seleccione una organización para editarla, vaya a la ficha **[!UICONTROL Productos]** y seleccione un producto.
1. Seleccione el icono **[!UICONTROL Más opciones]** ![Más opciones](./assets/manage-product-profiles_more-options.png) para el perfil de producto correspondiente y, a continuación, seleccione **[!UICONTROL Editar perfil]**.
1. Actualice los detalles del perfil del producto según sea necesario y seleccione **[!UICONTROL Guardar]**.
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** una vez que haya terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminación de un perfil de producto

>[!WARNING]
>
> Al eliminar un perfil de producto, se elimina el acceso al producto de todos los usuarios que eran miembros de dicho perfil o que pertenecían a grupos de usuarios adjuntos a dicho perfil.

1. Seleccione una organización para editarla, vaya a la ficha **[!UICONTROL Productos]** y seleccione un producto.
1. Seleccione el icono **[!UICONTROL Más opciones]** ![Más opciones](./assets/manage-product-profiles_more-options.png) para el perfil de producto correspondiente y, a continuación, seleccione **[!UICONTROL Eliminar perfil]**.
1. Seleccione **[!UICONTROL Aceptar]** en el cuadro de diálogo de confirmación.
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** una vez que haya terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).


## Lectura relacionada

- [Adoptar la administración global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [Administrar administradores](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [Administrar grupos de usuarios](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [Asignar productos a organizaciones secundarias](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [Ejecutar trabajos pendientes](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [Habilitar/deshabilitar servicios](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Información general de Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
