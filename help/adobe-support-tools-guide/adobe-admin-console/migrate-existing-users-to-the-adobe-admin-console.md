---
title: Migración de los usuarios existentes a Adobe Admin Console
description: Directrices para organizaciones que utilizan licencias de suscripción de Adobe y necesitan migrar a usuarios existentes en Admin Console a un programa de compra o tipo de licencia diferente.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: aace5ed8-65a6-4cff-8542-bc50e9c765b7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# Migración de los usuarios existentes a Adobe Admin Console

Se aplica a empresas y equipos.

Este documento es para organizaciones con licencias existentes de Creative Cloud, Document Cloud y Acrobat a través de un contrato de licencia Enterprise Term License Agreement (ETLA) o una suscripción Value Incentive Plan (VIP) que estén migrando a un programa de compra o tipo de licencia diferente.

>[!NOTE]
>
>Si se encuentra en Norteamérica y necesita ayuda con la renovación anual del contrato de Adobe VIP de su administrador de cuentas, envíe un mensaje de correo electrónico a **renewalhelp@adobe.com** y nos pondremos en contacto con usted en breve.

Para evitar que se produzca un lapso en el acceso a los productos por parte del usuario final, asigne licencias en Adobe Admin Console antes de que finalice el periodo de suscripción de VIP.

* Para los clientes de ETLA, espere al menos 30 días de superposición de productos. Complete la migración antes de la fecha de aniversario para que los usuarios mantengan el acceso a las aplicaciones y los servicios de Adobe. Para obtener detalles sobre la caducidad de contratos de ETLA, consulte [Fases de caducidad automatizadas para contratos de ETLA](https://helpx.adobe.com/enterprise/using/contract-expiry.html).
* Para los clientes de VIP, compre licencias antes de la fecha de aniversario y asígnelas antes de que se cierre la ventana de renovación durante el periodo actual de VIP.
* Los clientes de CLP o TLP pueden migrar desde Acrobat serializado o Creative Suite a licencias de usuario designado según las instrucciones de migración de [Licencias](https://helpx.adobe.com/enterprise/using/licensing.html).

>[!NOTE]
>
>Si el tipo de licencia de su organización cambia, los usuarios finales deben cerrar la sesión de cualquier producto o servicio de Adobe y volver a iniciarla con las mismas credenciales.
>
>Para productos de escritorio como Photoshop, Acrobat y Illustrator, utilice las opciones Cerrar sesión y Iniciar sesión en el menú Ayuda. En Adobe.com, utilice el icono de la esquina superior derecha para cerrar la sesión y, a continuación, vuelva a iniciarla.

## Asignación rápida de licencias (de VIP a VIP)

Los miembros actuales de VIP que hayan adquirido Creative Cloud para empresas o Acrobat (para empresas) a través de VIP pueden asignar licencias rápidamente durante su período de renovación mediante la Asignación rápida de licencias. Los clientes aptos cumplen criterios como los siguientes.

* Los productos son los mismos

   1. La ventana de renovación está abierta (30 días antes o después de la fecha de aniversario del acuerdo de VIP).
   2. Los productos empresariales del pedido son SKU nuevas equivalentes a las versiones de equipo del término actual.
   3. La cantidad del pedido de licencia de empresa es mayor o igual que la cantidad de licencia de equipo existente.

* Los productos son de mayor valor

   1. La ventana de renovación está abierta.
   2. Los productos empresariales del pedido son SKU nuevas que son productos de mayor valor que los productos de equipo del plazo actual.
   3. La cantidad del pedido de licencia de empresa es mayor o igual que la cantidad de licencia de equipo existente.

* La asignación rápida de licencias no está disponible cuando

   * La cantidad de licencias de empresa en el pedido es menor que el número de licencias de equipo existentes.
   * El pedido es para productos de empresa de mayor valor, pero la cantidad de licencia de empresa solicitada es menor que la cantidad de licencia de equipo existente.
   * El pedido combina productos de equipo y empresariales, independientemente de la cantidad.
   * El cliente ya compró productos de equipo y empresariales antes del período de renovación.
   * Los SKU de renovación de empresa se utilizan para el nuevo pedido de empresa.
   * El pedido de producto empresarial es para un número de acuerdo de VIP diferente.
   * Los productos de equipo actuales incluyen artículos que no tienen versiones de empresa.

Después de que Adobe procese su pedido de compra empresarial, recibirá un correo electrónico de confirmación con instrucciones, incluido el día en que debe transferir usuarios de licencias de equipo a licencias de empresa en Admin Console antes de que pierdan el acceso.

En Admin Console, se le pedirá que asigne licencias mediante Asignación rápida de licencias:

1. Confirme el número de licencias para la asignación.

   ![Transferir licencias](assets/migrate-transfer-licenses.png)

2. Confirme que las licencias de producto de equipo que se están quitando coinciden con las licencias de empresa que se están asignando.

3. Recibirá un correo electrónico cuando se complete el proceso.

   ![Confirmación de asignación de licencia](assets/migrate-license-assignment.png)

Descargue el [informe de resultados](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) en Admin Console para confirmar que se asignaron todas las licencias. Si termina antes de la fecha que figura en el correo electrónico de confirmación, los usuarios finales no deben experimentar ningún lapso de servicio.

Programe una llamada de incorporación de 1:1 con un especialista en incorporación de Adobe (si aún no lo ha hecho) para obtener más información sobre Admin Console, incluidas las [funciones administrativas](https://helpx.adobe.com/enterprise/using/admin-roles.html) y [Identity](https://helpx.adobe.com/es/enterprise/using/identity.html).

>[!NOTE]
>
>La asignación rápida de licencias no migra a los usuarios con invitaciones pendientes en Team Admin Console.

## Asignación masiva de licencias (de VIP a VIP)

Asigne licencias con una operación masiva mediante una plantilla CSV desde Admin Console. Utilice este método cuando:

* Es cliente de VIP que no cumple los requisitos de asignación rápida de licencias o
* Debe asignar licencias fuera de la ventana de renovación.

1. Después de tener acceso a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) y de agregar las licencias, ve a **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios]**.
2. Haga clic en ![Más opciones en el menú](assets/migrate-more-options.png) en la esquina superior derecha de la página de **[!UICONTROL Usuarios]** y, a continuación, elija **[!UICONTROL Editar detalles del usuario con CSV]**.
3. En el diálogo **[!UICONTROL Editar usuarios por CSV]**, haga clic en **[!UICONTROL Descargar plantilla CSV]** y elija **[!UICONTROL Lista de usuarios actuales]**.

   ![Editar usuarios por CSV](assets/migrate-edit-users-by-csv.png)

   Para obtener descripciones de los campos del archivo descargado, consulte [Formato de archivo CSV](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header).
4. Agregue asignaciones de licencia al CSV, luego arrastre el archivo actualizado al cuadro de diálogo **[!UICONTROL Editar usuarios por CSV]** y haga clic en **[!UICONTROL Cargar]**. Recibirá un correo electrónico cuando finalice la operación.

   ![Edición de usuario completa](assets/migrate-user-edit-complete.png)

Descargue el [informe de resultados](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) para validar las asignaciones. A continuación, programe la incorporación con un especialista en incorporación a Adobe para obtener información acerca de [las funciones administrativas](https://helpx.adobe.com/enterprise/using/admin-roles.html) y la [identidad](https://helpx.adobe.com/es/enterprise/using/identity.html).

## Asignación masiva de licencias (de VIP a ETLA)

Si tiene una suscripción de VIP y está trasladando usuarios a ETLA, utilice este flujo masivo:

1. Inicie sesión en [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) y abra la organización que contiene a los usuarios de VIP.
2. Vaya a **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios]**.
3. Haga clic en ![Menú de opciones más](assets/migrate-more-options.png) en la esquina superior derecha y, a continuación, elija **[!UICONTROL Exportar lista de usuarios a CSV]**.
4. Abra la organización de ETLA donde desee que estén esos usuarios.
5. Vaya a **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios]**.
6. Haga clic en **[!UICONTROL Agregar usuarios mediante CSV]**.
7. Haga clic en **[!UICONTROL Descargar plantilla CSV]** y, a continuación, agregue los usuarios de VIP desde el CSV que exportó en el paso 3.
8. Cargue el CSV actualizado.

