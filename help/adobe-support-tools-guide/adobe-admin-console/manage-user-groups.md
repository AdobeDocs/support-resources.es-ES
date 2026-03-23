---
title: Administrar grupos de usuarios en Global Admin Console
description: Obtenga información sobre cómo crear, compartir, editar y eliminar grupos de usuarios en Global Admin Console para optimizar la administración de usuarios en todas las organizaciones.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 1e20362a-0974-4b83-a083-9edaab04c255
source-git-commit: 265c341935b3257e5731a129c42411151645ae89
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# Administrar grupos de usuarios en Global Admin Console

Cree, administre y comparta grupos de usuarios en Global Admin Console para optimizar la administración de usuarios mediante la agrupación de usuarios con los mismos permisos, lo que ahorra tiempo y garantiza la coherencia.

En [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html), seleccione una organización y vaya a **[!UICONTROL Grupos de usuarios]**. Comparta grupos de varias organizaciones mediante una única fuente de administración de usuarios para sincronizar usuarios y grupos.

[Iniciar sesión en Global Admin Console](https://global-admin-console.adobe.com)



## Crear grupos de usuarios

Puede [crear grupos de usuarios](https://helpx.adobe.com/es/enterprise/using/user-groups.html) individualmente, de forma masiva o [sincronizarlos directamente desde un Azure AD](https://helpx.adobe.com/enterprise/using/add-azure-sync.html) establecido a un directorio federado en Adobe Admin Console. En Global Admin Console, puede definir grupos de usuarios con perfiles de producto relevantes asignados, a los que los administradores de grupos de usuarios pueden añadir posteriormente usuarios mediante Admin Console.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización para editar y, a continuación, vaya a la pestaña **[!UICONTROL Grupos de usuarios]**.

2. Seleccione **[!UICONTROL Agregar grupo de usuarios]**.

   ![Ficha Organizaciones de Global Admin Console con la ficha Grupos de usuarios seleccionada.](assets/add-user-group.png "Agregar grupo de usuarios")

   _Agregue grupos de usuarios a una organización para optimizar la administración de usuarios._

3. Escriba lo siguiente en el cuadro de diálogo **[!UICONTROL Agregar grupo de usuarios]** que aparece:
   - **[!UICONTROL Nombre]**: especifique un nombre para el grupo de usuarios.
   - **[!UICONTROL Perfiles de producto]**: si desea conceder acceso al producto a los miembros actuales o futuros del grupo de usuarios, haga clic en la flecha desplegable para seleccionar un perfil de producto de la lista o escriba el nombre del perfil de producto y selecciónelo en la lista desplegable que se muestra. Si desea agregar un perfil de producto que aún no se haya creado, primero debe hacerlo usando la ficha [Perfiles de producto](https://helpx.adobe.com/enterprise/using/global-admin-edit-organizations.html#profiles).
   - **[!UICONTROL Administradores]**: haga clic en la flecha desplegable para seleccionar un administrador de la lista o escriba la dirección de correo electrónico del administrador y selecciónelo en la lista desplegable que se muestra. Si desea agregar un administrador nuevo que aún no se haya creado, primero debe crearlo con la ficha [Administradores](#share-user-groups).

   Los perfiles de producto que especifique se asignarán al grupo de usuarios, y los administradores que especifique se convertirán en administradores del grupo de usuarios. Los administradores de grupos de usuarios pueden utilizar Adobe Admin Console de la organización correspondiente para administrar el grupo.

4. Seleccione **[!UICONTROL Guardar]**.

5. Seleccione **[!UICONTROL Revisar cambios pendientes]** para revisar las actualizaciones. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Los administradores globales pueden [asignar perfiles de producto y administradores de grupos de usuarios](#review-user-groups) a los grupos de usuarios que usan Global Admin Console. Con Adobe Admin Console, los administradores del sistema y de grupos de usuarios pueden [agregar usuarios y asignar administradores y perfiles de producto](https://helpx.adobe.com/es/enterprise/using/user-groups.html) al grupo de usuarios.



## Compartir grupos de usuarios

La proyección de grupos le permite sincronizar grupos de usuarios y sus usuarios asociados desde una sola fuente de administración a varias Admin Consoles. Los administradores globales pueden compartir grupos de usuarios con descendientes jerárquicos de la organización de origen, trabajando hacia abajo, no hacia arriba o de lado a lado.

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización y vaya a la pestaña **[!UICONTROL Grupos de usuarios]**.

2. Seleccione las casillas de verificación de los grupos de usuarios que desee compartir.

   Los grupos pueden quedar deshabilitados para compartir en los siguientes casos:
   - El grupo de usuarios se comparte desde otra organización. Para compartir o editar el grupo, seleccione la organización que lo posee en la jerarquía de organizaciones.
   - La organización no está usando [almacenamiento de Adobe para empresas](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html), que se está implementando globalmente por fases.
   - La directiva de organización está deshabilitada. Vaya a la ficha **[!UICONTROL Directivas]** para activar la directiva **[!UICONTROL Administrar grupos de usuarios compartidos]**.
   - La organización no tiene ninguna organización secundaria con la que compartir grupos de usuarios.

3. Seleccione **[!UICONTROL Compartir grupo de usuarios]**.

4. <a id="review-user-groups"></a>Revise los grupos de usuarios para compartirlos con otras organizaciones. Si también es administrador de sistemas de la organización seleccionada, seleccione **[!UICONTROL Abrir en Admin Console]** Icono <img src="assets/icon-open-in-admin-console.png" alt="Icono Abrir en Admin Console" width="14" height="14"> para revisar la lista de miembros del grupo de usuarios en Adobe Admin Console.

   >[!NOTE]
   >
   >Para evitar conflictos, asegúrese de que las organizaciones con las que planea compartir grupos de usuarios no tengan ya grupos con el mismo nombre.

5. Seleccione **[!UICONTROL Siguiente]**.

6. Seleccione las organizaciones con las que compartir grupos de usuarios y seleccione **[!UICONTROL Siguiente]**.

7. Si no hay conflictos, seleccione **[!UICONTROL Compartir grupos de usuarios]**.

   Si hay conflictos (donde existen grupos de usuarios con el mismo nombre en la organización de destino), elija una de las siguientes opciones y, a continuación, seleccione **[!UICONTROL Compartir grupos de usuarios]**:
   - **[!UICONTROL Omitir (predeterminado)]**: omita los grupos de las organizaciones de destino con el mismo nombre.
   - **[!UICONTROL Agregar solamente]**: combine los grupos de usuarios agregando nuevos usuarios a los grupos de usuarios existentes sin quitar ningún usuario.
   - **[!UICONTROL Grupo espejo]**: ajuste los grupos de la organización de destino para que coincidan con el grupo compartido agregando o quitando usuarios.

8. Seleccione **[!UICONTROL Revisar cambios pendientes]** para revisar las actualizaciones. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   Los eventos de proyección de grupo se registran para su referencia. Aprenda a [ver y descargar registros de auditoría](https://helpx.adobe.com/enterprise/global-admin-console/insights.html).


Cuando comparte un grupo de usuarios, el grupo y sus usuarios se añaden a la organización de destino. Sin embargo, el *grupo de usuarios de origen controla* los grupos de usuarios compartidos y sus usuarios. Las asignaciones de administrador y perfil de producto están *no* sincronizadas entre organizaciones.

Los cambios en el nombre del grupo de usuarios proyectado o en los usuarios asociados en el grupo de usuarios de origen se actualizan automáticamente en la organización de destino. Aunque el grupo de usuarios compartidos no se puede administrar directamente, un administrador de la organización de destino puede asignar perfiles de producto a un grupo compartido, lo que proporciona acceso de licencia a los usuarios del grupo.



## Revocar acceso a grupos compartidos

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización y vaya a la pestaña **[!UICONTROL Grupos de usuarios]**.

2. Seleccione **[!UICONTROL Administrar acceso compartido]** para el grupo de usuarios correspondiente.

3. Seleccione las organizaciones desde las que desea revocar el acceso.

4. Seleccione **[!UICONTROL Revocar acceso]**.

5. Al revocar el acceso, puede optar por eliminar el grupo de usuarios y los usuarios o dejar una copia en las organizaciones de destino:
   - Al eliminar, el grupo de usuarios se elimina de las organizaciones de destino. Los usuarios que no son miembros de otros grupos compartidos se eliminan de las organizaciones de destino y pierden el acceso a todos los productos, servicios y recursos.
   - Al dejar una copia, el grupo de usuarios y los usuarios permanecen en las organizaciones de destino manteniendo intactas todas las asignaciones. Sin embargo, el grupo de usuarios ya no se sincronizará y los administradores de las organizaciones de destino pueden administrarlo.

6. Seleccione **[!UICONTROL Revocar acceso]**.

7. Seleccione **[!UICONTROL Revisar cambios pendientes]** para revisar las actualizaciones. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).



## Editar grupos de usuarios

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización y vaya a la pestaña **[!UICONTROL Grupos de usuarios]**.

2. Seleccione **[!UICONTROL Más opciones]** <img src="assets/icon-more-options.png" alt="Icono Más opciones" width="14" height="14" style="vertical-align:middle"> icono para el grupo de usuarios correspondiente y seleccione **[!UICONTROL Editar grupo de usuarios]**.

   >[!NOTE]
   >
   >No puede editar grupos de usuarios que la organización seleccionada no posee.

   ![Una organización seleccionada con la opción Editar grupo de usuarios resaltada en la ficha Grupos de usuarios.](assets/edit-user-group.png "Editar grupo de usuarios")

   _Edite los grupos de usuarios para actualizar el nombre del grupo de usuarios, los perfiles de producto o los administradores._

3. Actualice el nombre del grupo de usuarios, los perfiles de producto o los administradores. A continuación, seleccione **[!UICONTROL Guardar]**.

   >[!NOTE]
   >
   >En el asistente **[!UICONTROL Editar grupo de usuarios]**, puede asignar roles de administrador solamente a los usuarios que ya tienen un rol de administrador asignado en esta organización. Aprenda a [agregar nuevos administradores](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators).

4. Seleccione **[!UICONTROL Revisar cambios pendientes]** para revisar las actualizaciones. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Si cambia el nombre de un grupo de usuarios compartidos, los cambios se actualizan automáticamente en la organización de destino.



## Eliminar grupos de usuarios

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/), seleccione una organización y vaya a la pestaña **[!UICONTROL Grupos de usuarios]**.

2. Seleccione **[!UICONTROL Más opciones]** <img src="assets/icon-more-options.png" alt="Icono Más opciones" width="14" height="14" style="vertical-align:middle"> icono para el grupo de usuarios correspondiente y seleccione **[!UICONTROL Eliminar grupo de usuarios]**.

   >[!NOTE]
   >
   >No puede eliminar grupos de usuarios que la organización seleccionada no posee.

3. Seleccione **[!UICONTROL Ok]** en el cuadro de diálogo que aparece.

   >[!CAUTION]
   >
   >Eliminar un grupo de usuarios puede afectar a los usuarios. Asegúrese de que no haya acceso ni información que se perderá cuando se elimine el grupo de usuarios.

4. Después de editar las organizaciones, seleccione **[!UICONTROL Revisar cambios pendientes]** para revisarlos. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).
