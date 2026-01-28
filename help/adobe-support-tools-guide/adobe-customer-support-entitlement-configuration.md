---
title: Configuración de derechos de asistencia al cliente de Adobe
description: Cómo los clientes de Adobe pueden configurar los derechos de asistencia para habilitar el envío de casos.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 009be3353a4bd690a7cf395e7e95540808058b39
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Derechos de asistencia al cliente de Adobe

Para configurar los derechos de asistencia para su organización, primero agregue o invite al usuario a través de Admin Console.

## Adición de funciones de asignación de derechos de asistencia a una organización

La función de administrador de asistencia es una función no administrativa que tiene acceso a información relacionada con la asistencia. Los administradores de asistencia pueden ver, crear y administrar informes de problemas.

Para agregar o invitar a un administrador:

1. En Admin Console, elija **[!UICONTROL Usuarios]** > **[!UICONTROL Administradores]**.
1. Haga clic en **[!UICONTROL Agregar administrador]**.
1. Introduzca un nombre o una dirección de correo electrónico.

   Puede buscar usuarios existentes o agregar nuevos especificando una dirección de correo electrónico válida y rellenando la información de la pantalla.

   ![Agregar administrador](assets/admin-console-add-admin.png)

1. Haga clic en **[!UICONTROL Siguiente]**. Aparecerá una lista de funciones de administrador.

Para asignar una función de administrador de soporte a un usuario (permitir que un usuario pueda ponerse en contacto con el servicio de asistencia):

1. Seleccione la opción **[!UICONTROL Administrador de asistencia]**.

   ![Editar derechos de administrador](assets/edit-admin-rights.png)

1. Elija una de las dos opciones siguientes:

   * Opción 1: **[!UICONTROL administrador de soporte básico]**. Seleccione esta opción si desea proporcionar al soporte técnico acceso para todas las soluciones (excepto Marketo Engage).
   * Opción 2: **[!UICONTROL Administrador de soporte técnico]**: Seleccione esta opción para el soporte técnico de Marketo Engage. Seleccione las instancias de Marketo Engage que darán acceso a la asistencia al usuario.

   ![Editar derechos de administrador en Marketo](assets/edit-admin-rights-advanced.png)

1. Una vez que haya realizado las selecciones, haga clic en **[!UICONTROL Guardar]**.

El usuario recibe una invitación por correo electrónico en relación con los nuevos privilegios administrativos de `message@adobe.com`.

Los usuarios deben hacer clic en **[!UICONTROL Empezar]** en el correo electrónico para unirse a la organización. Si los nuevos administradores no usan el vínculo **[!UICONTROL Introducción]** en la invitación por correo electrónico, no podrán iniciar sesión en Admin Console.

Como parte del proceso de inicio de sesión, se puede pedir a los usuarios que configuren un perfil de Adobe si aún no lo tienen. Si los usuarios tienen varios perfiles asociados a su dirección de correo electrónico, deben elegir **[!UICONTROL Unirse al equipo]** (si se le solicita) y luego seleccionar el perfil asociado a la nueva organización.

![Confirmación de derechos de administrador](assets/admin-rights-confirmation.png)

Para obtener más información, consulte [editar rol de administrador de empresa](admin-roles.md#add-enterprise-role) instrucciones en la documentación de roles administrativos. Tenga en cuenta que solo un administrador del sistema de su organización puede asignar esta función. Para obtener más información sobre la jerarquía administrativa, visite la documentación de [funciones administrativas](admin-roles.md).
