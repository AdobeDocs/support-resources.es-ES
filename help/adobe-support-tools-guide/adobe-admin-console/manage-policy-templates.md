---
title: Administración de plantillas de directivas en Global Admin Console
description: Descubra cómo los administradores globales pueden aplicar plantillas de directivas a cualquier organización secundaria, directa o indirectamente desde la organización en la que están almacenadas en Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: e4dc5c35-1323-4894-bd47-b31c61a864bc
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Administración de plantillas de directivas en Global Admin Console

**Se aplica a:** Empresa

Descubra cómo los administradores globales pueden aplicar plantillas de directivas a cualquier organización secundaria, directa o indirectamente desde la organización en la que están almacenadas en Global Admin Console.

>[!NOTE]
>
>En [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html), seleccione una organización para editarla y vaya a la pestaña **Plantillas de directivas** para optimizar la configuración y facilitar una administración coherente de las directivas en todas las organizaciones.
>
> [Iniciar sesión en Global Admin Console](https://global-admin-console.adobe.com/)

## Funcionamiento de las plantillas de directiva

Las plantillas de directivas se almacenan con una organización y son visibles para todos los administradores globales de dicha organización. Una vez aplicadas, las entradas de la plantilla de directiva se establecen individualmente en cada organización. Cuando se aplica una plantilla de directiva a una organización, cada una de las entradas de la plantilla de directiva se aplica a las directivas de la organización, reemplazando los valores de directiva existentes.

### Comportamiento de directiva bloqueado

Las actualizaciones de las directivas bloqueadas solo se realizan si el usuario que aplica la actualización es un administrador global de la organización indicada por el icono **[!UICONTROL Bloqueado por]** de la directiva que se está actualizando.

Si el usuario que aplica la plantilla tiene permiso para desbloquear la directiva, los bloqueos de directiva toman los valores de la plantilla aplicada (bloqueada o desbloqueada). Si la plantilla indica que el bloqueo debe dejarse tal cual, el valor del bloqueo en la directiva permanece igual que antes.

### Nota importante al guardar

>[!NOTE]
>
>A diferencia de otros cambios realizados en Global Admin Console, las ediciones en las plantillas de directivas se aplican inmediatamente sin necesidad de pasar por el proceso **[!UICONTROL Revisar cambios pendientes - Enviar]**. Sin embargo, para implementar cambios pendientes en organizaciones donde se aplica la plantilla de directiva, se requiere [envío](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Crear una plantilla de directiva

1. En [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editarla y luego vaya a la pestaña **[!UICONTROL Plantillas de directivas]**.
1. Seleccionar **[!UICONTROL Crear plantilla]**.<br>
   ![Imagen1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. En el cuadro de diálogo **[!UICONTROL Crear plantilla de directiva]**, escriba el **nombre** y **descripción** para la plantilla de directiva.<br>El nombre de la plantilla de directiva puede tener un máximo de 100 caracteres.
1. Seleccione las políticas que desea incluir en la plantilla.
1. Establecer valores para las directivas seleccionadas (consulte [Configurar valores de directiva](#setting-policy-values) a continuación).
1. Seleccione **[!UICONTROL Guardar]**.

### Estableciendo valores de directiva {#setting-policy-values}

Para cada directiva incluida en la plantilla, configure dos opciones:

* **Permitido / No permitido:** Establezca el control deslizante en el valor deseado. Más información sobre [detalles de la directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#policy-details).
* **Valor de bloqueo:** Modifique el estado de bloqueo de la directiva mediante una de las siguientes opciones:
   * **Bloquear**: la directiva se bloqueará después de aplicar la plantilla.
   * **Desbloquear**: la directiva se desbloqueará después de aplicar la plantilla.
   * **Mantener tal cual** — El estado de bloqueo de la directiva se dejará igual que antes de que se aplicara la plantilla.<br>
     ![Imagen2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## Aplicación de una plantilla a las organizaciones

1. En [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editarla y luego vaya a la pestaña **[!UICONTROL Plantillas de directivas]**.
1. Seleccione el icono **[!UICONTROL Más opciones]** ![Más opciones](./assets/manage-product-profiles_more-options.png) para la plantilla de directiva correspondiente y seleccione **[!UICONTROL Aplicar plantilla a la organización]**.<br>
   ![Imagen3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. Seleccione las organizaciones a las que desea aplicar la plantilla. Puede seleccionar varias organizaciones.<br>
   ![Imagen4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. Seleccione **[!UICONTROL Aplicar plantilla]**.
1. Para implementar cambios pendientes en organizaciones donde se aplica la plantilla de directiva, seleccione **[!UICONTROL Revisar cambios pendientes]**. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Si todos los valores de directivas de las organizaciones seleccionadas ya coinciden con los valores de la plantilla, aparece un mensaje que notifica que no se han realizado cambios. Además, **[!UICONTROL Revisar cambios pendientes]** no está habilitada si no hay otras ediciones pendientes.

## Edición de una plantilla

1. En [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editarla y luego vaya a la pestaña **[!UICONTROL Plantillas de directivas]**.
1. Seleccione el icono **[!UICONTROL Más opciones]** ![Más opciones](./assets/manage-product-profiles_more-options.png) para la plantilla correspondiente y seleccione **[!UICONTROL Editar plantilla]**.<br>
   ![Imagen5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. Actualice la plantilla de directiva y seleccione **[!UICONTROL Actualizar ahora]**.
1. Para implementar cambios pendientes en organizaciones donde se aplica la plantilla de directiva, seleccione **[!UICONTROL Revisar cambios pendientes]**. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminación de una plantilla

1. En [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editarla y luego vaya a la pestaña **[!UICONTROL Plantillas de directivas]**.
1. Seleccione el icono **[!UICONTROL Más opciones]** ![Más opciones](./assets/manage-product-profiles_more-options.png) para la plantilla correspondiente y seleccione **[!UICONTROL Eliminar plantilla]**.<br>
   ![Imagen6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. Seleccione *Yes* en el cuadro de diálogo que aparece.
