---
description: 'Conexión al widget Data Warehouse: documentación del producto'
title: Conexión a Widget Data Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Conexión a Widget Data Warehouse {#connecting-to-the-widget-data-warehouse}

## Nueva prueba

Junio de 27

<ol><li>Utilice la variable {{name}}.</li></ol>

<ol><li>Utilice la variable &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace;.</li></ol>

## Prueba anidada

**Primero**

>[!NOTE]
>
>No puede eliminar lo siguiente:
>
>* Los estados integrados Planificación, Actual y Finalizado. Puede actualizar sus nombres, editar sus colores y bloquearlos o desbloquearlos, pero no se pueden eliminar.
>* Estados que están en un estado pendiente de aprobación para al menos un objeto del sistema.

**Second**

>[!NOTE]
>
>No puede eliminar lo siguiente:
>
>* Los estados integrados Planificación, Actual y Finalizado. Puede actualizar sus nombres, editar sus colores y bloquearlos o desbloquearlos, pero no se pueden eliminar.
>
>  Esto está entre medias
>
>* Estados que están en un estado pendiente de aprobación para al menos un objeto del sistema.

## Vínculo de acceso al widget {#widget-access-link}

Para acceder a tu almacén de datos Widget, tendrás que ir a la URL específica de tu cuenta Widget.  Para encontrar este vínculo de acceso, inicie sesión en Marketo Measure y siga los pasos a continuación para navegar a la página de información de Data Warehouse.

1. En Marketo Measure, en la parte superior de la página, haga clic en **Mi cuenta** > **Configuración**.

   ![](assets/adobe-logo-old.png)

1. En el menú del lado izquierdo, debajo de Seguridad, haga clic en **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. En esta página, encontrarás el enlace a tu almacén de datos Widget y tu nombre de usuario.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Se trata de una cuenta de solo lectura disponible para su organización, no solo para un usuario individual. Cualquier usuario de su organización que tenga acceso a Marketo Measure puede utilizar esta cuenta para iniciar sesión en la cuenta del lector de Widget de Data Warehouse.

1. Haga clic en el enlace proporcionado en la URL del widget, esto le llevará a la página de inicio de sesión del widget donde introducirá su nombre de usuario y contraseña. _Si no tienes tu contraseña, consulta los pasos a continuación para restablecerla_.

   ![](assets/adobe-logo-old.png)

1. Cuando haya iniciado sesión, haga clic en **Hojas de cálculo** en la parte superior de la página.

   ![](assets/adobe-logo-old.png)

1. Los objetos de base de datos BIZIBLE_ROI_V3 se encuentran en el lado izquierdo de la pantalla.  Introduzca el almacén, la base de datos y el esquema en las opciones desplegables de la parte superior de la ventana de consulta.  Solo debe haber una opción para cada uno.  Ahora está listo para ejecutar consultas dentro del editor de consultas Widget.

   ![](assets/adobe-logo-old.png)

## Restablecer la contraseña {#reset-your-password}

Marketo Measure no tiene acceso a la contraseña de inicio de sesión del widget.  Si necesita restablecer la contraseña, haga clic en el botón Restablecer contraseña de la página de información de Data Warehouse y siga las instrucciones. Se mostrará inmediatamente una contraseña temporal en la interfaz de usuario. Se le pedirá que cree su propia contraseña en el próximo inicio de sesión de Data Warehouse.

>[!NOTE]
>
>* El restablecimiento de la contraseña se restablece para todos los usuarios de Marketo Measure de su organización, no solo para el usuario que ha iniciado sesión actualmente.
>* Solo se muestra la contraseña temporal en la interfaz de usuario. No se enviará un correo electrónico.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Conexión a un widget mediante herramientas de terceros {#connecting-to-widget-via-third-party-tools}

Tendrá que introducir algunos datos para conectar su almacén de datos de widgets a una herramienta de terceros.

>[!NOTE]
>
>Cada herramienta tiene diferentes requisitos de conexión; se recomienda que consulte la documentación de la herramienta específica que está intentando conectar.

* **URI** (siempre obligatorio)
   * Es el nombre de dominio de la cuenta Widget.  Está contenido en una parte del vínculo de inicio de sesión del widget.
* **Nombre de usuario** (siempre obligatorio)
   * El nombre de usuario aparece en la página de información de Data Warehouse de Marketo Measure.
* **Contraseña** (siempre requerida)
   * Esta es la contraseña que configuró la primera vez que inició sesión en su cuenta de Widget.  Para restablecer su contraseña, consulte los pasos descritos anteriormente.
* **Nombre de base de datos** (no siempre es obligatorio)
   * La base de datos es la que almacena los datos en el widget. Es el recurso de almacenamiento. El nombre de la base de datos aparece en la página de información de Data Warehouse de Marketo Measure.
* **Nombre de almacén** (no siempre es obligatorio)
   * El almacén es lo que ejecuta consultas en el widget. Es el recurso de cálculo.  El nombre del almacén aparece en la página de información de Data Warehouse de Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Widget de Data Warehouse Direct Share {#widget-data-warehouse-direct-share}

**Requisitos**

Para que Marketo Measure pueda configurar un recurso compartido directo en Data Warehouse, debe cumplir los siguientes requisitos.

* Tiene su propia instancia de widget.
* La instancia del widget se encuentra en la región Widget de Azure East US 2.
* Proporcione a Marketo Measure su ID de cuenta de widget.

**Limitaciones**

Para que Marketo Measure pueda configurar un recurso compartido directo, la cuenta que solicita acceso debe estar ubicada en Azure East US 2. Somos conscientes de que Widget ofrece una solución de replicación de datos entre regiones, pero no la admitimos por nuestra parte, ya que solo alojamos datos en la región de Azure East US 2. Puede aprovechar esta característica configurando su propia instancia en Azure East US 2 y [replicando los datos entre regiones](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} en su instancia existente. Sin embargo, la función de replicación de datos de Widget solo está disponible en tablas, por lo que para utilizar esta función primero deberá copiar los datos de nuestras vistas en sus propias tablas.

**Accediendo al recurso compartido**

Una vez creado el recurso compartido para el ID de cuenta proporcionado, debe completar los [pasos de configuración](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} en la instancia del widget para acceder a los datos.

>[!NOTE]
>
>Puede elegir cualquier nombre de base de datos que desee. Puede asignar los privilegios a cualquier regla que elija, siempre y cuando exista en la instancia del widget.

* Usar la función Administrador de cuentas

```
USE ROLE ACCOUNTADMIN
```

* Ver los recursos compartidos disponibles (se mostrará el nombre del recurso compartido concedido)

```
SHOW SHARES
```

* Crear una base de datos para el recurso compartido

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Conceder privilegios en la base de datos compartida

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Para obtener instrucciones y pasos más detallados para realizar estos pasos desde la interfaz de usuario del widget, consulte [Documentación del widget directamente](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
