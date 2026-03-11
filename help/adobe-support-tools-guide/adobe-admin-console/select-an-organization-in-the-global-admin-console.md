---
title: Seleccione una organización en Global Admin Console
description: Obtenga información sobre cómo elegir una organización para editarla en Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 0bc0dbd8c7040e0be7e7bd45945edb0fb24cb7cc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 1%

---


# Seleccione una organización en Global Admin Console

Obtenga información sobre cómo elegir una organización para editarla en Global Admin Console.

>[!NOTE]
>
>Una vez que tenga acceso a [Global Admin Console](https://helpx.adobe.com/es/enterprise/global-admin-console/adopt-global-administration.html#request-access), podrá empezar seleccionando una organización para ver y administrar el nombre de la organización, los grupos de usuarios, los perfiles de producto, los administradores y las directivas de la organización. Para iniciar sesión en Global Admin Console, [haga clic aquí](https://global-admin-console.adobe.com/).

Global Admin Console actúa como centro de administración central de una organización para los recursos de Adobe. Los administradores globales pueden:

- Crear organizaciones secundarias dentro de su organización
- Asignar administradores del sistema para administrarlos
- Distribuya recursos a las organizaciones secundarias para su administración y asignarlos a los usuarios de esas organizaciones

>[!NOTE]
>
> Los usuarios y administradores de una organización no tienen visibilidad de los usuarios, el almacenamiento u otros recursos fuera de su organización.

## Seleccione su organización

Las organizaciones enumeradas en la lista desplegable **[!UICONTROL selector de organización]** son aquellas de las que usted es administrador global, es decir, que se le añadió a la lista de administradores de esa organización con una función de administrador global o visualizador global. Usted es implícitamente un administrador global (o un visor global) de todas las organizaciones por debajo de ese punto en la jerarquía, pero esas organizaciones no están en la lista del [!UICONTROL selector de organizaciones].

![Selector de organización](/help/adobe-support-tools-guide/assets/org-picker.png)

Si desea que aparezcan en la lista, añádase como administrador global a las organizaciones que desea que aparezcan en ella. Cuando selecciona una organización en el [!UICONTROL selector de organización], sus permisos administrativos se basan en ser administrador global de la organización seleccionada. También puede aparecer como administrador global de una organización principal superior en el árbol, lo que podría proporcionarle más permisos. Debe seleccionar esa organización de nivel superior para obtener los permisos adicionales.

En Global Admin Console, después de seleccionar una organización del [!UICONTROL árbol de jerarquías], puede empezar a editar información para una organización en particular.

**Las ediciones pueden afectar a:**

- Nombre de la organización
- Grupos de usuarios
- Perfiles de producto
- Administradores
- Políticas de organización

**Las ediciones no pueden afectar:**

- Usuarios (excepto para la eliminación de grupos o perfiles de producto)
- Adición de usuarios (excepto para administradores)

Cuando se selecciona una organización del árbol de jerarquías, se muestra la siguiente información:

- Nombre de la organización
- Región
- Cantidad de usuarios
- Lista de productos
- Perfiles de producto
- Grupos de usuarios
- Administradores
- Dominios reclamados
- Valores de política de la organización

Para ver o editar productos, grupos de usuarios, administradores, dominios, directivas o plantillas de directivas, seleccione la ficha adecuada. Puede usar el campo [!UICONTROL search] en la mayoría de los casos para localizar un elemento específico dentro de la pestaña.

![Editar una organización](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Los administradores añadidos o eliminados de una organización recibirán una notificación por correo electrónico. Ciertos cambios de directiva en una organización dan como resultado una notificación en [!DNL Admin Console] de esa organización.

## Obtenga información sobre las restricciones y las condiciones necesarias

- La profundidad máxima para anidar organizaciones es de cinco. Por lo tanto, se permite a/b/c/d/e, pero a/b/c/d/e/f es un error. Por ejemplo, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London está permitido, pero Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair es un error.

- La longitud máxima del nombre de ruta (incluidas todas las organizaciones) es de 255 caracteres (incluyendo &quot;/&quot;). La longitud máxima de un solo nombre de organización es de entre 4 y 100 caracteres.

- El nombre de la ruta de la organización es único, pero el nombre simple solo es único entre sus hermanos. Puede haber organizaciones con el mismo nombre simple en cualquier parte de la jerarquía organizativa.

- Solo puede ver la lista de dominios vinculados a la organización seleccionada mediante Global Admin Console. Si es administrador de sistemas de la organización seleccionada, seleccione **[!UICONTROL Abrir en Admin Console]** para [administrar dominios](https://helpx.adobe.com/es/enterprise/using/manage-domains-directories.html). Para comprender la información mostrada en la ficha Dominios, vea [exportar e importar esquemas](https://helpx.adobe.com/es/enterprise/global-admin-console/export-and-import-data.html#export-and-import-schemas).

- IE 11 no es compatible con el acceso de administración global. Utilice un explorador diferente o una versión más reciente del explorador IE.
