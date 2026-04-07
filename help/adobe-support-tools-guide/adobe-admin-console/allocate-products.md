---
title: Asignación de productos a organizaciones secundarias mediante Global Admin Console
description: Descubra cómo los administradores globales pueden distribuir recursos a las organizaciones secundarias, lo que permite una administración eficaz de los recursos y la asignación de usuarios dentro de cada organización.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Asignación de productos a organizaciones secundarias mediante Global Admin Console

Se aplica a la empresa.

Descubra cómo los administradores globales pueden distribuir recursos a las organizaciones secundarias, lo que permite una administración eficaz de los recursos y la asignación de usuarios dentro de cada organización.

En [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration), vaya a la ficha **[!UICONTROL Asignación de productos]** y, a continuación, seleccione un producto para asignarlo a organizaciones secundarias.

Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com).

>[!NOTE]
>
>La **[!UICONTROL asignación de productos]** solo está disponible para contratos de licencia con plazo Enterprise (ETLA).

Parte de la distribución y administración de productos de Adobe entre organizaciones consiste en dividir los recursos adquiridos en asignaciones de recursos entre las organizaciones que se van a administrar. Puede distribuir la administración de recursos de productos a otras organizaciones proporcionando todos o algunos de los recursos. No se pueden asignar todos los recursos de todos los productos; algunos productos no se pueden distribuir a otras organizaciones. Estos productos aparecen en la ficha **[!UICONTROL Asignación de productos]**, pero no tienen controles para agregarlos a otras organizaciones.

