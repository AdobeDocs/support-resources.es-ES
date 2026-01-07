---
title: Funciones administrativas
description: Con Adobe Admin Console, las organizaciones pueden definir una jerarquía administrativa flexible que permita una administración precisa del acceso y el uso de los productos de Adobe.
solution: Admin Console
source-git-commit: a96f8be10d63d4f1f40738d533147c22de9b5482
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# Funciones administrativas

Con Adobe Admin Console, las organizaciones pueden definir una jerarquía administrativa flexible que permita una administración precisa del acceso y el uso de los productos de Adobe. Uno o más administradores del sistema, aprovisionados durante el proceso de incorporación a la empresa, se sientan en la parte superior de la jerarquía. Estos administradores del sistema pueden delegar responsabilidades a otros administradores, al tiempo que conservan el control general.

Las funciones administrativas proporcionan a las empresas las siguientes ventajas clave:

* Descentralización controlada de las responsabilidades administrativas
* Vista rápida de asignaciones de productos, por usuario y por producto
* Funcionalidad para asignar cuotas a administradores de productos

## Jerarquía administrativa

Se aplica a: clientes empresariales de Adobe.

La jerarquía administrativa se puede utilizar para adaptarse a los requisitos únicos de su empresa. Por ejemplo, una empresa puede designar diferentes administradores para que administren los derechos de las ofertas de Adobe Creative Cloud y Adobe Marketing Cloud. Como alternativa, una empresa puede tener distintos administradores para administrar los derechos de los usuarios que pertenecen a diferentes unidades de negocio.

