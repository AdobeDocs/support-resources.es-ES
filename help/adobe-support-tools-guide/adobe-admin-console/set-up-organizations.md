---
title: Administrar jerarquía de organización
description: Descubra cómo los administradores globales pueden administrar la jerarquía de la organización en Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# Administrar jerarquía de organización

Se aplica a la empresa.

Descubra cómo los administradores globales pueden administrar la jerarquía de la organización en Global Admin Console.

Una vez que obtenga acceso de [a [!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), podrá crear nuevas organizaciones, agregar organizaciones existentes a la jerarquía, eliminar organizaciones y cambiar una organización principal. Vaya aquí para [iniciar sesión en Global Admin Console](https://global-admin-console.adobe.com/)

Una organización es una estructura que se utiliza para administrar productos y usuarios de Adobe. [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) permite a los administradores administrar la implementación y configuración de los productos y usuarios de su organización. [[!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration) permite que los administradores globales creen, administren y eliminen varias organizaciones.

## Creación de una organización secundaria

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puede crear organizaciones secundarias de cualquier organización en la jerarquía y establecer el nombre, el país, los grupos de usuarios, los productos, los perfiles de producto, los administradores y las directivas.

Cuando se crea una nueva organización secundaria, las siguientes se heredan automáticamente del elemento principal inmediato:

- Configuración de [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) de la organización (incluidos los bloqueos si están presentes).
- La lista de administradores del sistema (controlada por **[!UICONTROL Heredar administradores del sistema al crear]** [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).
Lo siguiente puede impedir que se hereden los administradores del sistema:
   - Falta de [confianza de dominio](https://helpx.adobe.com/enterprise/using/directory-trust.html).
   - Restricciones de tipo de usuario (Añadir políticas de usuario de Adobe ID/Enterprise ID/Federated ID). Obtenga información acerca de [detalles de directivas](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Acceso a [[!DNL Federated ID]] o [[!DNL Enterprise ID]] usuarios de dominios a los que tiene acceso la organización principal. Esto hace que los usuarios del dominio principal estén disponibles en la organización secundaria. **Heredar usuarios de directorios administrados por la organización principal** [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) controla la herencia del acceso de usuarios.
- Directiva de uso compartido, directiva de contraseñas y contactos de seguridad (controlados por **Heredar la configuración de uso compartido de recursos cuando se crea la organización secundaria** [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la pestaña **[!UICONTROL Organizaciones]**, seleccione la organización a la que desee agregar una organización secundaria.
2. Seleccione el icono **[!UICONTROL Agregar+]**.
   ![Agregar organización](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Especifique un **nombre** y el **país** de la organización.\
   El nombre simple de la organización debe tener entre 4 y 100 caracteres; la longitud máxima de la ruta de acceso es de 255 caracteres.
   ![Agregar organización secundaria](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. Seleccione **[!UICONTROL Guardar]**.
5. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminación de una organización secundaria

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puede eliminar organizaciones secundarias. La operación de eliminación no se puede deshacer y no se puede eliminar la organización raíz. Los recursos asignados a la organización eliminada se devuelven a su organización principal. Antes de eliminar una organización, su organización principal se convierte automáticamente en la principal de cualquiera de sus organizaciones secundarias.

Una organización solo se puede eliminar si se cumplen los siguientes criterios:

- No hay cuentas de Sign, compras de Adobe Stock ni repositorios de almacenamiento en la organización.
- No hay dominios reclamados en la organización.
- No hay productos en los que se hayan creado instancias en la organización.
- No hay productos de Experience Cloud que puedan incluir instancias en la organización.

>[!WARNING]
>
>La eliminación de una organización afecta a los usuarios. Asegúrese de que no haya acceso ni información que se perderá cuando se elimine una organización.

1. Inicie sesión en [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Vaya a la pestaña **[!UICONTROL Organizaciones]** y seleccione la organización que desee eliminar.
1. Seleccione el icono **[!UICONTROL Eliminar]**.
   ![Eliminar organización](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. En el cuadro de diálogo **[!UICONTROL Eliminar organización]**, seleccione **[!UICONTROL Aceptar]**.
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Cambiar el nombre de una organización

El nombre de la organización es el nombre oficial de su empresa o institución, que se establece durante la compra. Los usuarios ven este nombre cuando seleccionan un perfil durante el inicio de sesión, especialmente si tienen acceso a productos de Adobe de varias organizaciones o si necesitan elegir entre un perfil profesional y uno personal.

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puede editar el nombre de cualquier organización principal o secundaria para ayudar a los usuarios a identificar el perfil correcto al iniciar sesión en [[!DNL Creative Cloud]] productos y servicios.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la ficha **[!UICONTROL Organizaciones]**, seleccione la organización cuyo nombre desea cambiar.
1. Seleccione el icono **[!UICONTROL Editar]**.
   ![Cambiar nombre de organización](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Actualice el nombre de su organización y seleccione **[!UICONTROL Guardar]**.

>[!TIP]
>
>Utilice un nombre de organización claro y reconocible de hasta 255 caracteres para ayudar a los usuarios a seleccionar el perfil correcto. Evite utilizar caracteres especiales y considere la posibilidad de incluir la región, el departamento o el derecho. Además, evite acrónimos poco comunes y nombres vagos o similares en la jerarquía de la organización.

Los cambios se registran en el registro de auditoría, se notifica a todos los usuarios por correo electrónico y el nombre no se puede actualizar de nuevo durante 24 horas. [Obtenga información sobre cómo ver y descargar registros de auditoría](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## Cambiar el elemento principal de una organización

Como [!DNL Global Administrator](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puede crear una organización en la jerarquía de organizaciones con el botón **[!UICONTROL Cambiar jerarquía]**.

Cambiar el elemento principal de una organización tiene el siguiente impacto:

- Al representar una organización, se mueve todo el subárbol enraizado en la organización reparada con él. Los nombres de ruta de la organización reparada y sus elementos secundarios se actualizan para reflejar su nueva ubicación.
- Las [directivas](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) de la organización de las organizaciones movidas se actualizan para que cualquier bloqueo de directivas sea mantenido por una organización en la nueva jerarquía.
- Cambiar la posición de una organización en la jerarquía puede cambiar los administradores globales de esa organización. Las funciones de administración global se heredan en la jerarquía inferior, de modo que los administradores globales de la nueva organización principal se convierten automáticamente en administradores globales de la organización trasladada. Del mismo modo, los administradores globales pueden perder su función en la organización desplazada si tienen esa función en virtud de ser administradores globales del padre antiguo. Las funciones de administración global heredadas no aparecen en el panel Administradores de la organización.
- La reparación también afecta a los productos disponibles en las organizaciones trasladadas. Cuando sea posible, [las asignaciones de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) se actualizarán para que lleguen a través de la nueva ubicación principal.
- Si las asignaciones de productos no se pueden actualizar para que provengan del nuevo elemento principal, los productos se eliminan junto con los perfiles de producto de esos productos. Los usuarios pueden perder el acceso como resultado de esta operación. Para que el producto esté disponible en la nueva ubicación, el antecesor común más cercano de las ubicaciones antigua y nueva debe tener el producto disponible.

>[!WARNING]
>
>Si los productos se eliminan como resultado de la reparación, los usuarios pierden el acceso a esos productos.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la ficha **[!UICONTROL Organizaciones]**, seleccione **[!UICONTROL Cambiar jerarquía]** para habilitar la reparación de las organizaciones.
2. Seleccione **[!UICONTROL Aceptar]** en la pantalla emergente que aparece.
3. Para ascender, arrastre la organización secundaria sobre la organización deseada.
4. Seleccione **[!UICONTROL Guardar]** cuando haya terminado de reparar sus organizaciones.
5. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Una vez completado el trabajo, puede ir a Asignación de productos y [cambiar los valores de concesión](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) para reflejar el cambio en la asignación de recursos de productos.

## Añadir organizaciones existentes mediante el asignador de organizaciones

Como [Administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puede agregar organizaciones existentes que actualmente no forman parte de su jerarquía de Global Admin Console a la jerarquía de organizaciones.

También puede añadir organizaciones de equipo a la jerarquía de organizaciones. Las organizaciones de equipo no participan en la asignación de productos ni en el resumen del uso de productos, y la administración de organizaciones de equipo en Global Admin Console es limitada. Puede añadirlos a la jerarquía de la organización para realizar un seguimiento de ellos y tener visibilidad de los productos que compran. Las organizaciones de equipo no pueden tener organizaciones secundarias y no tienen muchas de las características de las organizaciones empresariales.

Más información sobre las [limitaciones de la asignación de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Solo puede añadir organizaciones secundarias a organizaciones raíz basadas en el mismo modelo de almacenamiento. Por lo tanto, las organizaciones secundarias basadas en el modelo de almacenamiento de usuario solo se pueden añadir a las organizaciones raíz basadas en el modelo de almacenamiento de usuario. Además, las organizaciones secundarias basadas en el modelo de almacenamiento empresarial solo se pueden agregar a las organizaciones raíz basadas en el modelo de almacenamiento empresarial.

La ficha **[!UICONTROL Asignador de organizaciones]** muestra lo siguiente:

1. Lista desplegable con una lista de posibles organizaciones principales en la que puede agregar una organización secundaria. Son organizaciones de las que es administrador global.
1. Una lista de organizaciones secundarias que se pueden añadir bajo el padre seleccionado en el paso 1. Son organizaciones de las que es administrador del sistema y que no son secundarias de otra organización.

Cuando se agrega una organización a la administración global, los productos de las organizaciones que se agregan mediante el asignador de organizaciones permanecen como compras; los números de [Asignación de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) dejan de acumularse en estas organizaciones.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/) y vaya a **[!UICONTROL Asignador de organizaciones]**.
2. Seleccione una organización principal de la lista desplegable.\
   Son las organizaciones para las que se le añade directamente como administrador global. En la lista desplegable, si no ve una organización que desee utilizar como principal, seleccione una situada en la parte superior de la jerarquía. Una vez completada la operación de asignación de organizaciones, puede usar [Cambiar jerarquía](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization) para mover la nueva organización hacia abajo en el árbol y que tenga el elemento principal que desee usar.
3. Seleccione las organizaciones que desea añadir como hijos de la organización seleccionada en el paso anterior.
4. Seleccione **[!UICONTROL Revisar cambios pendientes]**. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).
5. Después de ejecutar los cambios, puede repetir los pasos anteriores para agregar organizaciones secundarias adicionales a la jerarquía de organizaciones.

Una vez que una organización esté en la jerarquía, puede ajustar las directivas de la organización, los administradores u otras opciones de configuración si navega hasta la ficha **[!UICONTROL Organizaciones]**.