>[!WARNING]
>
>No puede asignar productos a una organización secundaria a partir de un contrato que tenga **caducado** o si la organización está en un estado **inactivo**. Obtenga más información sobre [caducidad del contrato](https://helpx.adobe.com/enterprise/using/contract-expiry.html) o póngase en contacto con el administrador de su empresa para obtener ayuda y evitar que los usuarios de la organización secundaria pierdan el acceso a sus aplicaciones y servicios de Adobe.

## Almacenamiento agrupado

Esto se aplica a los clientes que tienen una pestaña de almacenamiento en su Admin Console. Si no ve una pestaña Almacenamiento, significa que su Admin Console aún no se ha actualizado al modelo de almacenamiento empresarial. Una vez migrada su organización, verá los siguientes cambios:

- Los administradores globales obtienen acceso a la cuota de almacenamiento y al uso en toda la jerarquía, y pueden asignar almacenamiento a organizaciones mediante la ficha **[!UICONTROL Asignación de productos]** en [Global Admin Console](https://adminconsole.adobe.com/).
- Los administradores de sistemas y de almacenamiento tienen control total y visibilidad del almacenamiento en toda la organización. Pueden rastrear y administrar el almacenamiento usando la ficha **[!UICONTROL Almacenamiento]** en [Adobe Admin Console](https://adminconsole.adobe.com/).

Con las actualizaciones del almacenamiento de Adobe Creative Cloud, las cuotas de almacenamiento son flexibles para los usuarios finales, hasta la cantidad de almacenamiento adquirido por la organización. [Más información](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Asignar productos

La pestaña **[!UICONTROL Asignación de productos]** de Global Admin Console muestra las unidades de asignación de productos comprados en toda la jerarquía de la organización. Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puede asignar estos recursos de productos a otra organización en el árbol de organizaciones y especificar la cantidad de asignación. Como [visor global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puede ver y exportar los datos, pero no puede realizar ninguna actualización.

Para asignar productos a una organización, siga estos pasos:

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com) y vaya a **[!UICONTROL Asignación de productos]**.
1. Seleccione un producto de la lista desplegable para ver cómo se asigna a diferentes organizaciones.\
   Si una organización no tiene el producto actualmente, aparece el icono **[!UICONTROL Agregar +]**.

   >[!NNota]
   >
   >Si la organización secundaria ya tiene un contrato de compra, la asignación de productos de la organización principal a esa organización secundaria puede estar limitada. [Más información](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Para asignar el producto, seleccione el icono **[!UICONTROL Agregar +]** para la organización correspondiente.\
   Algunos productos incluyen más de un recurso que se puede asignar; en ese caso, se muestran varios recursos en el cuadro de diálogo y debe proporcionar valores para cada uno. Por ejemplo, Adobe Stock puede incluir créditos de Adobe Stock Image y créditos premium.
   ![Imágenes de Adobe Stock](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. En el cuadro de diálogo que aparece, especifique la cantidad de producto.
1. Seleccione **[!UICONTROL Guardar]**.
1. Para permitir o impedir la sobreasignación de un recurso, seleccione la opción correspondiente.
   ![Sobreasignación](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de asignar recursos. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Asignar y distribuir licencias o transacciones de usuarios de Adobe Acrobat Sign

Global Admin Console permite asignar y distribuir licencias o transacciones de usuarios de Acrobat Sign entre la jerarquía organizativa. Cada organización de la jerarquía que tiene asignadas licencias o transacciones de Acrobat Sign crea su propia cuenta de Acrobat Sign independiente.

- Cada cuenta de Acrobat Sign creada es independiente y está en silo en términos de administración y contenido.
- Cada cuenta de Acrobat Sign desconoce otras cuentas de Acrobat Sign (por ejemplo, en organizaciones principales o hermanas).

Más información acerca de [administrar Adobe Acrobat Sign en Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Para administrar los complementos de autenticación, como la autenticación basada en conocimientos (KBA) y la autenticación por teléfono (PA), póngase en contacto con su representante de Adobe o con el administrador de éxito del cliente.


## Limitaciones en la asignación de productos

La asignación de una organización principal a una organización secundaria está limitada en estos casos:

- Si ambas organizaciones tienen contratos diferentes y el producto que intenta asignar existe en ambas, no se permite combinar la misma oferta entre contratos.
- Si ambas organizaciones tienen el mismo contrato, puede solicitar permiso para asignar el producto poniéndose en contacto con su representante de Adobe o enviando un caso de [soporte técnico](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) en el que se especifique que **[!UICONTROL Asignación de productos]** está bloqueada en Global Admin Console.

## Sobreasignación

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puede permitir la sobreasignación de recursos.

Una asignación [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies) asociada con el producto y la organización indica si se permite la sobreasignación.

La sobreasignación permite conceder a una organización secundaria más recursos de producto de los que hay disponibles en la organización principal. Resulta útil cuando las asignaciones son aproximadas y el administrador no desea tener que cargar con la tarea de mantener las asignaciones de recursos acumuladas.
Si la sobreasignación está deshabilitada para un recurso de producto en una organización, la suma de las concesiones secundarias no puede superar la concesión principal. No se ejecutan las solicitudes de sobreasignación de un recurso marcado con la sobreasignación deshabilitada.
Cuando se activa o desactiva la opción de sobreasignación, los valores de concesión deben ajustarse para eliminar la sobreasignación antes de que se puedan ejecutar las actualizaciones de concesión, si existe una situación de sobreasignación en las cantidades de concesión de un recurso.

![Sobreasignación](/help/adobe-support-tools-guide/assets/overallocation.png)

## Contratos caducados en la jerarquía

No puede asignar productos a una organización secundaria desde un contrato de ETLA que haya caducado. Los titulares y las notificaciones en la aplicación, como los siguientes, de las páginas de **[!UICONTROL Información general]** y **[!UICONTROL Asignación de productos]** indican claramente cuándo caducará el contrato de una o más organizaciones secundarias, cuándo ha caducado o cuándo está inactivo.

![Asignación de productos](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[!IImportante]
>
>Una vez que un contrato de ETLA que forma parte de la jerarquía está inactivo, los productos se eliminan de las páginas **[!UICONTROL Información general]** y **[!UICONTROL Asignación de productos]**.

[Obtenga más información sobre la caducidad del contrato](https://helpx.adobe.com/enterprise/using/contract-expiry.html) o póngase en contacto con el administrador de su empresa para obtener ayuda y evitar que los usuarios de la organización secundaria pierdan el acceso a sus aplicaciones y servicios de Adobe.