>[!NOTE]
>
>La jerarquía administrativa no se aplica a los equipos y clientes. Los clientes de Teams tienen un único rol de **administrador del sistema**. El propietario del contrato (_anteriormente denominado **administrador principal**&#x200B;_) es el administrador del sistema con acceso a los detalles del contrato y al historial de facturación. Si usted es el propietario actual del contrato, puede nombrar a un administrador del sistema existente (_ anteriormente denominado **administrador secundario**&#x200B;_) como propietario del contrato.

![imagen de administrador](assets/storage_admin.png)

_Jerarquía de funciones de administrador_

| Función | Descripción |
|--- |--- |
| **Administrador del sistema** | Superusuario de la organización; con permiso para realizar todas las tareas administrativas en Admin Console.<br>Además, tiene permisos para delegar la siguiente funcionalidad administrativa a otros usuarios: administrador de productos, administrador de perfiles de productos, administrador de grupos de usuarios, administrador de implementación y administrador de soporte técnico. |
| **Administrador de productos** | Administra los productos asignados a ese administrador y todas las funciones administrativas asociadas, que incluyen:<ul><li>Creación de perfiles de producto</li><li>Agregar usuarios y grupos de usuarios a la organización, pero no eliminarlos</li><li>Agregar o quitar usuarios y grupos de usuarios de perfiles de producto</li><li>Añadir o quitar administradores de perfil de producto de perfiles de producto</li><li>Agregar o quitar otros administradores de productos del producto</li><li>Agregar o quitar administradores de grupo de los grupos</li></ul> |
| **Administrador de perfil de producto** | Administra las descripciones de perfil de producto asignadas a dicho administrador y todas las funciones administrativas asociadas, que incluyen:<ul><li>Agregar usuarios y grupos de usuarios a la organización, pero no eliminarlos</li><li>Agregar o quitar usuarios y grupos de usuarios de perfiles de producto</li><li>Asignar o revocar permisos de producto a usuarios y grupos de usuarios desde perfiles de producto</li><li>Administrar las funciones de producto de los usuarios y grupos de usuarios para los perfiles de producto |
| **Administrador del grupo de usuarios** | Administra las descripciones de grupos de usuarios asignadas a dicho administrador y todas las funciones administrativas asociadas, que incluyen:<ul><li>Agregar o quitar usuarios de grupos</li><li>Adición o eliminación de administradores de grupos de usuarios de grupos |
| **Administrador de implementación** | Crea, administra e implementa paquetes de software y actualizaciones para los usuarios finales. |
| **Administrador de asistencia** | Función no administrativa que tiene acceso a información relacionada con la asistencia, como informes de problemas notificados por el cliente. |
| **Administrador de almacenamiento** | Gestiona la administración de almacenamiento de la organización. El administrador puede ver el consumo de almacenamiento de los usuarios activos e inactivos y transferir contenido a otros destinatarios. |

Para obtener una lista detallada de permisos y privilegios para cada rol de administrador, consulte [Permisos](#enterprise-admins-permissions-matrix).

## Agregar un rol de administrador de empresa {#add-enterprise-role}

Se aplica a: clientes empresariales de Adobe.

Como administrador, puede asignar un rol de administrador a otros usuarios, otorgándoles los mismos privilegios que usted tiene, o privilegios para un rol bajo su rol de administrador en la jerarquía como se describe [arriba](#administrative-hierarchy). Por ejemplo, como administrador de productos puede otorgar privilegios de administrador de productos o privilegios de administrador de perfil de productos a un usuario, pero no privilegios de administrador de implementación. Para obtener los permisos de Admin Console, consulte la [Matriz de permisos](#enterprise-admins-permissions-matrix).

Para agregar o invitar a un administrador:

1. En **[[!UICONTROL Adobe Admin Console]](https://adminconsole.adobe.com/)**, elija **[!UICONTROL Usuarios]** > **[!UICONTROL Administradores]**.

   También puede ir al producto, al perfil de producto o al grupo de usuarios correspondiente y navegar a la pestaña **[!UICONTROL Administradores]**.

1. Haga clic en **[!UICONTROL Agregar administrador]**.
1. Introduzca un nombre o una dirección de correo electrónico. Puede buscar usuarios existentes o agregar nuevos usuarios especificando una dirección de correo electrónico válida y rellenando la información de la pantalla.
1. Haga clic en **[!UICONTROL Siguiente]**. Aparecerá una lista de funciones de administrador.

   >[!NOTE]
   >
   >* Las opciones de esta pantalla dependen de su cuenta y de la función de administrador. Puede otorgar los mismos privilegios que tiene o privilegios para un rol suyo en la jerarquía.
   >* Como administrador del sistema de un equipo, solo puede asignar un rol de administrador: administrador del sistema.

1. Seleccione uno o varios roles de administrador.
1. Para tipos de administradores como administrador de productos, administrador de perfiles de producto y administrador de grupos de usuarios, seleccione los productos, perfiles y grupos específicos respectivamente.

   >[!NOTE]
   >
   >Para un Administrador de perfiles de producto, puede incluir perfiles de más de un producto.

   ![agregar administrador](assets/add-admin.png)

1. Revise los roles de administrador asignados al usuario y haga clic en **Guardar**.

El usuario recibe una invitación por correo electrónico en relación con los nuevos privilegios administrativos de `message@adobe.com`.

Los usuarios deben hacer clic en **[!UICONTROL Empezar]** en el correo electrónico para unirse a la organización. Si los nuevos administradores no usan el vínculo **[!UICONTROL Introducción]** en la invitación por correo electrónico, no podrán iniciar sesión en Admin Console.

Como parte del proceso de inicio de sesión, se puede pedir a los usuarios que configuren un perfil de Adobe si aún no lo tienen. Si los usuarios tienen varios perfiles asociados a su dirección de correo electrónico, deben elegir &quot;Unirse al equipo&quot; (si se le solicita) y luego seleccionar el perfil asociado a la nueva organización.

![imagen de derechos de administrador](assets/admin-get-started-email.png)

## Agregar un administrador de equipos {#add-admin-teams}

Se aplica a: Adobe reúne a clientes.

Como administrador, puede asignar la función de administrador del sistema a otros usuarios, otorgándoles los mismos privilegios que tiene usted.

Para agregar o invitar a un administrador del sistema:

1. En **[!UICONTROL Adobe Admin Console]**, elija **[!UICONTROL Usuarios]** > **[!UICONTROL Administradores]**.

   Se muestra una lista de los administradores existentes.

1. Haga clic en **[!UICONTROL Agregar administrador]**.

   Se muestra la pantalla **[!UICONTROL Agregar un administrador]**.

1. Introduzca un nombre o una dirección de correo electrónico. Puede buscar usuarios existentes o agregar nuevos usuarios especificando una dirección de correo electrónico válida y rellenando la información de la pantalla.

   De forma predeterminada, la opción Administrador del sistema está seleccionada.

1. Haga clic en **[!UICONTROL Guardar]**.

![imagen de administrador de equipos](assets/teams-admin.png)

Dado que todos los usuarios de una organización de equipos son usuarios de ID empresarial, reciben una invitación por correo electrónico con respecto a los nuevos privilegios administrativos de `message@adobe.com`.
Los usuarios deben hacer clic en Comenzar en el correo electrónico para unirse a la organización.

Como parte del proceso de inicio de sesión, se puede pedir a los usuarios que configuren un perfil de Adobe si aún no lo tienen. Si los usuarios tienen varios perfiles asociados a su dirección de correo electrónico, deben elegir &quot;Unirse al equipo&quot; (si se le solicita) y luego seleccionar el perfil asociado a la nueva organización.

![imagen de derechos de administrador](assets/admin-get-started-email.png)

## Editar rol de administrador de empresa

Se aplica a: clientes empresariales de Adobe.

Como administrador, puede editar la función de administrador a otros administradores que estén por debajo de usted en la jerarquía administrativa. Por ejemplo, puede eliminar los privilegios de administrador de otros administradores.

Para editar los roles de administrador:

1. En **[!UICONTROL Adobe Admin Console]**, elija **[!UICONTROL Usuarios]** > **[!UICONTROL Administradores]**. Se muestra la lista de administradores existentes.

   También puede ir al producto, al perfil de producto o al grupo de usuarios correspondiente y navegar a la pestaña **[!UICONTROL Administradores]**.

1. Haga clic en el nombre del administrador que desea editar.
1. En **[!UICONTROL Detalles del usuario]**, haga clic en ![icono](assets/one-console-ellipses.png) para la sección **Derechos administrativos** y elija **[!UICONTROL Editar derechos de administrador]**.

   ![editar derechos de administrador](assets/admin-rights-section.png)

1. Edite los derechos administrativos y guarde los cambios.

## Editar rol de administrador de equipos

Se aplica a: Adobe reúne a clientes.

Como administrador del sistema de equipos, puede eliminar los privilegios de administrador del sistema de otros administradores.

Para revocar los privilegios de administrador del sistema:

1. En **[!UICONTROL Adobe Admin Console]**, elija **[!UICONTROL Usuarios]** > **[!UICONTROL Administradores]**.

   Se muestra la lista de administradores existentes.

1. En **[!UICONTROL Detalles del usuario]**, haga clic en ![icono](assets/one-console-ellipses.png) a la derecha de la sección **[!UICONTROL Derechos administrativos]** y elija **[!UICONTROL Editar derechos de administrador]**.

   ![editar derechos de administrador](assets/admin-rights-section.png)

1. Edite los derechos administrativos y guarde los cambios.

## Eliminar un administrador

Se aplica a: Adobe reúne a clientes empresariales.

Para revocar los permisos de administrador, seleccione un usuario y haga clic en **[!UICONTROL Quitar administrador]**.

![quitar imagen de administrador](assets/remove-admin.png)

>[!NOTE]
>
>Al eliminar un administrador no se elimina el usuario de Admin Console, sino que solo se eliminan los privilegios asociados con el rol de administrador.

## Matriz de permisos de Enterprise Admin

Se aplica a: clientes empresariales de Adobe.

En la tabla siguiente se enumeran todos los permisos para los distintos tipos de administradores, clasificados por las siguientes áreas de funcionalidad:

### Administración de identidad

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Añadir dominio (solicitar/reclamar un dominio) | ✔ | |
| Ver lista de dominios y dominios | ✔ | |
| Administrar claves de cifrado de dominio | ✔ | |
| Administrar directiva de contraseñas de organización predeterminada | ✔ | |
| Ver directiva de contraseñas de organización predeterminada | ✔ | |

### Administración de usuarios

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Añadir usuario a la organización | ✔ | |
| Eliminar usuario de la organización | ✔ | |
| Ver detalles y listado de usuarios | ✔ | |
| Editar perfil de usuario | ✔ | |
| Añadir perfil de producto al usuario o grupo | ✔ | |
| Quitar perfil de producto al usuario o grupo | ✔ | |
| Añadir el perfil de producto a varios usuarios | ✔ | |
| Ver perfiles de producto de un usuario | ✔ | |
| Ver lista de usuarios de productos | ✔ | |
| Adición masiva de usuarios a la organización | ✔ | |

### Administración del administrador

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Concesión de administrador de organización a un usuario | ✔ | |
| Revocar administrador de organización de un usuario | ✔ | |
| Conceder el administrador de licencias de producto a un usuario | ✔ | |
| Revocar administrador de licencias de producto de un usuario | ✔ | |
| Conceder administrador de implementación a un usuario | ✔ | |
| Revocar administrador de implementación de un usuario | ✔ | |
| Conceder administrador de grupo de usuarios a un usuario | ✔ | |
| Revocar administrador de grupo de usuarios de un usuario | ✔ | |
| Conceder el administrador del propietario del producto a un usuario | ✔ | |
| Revocar administrador de propietario de producto de un usuario | ✔ | |

### Administración de configuración de licencias de producto

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Conceder derecho de producto a la organización | | |
| Eliminar el derecho del producto de la organización | | |
| Ver el número total de licencias propiedad de la organización | ✔ | |
| Ver productos y familias de productos disponibles | ✔ | |
| Editar datos/descripciones de licencias de productos | ✔ | |
| Aprovisionar licencia de producto a un usuario | ✔ | |
| Desaprovisionar la licencia de producto de un usuario | ✔ | |
| Añadir nueva configuración de licencia del producto | ✔ | |
| Editar configuración del servicio de licencias del producto | ✔ | |
| Eliminar configuración del servicio de licencias del producto | ✔ | |
| Eliminar el acceso al producto de un usuario (eliminar de todas las configuraciones) | ✔ | |

### Administración de almacenamiento

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Ver carpetas de usuario activas e inactivas | ✔ | |
| Eliminar carpetas de usuario inactivas y transferir contenido | ✔ | |

### Implementación

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Pestaña Ver/usar paquetes | ✔ | |

### Asistencia

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Ver ficha de asistencia | ✔ | |
| Administración de casos de asistencia | ✔ | ✔ |

### Administración de grupos de usuarios

| Permiso | Administrador del sistema | Administrador de soporte |
|--- |--- |--- |
| Crear grupo de usuarios | ✔ | |
| Quitar grupo de usuarios | ✔ | |
| Añadir usuario al grupo de usuarios | ✔ | |
| Quitar usuario del grupo de usuarios | ✔ | |
| Asignar un grupo de usuarios a una licencia de producto | ✔ | |
| Quitar grupo de usuarios de la licencia del producto | ✔ | |
| Ver miembros del grupo de usuarios | ✔ | ✔ |
| Ver lista de grupos de usuarios | ✔ | ✔ |