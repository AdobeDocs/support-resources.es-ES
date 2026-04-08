---
title: Actualizar directivas de organización en Global Admin Console
description: Obtenga información sobre cómo un administrador global puede definir y modificar directivas para una organización y sus elementos secundarios en Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 1%

---

# Actualizar directivas de organización en Global Admin Console

**Se aplica a:** Empresa

Obtenga información sobre cómo un administrador global puede definir y modificar directivas para una organización y sus elementos secundarios en Global Admin Console.

>[!NOTE]
>
>En [Global Admin Console](https://helpx.adobe.com/es/enterprise/global-admin-console/adopt-global-administration.html), seleccione una organización de la jerarquía y vaya a la ficha **Directivas** para permitir o no permitir o bloquear las directivas.
>
> [Iniciar sesión en Global Admin Console](https://global-admin-console.adobe.com/)

Las directivas están asociadas a una organización y restringen las operaciones que se pueden realizar en esa organización. Cuando se establece un valor de directiva, restringe o habilita las acciones a partir de ese momento.
Por ejemplo, si la directiva **Reclamar dominios** se establece en *no permitido*, no se podrá reclamar ningún dominio adicional, pero no se verá afectado ningún dominio reclamado antes de establecer el valor de la directiva.

## Configurar directivas

Para modificar las políticas de una organización, haga lo siguiente:

1. En Global Admin Console, [seleccione una organización](https://helpx.adobe.com/es/enterprise/global-admin-console/overview.html) para editar y luego vaya a la pestaña **[!UICONTROL Políticas]**.
1. Seleccione el conmutador de la política correspondiente para permitirlo o no. También puede bloquear una directiva para que nadie, excepto un administrador global de la [organización seleccionada](https://helpx.adobe.com/es/enterprise/global-admin-console/overview.html) o su organización principal, pueda cambiarla o desbloquearla.
1. Para bloquear una directiva, selecciona el icono **[!UICONTROL Bloquear]** ![Bloquear](./assets/lock.png). Al pasar el ratón por encima del bloqueo, se muestra el nombre de la organización seleccionada. Más información sobre [bloqueos de directivas](#policy-locks).
1. Seleccione **[!UICONTROL Revisar cambios pendientes]** después de haber terminado de editar las organizaciones. Después de revisarlos, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/es/enterprise/global-admin-console/execute-jobs.html).

## Bloqueos de directivas {#policy-locks}

Cuando una directiva está bloqueada, su valor no se puede cambiar hasta que se desbloquea. Global Admin Console recuerda que la [organización seleccionada](https://helpx.adobe.com/es/enterprise/global-admin-console/overview.html) en el selector de organizaciones es la organización desde la que se bloqueó la directiva. Cualquier administrador global de la organización seleccionada o de cualquier organización superior del árbol tiene permiso para desbloquear la directiva. Los administradores globales cuyo ámbito es inferior a esa organización no tienen permiso para desbloquear y cambiar valores de directiva.

Para crear un entorno bloqueado, defina los valores de directiva deseados en las organizaciones secundarias y, a continuación, bloquéelos. Los administradores globales de esas organizaciones secundarias no podrán editar los valores de directiva.

### Ejemplo: Entorno bloqueado

Si Elissa, la administrador global de *Acme Division*, crea las organizaciones secundarias *Marketing* e *Ingeniería*, entonces agrega a Robert como administrador global de *Marketing* y a Sarah como administrador global de *Ingeniería*. A continuación, establece varias directivas en *No permitido* y las *bloquea*. Elissa puede desbloquear y cambiar posteriormente los valores de las directivas cuando elija *Acme Division* como la organización seleccionada, pero Robert y Sarah no pueden desbloquear las directivas en las organizaciones de las que son administradores globales, ya que están bloqueadas por la organización *Acme Division*.

## Detalles de la política

### Administración de organización

| Nombre de política | Descripción |
| --- | --- |
| **Crear organizaciones secundarias** | Permite a los administradores globales crear organizaciones secundarias. Si *se deshabilita*, no se pueden crear organizaciones secundarias. |
| **Cambiar nombre de organización** | Si se permite, un administrador global o del sistema puede cambiar el nombre de la organización. También controla el cambio de país o región de la organización. El nombre de ruta de acceso de una organización también se puede cambiar independientemente de esta configuración de directiva si se cambia el nombre de una organización principal, o si se prepara la organización o un antecesor de la organización. |
| **Eliminar organizaciones** | Permite que los administradores globales eliminen organizaciones secundarias. Esto es más importante cuando las organizaciones con almacenamiento empresarial están habilitadas debido al riesgo de eliminar recursos de usuario. |

### Administración del administrador

| Nombre de política | Descripción |
| --- | --- |
| **Agregar o eliminar administradores** | Permite a los administradores globales añadir nuevos administradores a una organización. Si se deshabilita *de*, no se podrán agregar nuevos administradores. |
| **Heredar administradores de sistema del elemento principal cuando se crea la organización secundaria** | Cuando los administradores globales crean nuevas organizaciones secundarias, los administradores del sistema de la organización principal se convierten automáticamente en administradores del sistema de la nueva organización. Esta directiva está *desactivada* de manera predeterminada. |
| **Administrar administradores** | Permite a los administradores globales cambiar o eliminar o editar permisos de administración. |

### Administración de usuarios

| Nombre de política | Descripción |
| --- | --- |
| **Heredar usuarios de directorios administrados por la organización principal** | Esta directiva debe estar *activada* y activa antes de crear la nueva organización secundaria. Cuando se crea una organización secundaria, los usuarios de la organización principal están disponibles como usuarios en la organización secundaria. En otras palabras, esta directiva configura automáticamente una relación de confianza entre el elemento principal y el secundario cuando se crea el nuevo elemento secundario dentro de la GAC. Para las organizaciones existentes, cualquier relación de confianza antes de agregarse a la GAC se mantendrá una vez introducida en la GAC. Si no existen relaciones de confianza, se debe seguir el proceso habitual de solicitud de confianza. Para que esta directiva tenga éxito, el administrador global que crea la nueva organización también debe ser un administrador del sistema de la organización principal con el dominio reivindicado. Si no es así, la relación de confianza de dominio no se heredará en la organización recién creada. |
| **Agregar usuarios de Adobe ID** | Si se configura, la organización no puede agregar usuarios de tipo Adobe ID a través de Admin Console, la API de administración de usuarios (UMAPI) ni el mecanismo de sincronización. |
| **Administrar grupos de usuarios** | Si se permite, los administradores globales, del sistema y de grupos de usuarios pueden crear, editar y eliminar grupos de usuarios. |

### Aplicación de directorios y dominios

| Nombre de política | Descripción |
| --- | --- |
| **Reclamar dominios** | Si se configura, los administradores del sistema pueden reclamar dominios en Admin Console. |
| **Cambiar configuración de identidad** | Si se configura, los administradores del sistema pueden cambiar la configuración de la identidad del usuario en Admin Console. |

### Asignación de productos

| Nombre de política | Descripción |
| --- | --- |
| **Administrar productos** | Permite a los administradores globales añadir o eliminar productos y cambiar las concesiones de recursos de productos. |

### Uso compartido de recursos

| Nombre de política | Descripción |
| --- | --- |
| **El administrador de sistema o de almacenamiento puede cambiar la configuración de uso compartido de recursos** | Si se permite, los administradores del sistema y del almacenamiento pueden cambiar la configuración de uso compartido de recursos, incluidos los contactos de seguridad, la directiva de contraseñas y la directiva de almacenamiento. |
| **Heredar la directiva de uso compartido de un elemento principal al crear una organización** | Si se permite, la configuración de uso compartido de recursos se hereda del nodo principal cuando se crea una organización secundaria. La configuración de uso compartido de recursos incluye contactos de seguridad, directiva de contraseñas y directiva de almacenamiento. Esto solo se aplica a las organizaciones recién creadas en el momento de la creación. Se establece en un elemento principal y afecta a la creación de organizaciones secundarias en ese elemento principal. |
