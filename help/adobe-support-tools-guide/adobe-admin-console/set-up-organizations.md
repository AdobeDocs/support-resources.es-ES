---
title: Administrar jerarquía de organización
description: Descubra cómo los administradores globales pueden administrar la jerarquía de la organización en Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# Administrar jerarquía de organización

Se aplica a la empresa.

Descubra cómo los administradores globales pueden administrar la jerarquía de la organización en Global Admin Console.

Una vez que obtenga acceso de [a [!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access), podrá crear nuevas organizaciones, agregar organizaciones existentes a la jerarquía, eliminar organizaciones y cambiar una organización principal.
[Iniciar sesión en Global Admin Console](https://global-admin-console.adobe.com/)

Una organización es una estructura que se utiliza para administrar productos de Adobe y usuarios. [[!DNL Adobe Admin Console]](https://helpx.adobe.com/es/enterprise/using/admin-console.html) permite a los administradores administrar la implementación y configuración de productos y usuarios en su organización. [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) permite a los administradores globales crear, administrar y eliminar varias organizaciones.

## Crear una organización secundaria

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puedes crear organizaciones secundarias de cualquier organización en la jerarquía y establecer el nombre, el país, los grupos de usuarios, los productos, los perfiles de productos, los administradores y las políticas.

Cuando se crea una nueva organización secundaria, se heredan automáticamente las siguientes organizaciones de la organización principal inmediata:

- Configuración de [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) de la organización (incluidos los bloqueos si existen).
- La lista de administradores del sistema (controlada por la **[!UICONTROL directiva]** Heredar administradores del sistema al crearla[&#128279;](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

Lo siguiente puede impedir que se hereden los administradores del sistema:
   - Falta de [confianza de dominio](https://helpx.adobe.com/enterprise/using/directory-trust.html).
   - Restricciones de tipo de usuario (Añadir políticas de usuario de Adobe ID/ Enterprise ID/ Federated ID). Obtenga información acerca de [detalles de directivas](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Acceso a [[!DNL Federated ID]] o [[!DNL Enterprise ID]] usuarios de dominios a los que tiene acceso la organización principal. Esto hace que los usuarios del dominio principal estén disponibles en la organización secundaria. La herencia del acceso de los usuarios está controlada por **Heredar usuarios de directorios administrados por la organización principal** [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Directiva de uso compartido, directiva de contraseñas y contactos de seguridad (controlados por **Heredar la configuración de uso compartido de recursos cuando se crea la organización secundaria** [directiva](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la pestaña **[!UICONTROL Organizaciones]**, seleccione la organización a la que desee agregar una organización secundaria.
2. Seleccione el icono **[!UICONTROL Agregar+]**.
   ![Agregar organización](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Especifique un **nombre** y el **país** de la organización.\
   El nombre común de la organización debe tener entre 4 y 100 caracteres; el nombre de la ruta no puede superar los 255 caracteres.
   ![Agregar organización secundaria](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. Seleccione **[!UICONTROL Guardar]**.
5. Seleccione **[!UICONTROL Revisar cambios pendientes]** una vez que haya terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminar una organización secundaria

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puedes eliminar organizaciones secundarias. La operación de eliminación no se puede deshacer y la organización raíz no se puede eliminar. Los recursos asignados a la organización eliminada se devuelven a su organización principal. Antes de eliminar una organización, su organización principal se convierte automáticamente en la principal de cualquiera de sus organizaciones secundarias.

Una organización solo se puede eliminar si se cumplen los siguientes criterios:

- No hay cuentas de Sign, compras de Adobe Stock ni repositorios de almacenamiento en la organización.
- No hay dominios reivindicados en la organización.
- No hay productos con instancias en la organización.
- No hay productos de Experience Cloud que puedan incluir instancias en la organización.

>[!WARNING]
>
>Eliminar una organización afecta a los usuarios. Asegúrese de que no se pierda ningún acceso o información cuando se elimine una organización.

1. Inicie sesión en [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Ve a la pestaña **[!UICONTROL Organizaciones]** y selecciona la organización que deseas eliminar.
1. Seleccione el icono **[!UICONTROL Eliminar]**.
   ![Eliminar organización](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. En el cuadro de diálogo **[!UICONTROL Eliminar organización]**, seleccione **[!UICONTROL Aceptar]**.
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Cambiar el nombre de una organización

El nombre de la organización es el nombre oficial de su empresa o institución, que se establece durante la compra. Los usuarios ven este nombre cuando seleccionan un perfil durante el inicio de sesión, especialmente si tienen acceso a productos de Adobe de varias organizaciones o si necesitan elegir entre un perfil profesional y uno personal.

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede editar el nombre de cualquier organización principal o secundaria para ayudar a los usuarios a identificar el perfil correcto al iniciar sesión en [[!DNL Creative Cloud]] productos y servicios.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la ficha **[!UICONTROL Organizaciones]**, seleccione la organización cuyo nombre desea cambiar.
1. Seleccione el icono **[!UICONTROL Editar]**.
   ![Cambiar nombre de organización](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Actualice el nombre de su organización y seleccione **[!UICONTROL Guardar]**.

>[!TIP]
>
>Utilice un nombre de organización claro y reconocible de hasta 255 caracteres para ayudar a los usuarios a seleccionar el perfil correcto. Evite utilizar caracteres especiales y considere la posibilidad de incluir la región, el departamento o el derecho. Además, evite acrónimos poco comunes y nombres vagos o similares en la jerarquía de la organización.
>Utilice un nombre de organización claro y reconocible de hasta 255 caracteres para ayudar a los usuarios a seleccionar el perfil correcto. Evite utilizar caracteres especiales y considere la posibilidad de incluir la región, el departamento o el derecho. Además, evite acrónimos poco comunes y nombres imprecisos o similares en la jerarquía de su organización.

Los cambios se registran en el registro de auditoría, se notifica a todos los usuarios por correo electrónico y el nombre no se puede actualizar de nuevo durante 24 horas. [Obtenga información sobre cómo ver y descargar registros de auditoría](https://helpx.adobe.com/enterprise/global-admin-console/insights.html).

## Cambiar el elemento principal de una organización

Como [[!DNL Global Administrator]](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede crear una organización en la jerarquía de organizaciones con el botón **[!UICONTROL Cambiar jerarquía]**.

Cambiar el elemento principal de una organización tiene el siguiente impacto:

- Al representar una organización, se mueve todo el subárbol enraizado en la organización reparada con él. Los nombres de ruta de la organización reparada y sus elementos secundarios se actualizan para reflejar su nueva ubicación.
- Las [políticas](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) de las organizaciones que se han movido se actualizan para que cualquier bloqueo de las políticas quede en manos de una organización de la nueva jerarquía.
- Cambiar la posición de una organización en la jerarquía puede cambiar los administradores globales de esa organización. Las funciones de administración global se heredan en la jerarquía inferior, de modo que los administradores globales de la nueva organización principal se convierten automáticamente en administradores globales de la organización trasladada. Del mismo modo, los administradores globales pueden perder su función en la organización desplazada si tienen esa función en virtud de ser administradores globales del padre antiguo. Las funciones de administración global heredadas no aparecen en el panel Administradores de la organización.
- La reparación también afecta a los productos disponibles en las organizaciones trasladadas. Cuando sea posible, [las asignaciones de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) se actualizarán para que lleguen a través de la nueva ubicación principal.
- Si las asignaciones de productos no se pueden actualizar para que provengan de la nueva organización principal, los productos se eliminan junto con los perfiles de producto de esos productos. Los usuarios pueden perder el acceso como resultado de esta operación. Para que el producto esté disponible en la nueva ubicación, el antecesor común más cercano de las ubicaciones antigua y nueva debe tener el producto disponible.

>[!WARNING]
>
>Si los productos se eliminan como resultado de la reparación, los usuarios pierden el acceso a esos productos.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la ficha **[!UICONTROL Organizaciones]**, seleccione **[!UICONTROL Cambiar jerarquía]** para habilitar la reparación de las organizaciones.
2. Seleccione **[!UICONTROL OK]** en la pantalla emergente que aparece.
3. Para ascender, arrastre la organización secundaria sobre la organización deseada.
4. Seleccione **[!UICONTROL Guardar]** cuando haya terminado de reparar sus organizaciones.
5. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Una vez completado el trabajo, puede ir a Asignación de productos y [cambiar los valores de concesión](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) para reflejar el cambio en la asignación de recursos de productos.

## Añadir organizaciones existentes mediante el asignador de organizaciones

Como [Administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede agregar organizaciones existentes que actualmente no forman parte de su jerarquía de Global Admin Console a la jerarquía de organizaciones.

También puede añadir organizaciones de equipo a la jerarquía de organizaciones. Las organizaciones de equipo no participan en la asignación de productos ni en el resumen del uso de productos, y la administración de organizaciones de equipo en Global Admin Console es limitada. Puede añadirlos a la jerarquía de la organización para realizar un seguimiento de ellos y tener visibilidad de los productos que compran. Las organizaciones de equipo no pueden tener organizaciones secundarias y no tienen muchas de las características de las organizaciones empresariales.

Más información sobre las [limitaciones de la asignación de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Solo puede añadir organizaciones secundarias a organizaciones raíz basadas en el mismo modelo de almacenamiento. Por lo tanto, las organizaciones secundarias basadas en el modelo de almacenamiento de usuario solo se pueden añadir a las organizaciones raíz basadas en el modelo de almacenamiento de usuario. Además, las organizaciones secundarias basadas en el modelo de almacenamiento empresarial solo se pueden añadir a las organizaciones raíz basadas en el modelo de almacenamiento empresarial.
>Solo puede añadir organizaciones secundarias a organizaciones raíz basadas en el mismo modelo de almacenamiento. Por lo tanto, las organizaciones secundarias basadas en el modelo de almacenamiento de usuarios solo se pueden añadir a las organizaciones raíz basadas en el modelo de almacenamiento de usuarios. Además, las organizaciones secundarias basadas en el modelo de almacenamiento empresarial solo se pueden añadir a las organizaciones raíz basadas en el modelo de almacenamiento empresarial.

La ficha **[!UICONTROL Asignador de organizaciones]** muestra lo siguiente:

1. Un menú desplegable con una lista de posibles organizaciones principales en las que puede añadir una organización secundaria. Estas son las organizaciones de las que es administrador global.
1. Una lista de organizaciones secundarias que se pueden añadir debajo de la organización principal seleccionada en el paso 1. Estas son organizaciones para las que es administrador del sistema y que ya no son secundarias de otra organización.

Cuando se agrega una organización a la administración global, los productos de las organizaciones que se agregan mediante el Asignador de organizaciones permanecen como compras; los números de [Asignación de productos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) dejan de acumularse en estas organizaciones.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/) y vaya a **[!UICONTROL Asignador de organizaciones]**.
2. Seleccione una organización principal en la lista desplegable.\
   Son las organizaciones para las que se le añade directamente como administrador global. En la lista desplegable, si no ve una organización que desee utilizar como principal, seleccione una situada en la parte superior de la jerarquía. Una vez completada la operación de asignación de organizaciones, puede usar [Cambiar jerarquía](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization) para mover la nueva organización hacia abajo en el árbol y que tenga el elemento principal que desee usar.
3. Seleccione las organizaciones que se añadirán como secundarias de la organización seleccionada en el paso anterior.
4. Seleccione **[!UICONTROL Revisar cambios pendientes]**. Luego, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).
5. Después de ejecutar los cambios, puede repetir los pasos anteriores para añadir organizaciones secundarias adicionales a la jerarquía de su organización.

Una vez que una organización esté en la jerarquía, puedes ajustar las políticas de la organización, los administradores u otras configuraciones navegando a la pestaña **[!UICONTROL Organizaciones]**.