Recibirá un correo electrónico cuando se agreguen usuarios a la organización de ETLA.

![Usuarios añadidos después de la migración de VIP a ETLA](assets/migrate-users-added-vip-etla.png)

Descargue el [informe de resultados](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) para validar las asignaciones. Programe la incorporación con un especialista en incorporación de Adobe para [funciones administrativas](https://helpx.adobe.com/enterprise/using/admin-roles.html) e [identidad](https://helpx.adobe.com/es/enterprise/using/identity.html).

Para problemas de carga en lotes, consulte [Solucionar problemas de carga en lotes de usuarios](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).

## Asignación masiva de licencias (de ETLA a VIP)

Si tiene una suscripción a ETLA y va a mover usuarios a VIP:

1. Inicie sesión en [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) y abra la organización que contiene a los usuarios de ETLA.
2. Vaya a **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios]**.
3. Haga clic en ![Menú de opciones más](assets/migrate-more-options.png) en la esquina superior derecha y, a continuación, elija **[!UICONTROL Exportar lista de usuarios a CSV]**.

   ![Menú de lista de usuarios de exportación](assets/migrate-export-user-list.png)

4. Abra la organización de VIP donde desee que estén esos usuarios.
5. Vaya a **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios]**.
6. Haga clic en **[!UICONTROL Agregar usuarios mediante CSV]**.
7. Haga clic en **[!UICONTROL Descargar plantilla CSV]** y, a continuación, agregue los usuarios de ETLA desde el CSV que exportó en el paso 3.
8. Cargue el CSV actualizado.

Recibirá un correo electrónico cuando se agreguen usuarios a la organización de VIP.

![Usuarios añadidos después de la migración de ETLA a VIP](assets/migrate-users-added-etla-vip.png)

Descargue el [informe de resultados](https://helpx.adobe.com/enterprise/using/users.html#main-pars_header_1346350355) para validar las asignaciones. Programe la incorporación con un especialista en incorporación de Adobe para [funciones administrativas](https://helpx.adobe.com/enterprise/using/admin-roles.html) e [identidad](https://helpx.adobe.com/es/enterprise/using/identity.html).

Para problemas de carga en lotes, consulte [Solucionar problemas de carga en lotes de usuarios](https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).
