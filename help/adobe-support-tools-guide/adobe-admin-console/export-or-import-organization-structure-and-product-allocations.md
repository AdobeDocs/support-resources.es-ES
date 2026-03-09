---
title: Exportar o importar la estructura de la organización y las asignaciones de productos
description: Obtenga información sobre cómo los administradores globales exportan e importan datos de jerarquía de organizaciones y asignación de productos en Global Admin Console mediante JSON, CSV o XLSX. Se aplica a Enterprise.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: fe5b03e5886a43b55929a2bdba45da3c08ad0ab9
workflow-type: tm+mt
source-wordcount: '4423'
ht-degree: 3%

---


# Exportar o importar la estructura de la organización y las asignaciones de productos

**Se aplica a:** Empresa

Descubra cómo los administradores globales pueden optimizar la administración de organizaciones y productos con las funciones de exportación e importación de Global Admin Console.

Acceda a la ficha **[!UICONTROL Organizaciones]** en [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) para exportar o importar la estructura de la organización. Vaya a la pestaña **[!UICONTROL Asignación de productos]** para ver los datos de asignación. Utilice el icono **[!UICONTROL Más opciones]** **⋮** para seleccionar la exportación o la importación. [Inicie sesión en Global Admin Console](https://global-admin-console.adobe.com).

## Exportar la estructura de la organización

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede exportar la jerarquía de la organización. Puede descargar una representación JSON, CSV o XLSX de toda la jerarquía de la organización o un subconjunto de ella. A continuación, puede utilizar estos datos para su análisis o modificación.

El formato de exportación elegido afecta a la estructura de los datos exportados:

- Formato CSV: permite exportar sólo un tipo de datos a la vez. Al exportar perfiles de producto en formato CSV, los perfiles y recursos se combinan en una tabla. Hay varias entradas para el perfil del producto, una para cada recurso.
- Formato XLSX: los resultados de cada detalle de organización se muestran en una hoja independiente. Los registros están conectados entre los distintos tipos de objeto mediante un ID de referencia. En algunos casos, puede haber varias filas para un objeto en particular (por ejemplo, objetos Resource cuando hay un conjunto de valores asociados a un recurso determinado).
- Formato JSON: el más flexible. Puede aprovechar las relaciones estructurales entre los objetos exportados (por ejemplo, los productos de una organización aparecen directamente en el elemento de la organización). Los mismos campos se exportan en los tres formatos, pero algunos valores son redundantes en el formato JSON.

### Pasos a exportar

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/). En la ficha **[!UICONTROL Organizaciones]**, use el selector de organizaciones para seleccionar la jerarquía de organizaciones a la que desea exportar. Se exportan los datos de todas las organizaciones de la jerarquía.
2. Seleccione el icono de ⋮ **[!UICONTROL Más opciones]** y elija **[!UICONTROL Exportar]**.

   ![Exportar estructura organizativa](./assets/export-org-structure.png)

3. En el cuadro de diálogo **[!UICONTROL Exportar]**, seleccione lo que desea exportar y un formato en el que exportar los datos.

   ![Cuadro de diálogo de exportación de Admin Console](./assets/export-12.png)

4. Seleccione **[!UICONTROL Exportar]**. El archivo de exportación puede tardar varios minutos en generarse. Una vez finalizado, para descargar el informe, vaya a **[!UICONTROL Global Admin Console]** > **[!UICONTROL Información]** > **[!UICONTROL Exportar informes]**.

&#x200B;> [!NOTE]
>
> Los archivos JSON se exportan en formato zip. Puede abrirlos con una utilidad de compresión o con las funciones de compresión zip del sistema operativo.

Después de descargar el archivo, puede manipular los datos y, a continuación, importarlos de nuevo. Las actualizaciones importadas aparecen en Global Admin Console como si los datos se hubieran editado manualmente.

## Importar la estructura de la organización

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede importar datos potencialmente modificados. Cuando se cargan, los nuevos datos se comparan con los datos actuales y los cambios se aplican a la jerarquía de la organización. Todas las operaciones de importación se realizan en la copia actualizada de la jerarquía de la organización. Si tiene cambios pendientes, los cambios de importación se agregarán encima de los cambios pendientes en la jerarquía.

### Pasos para la importación

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com). En la ficha **[!UICONTROL Organizaciones]**, use el selector de organizaciones para seleccionar la jerarquía de organizaciones donde desea realizar la importación.
2. Seleccione el icono **[!UICONTROL Más opciones]** **⋮** y seleccione **[!UICONTROL Importar]**. Según el tamaño y la complejidad del archivo de importación, el procesamiento puede tardar entre unos segundos y varios minutos.
3. Seleccione **[!UICONTROL Seleccionar un archivo]** y elija un archivo JSON, CSV o XLSX para cargar. Para el CSV, solo se puede importar un detalle de organización a la vez y no admite la importación de productos. Los cambios importados aparecen como si los datos se hubieran editado manualmente.
4. Seleccione **[!UICONTROL Cerrar]**.
5. Seleccione **[!UICONTROL Revisar cambios pendientes]**. A continuación, seleccione **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html). Antes de ejecutar los cambios, las acciones pendientes se muestran del mismo modo que cuando las ediciones se realizan manualmente en Global Admin Console.

## Exportación e importación de esquemas

Al importar datos mediante un archivo CSV, los campos pueden aparecer en cualquier orden, pero siempre deben coincidir con su fila de encabezado.

Al importar datos, debe especificar una operación para cada elemento. La operación puede ser cualquiera de las siguientes:

- Update: indica una edición.
- Crear: indica la creación de un nuevo objeto (por ejemplo, organización, grupo de usuarios o administrador).
- Eliminar: indica la eliminación de un objeto (por ejemplo, organización, grupo de usuarios o administrador).

Los registros de entrada sin campo de operación o en blanco se omiten.

### Organizaciones

<table>
  <tr>
    <th>Nombre del campo</th>
    <th>Descripción</th>
    <th>Notas</th>
  </tr>

<tr>
    <td>id</td>
    <td>
      ID de organización.<br><br>
      Al añadir una nueva organización, puede estar vacía o configurarse como identificador de marcador de posición, por ejemplo,
      new_org_1. El identificador del marcador de posición se utiliza en casos en los que otras entradas importadas deben hacer referencia a
      a esta organización. Después de la creación, se asigna un ID de organización real que reemplaza a todos los
      usos del id de organización de marcador de posición.
    </td>
    <td>Se puede establecer en un valor temporal cuando operation=create</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      Nombre simple de la organización. Longitud mínima 4, máxima 100.
      Los nombres pueden contener caracteres UTF-8 de hasta 3 bytes,
      No se admiten caracteres de 4 bytes.
    </td>
    <td>
      Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>Código de país o región</td>
    <td>
      Debe definirse cuando operation=create, puede actualizarse cuando operation=update
    </td>
  </tr>

<tr>
    <td>tipo</td>
    <td>Tipo de organización</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID de la organización principal. En blanco para la organización raíz.
      Al actualizar, se aplican restricciones significativas, incluido que el nuevo elemento principal esté en la misma jerarquía y
      tienen los productos que están presentes en la organización.
    </td>
    <td>
      Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Número de administradores</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Número de dominios</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Cantidad de usuarios</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Número de grupos de usuarios</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>administradores</td>
    <td>Conjunto de objetos de administración que representan a los administradores de esta organización</td>
    <td rowspan="6">
      Puede que falte si no se selecciona para la exportación. Se muestra en una pestaña independiente en los archivos XLSX.
    </td>
  </tr>

<tr>
    <td>dominios</td>
    <td>Conjunto de objetos de dominio que representan los dominios de esta organización</td>
  </tr>

<tr>
    <td>products</td>
    <td>Conjunto de objetos de producto que representan los productos de esta organización</td>
  </tr>

<tr>
    <td>productProfiles</td>
    <td>Conjunto de objetos de perfil de producto que representan perfiles de producto en esta organización</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Conjunto de objetos de grupo de usuarios que representan grupos de usuarios en esta organización</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Estructura que representa las políticas y sus valores</td>
  </tr>

<tr>
    <td>operación</td>
    <td>
      Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos.
    </td>
    <td>Siempre en blanco al exportar.</td>
  </tr>
</table>


**Requisitos de importación:**

- Para actualizar o eliminar, orgId debe hacer referencia a una organización existente en su jerarquía.
- Si está creando una nueva organización, puede dejar en blanco el campo orgId o establecerlo en un ID único que pueda configurar (como new-1 o new-2). Esto proporciona un ID que se puede utilizar para hacer referencia a la organización que se va a crear.
- El código de país debe ser válido.
- orgId para la operación *Update* y *Delete* ya debería estar presente en la jerarquía de la organización.
- orgId marcado como *Delete* no debería seleccionarse como parentOrgId para organizaciones con *actualización* o *creación* de la operación.
- Las organizaciones secundarias del mismo nivel y del mismo padre no deben tener los mismos orgNames.
- Para crear una organización o actualizar un nombre de organización, el nombre de la organización no debe coincidir con el nombre de un hijo existente del mismo padre.

### Administradores

<table>
  <tr>
    <th>Nombre del campo</th>
    <th>Descripción</th>
    <th>Utilice </th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Referencia a la organización en la que reside el administrador.</td>
    <td>Se utiliza como referencia para buscar objetos asociados o que los contengan.</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     Nombre del usuario administrador.
El nombre y los apellidos de los usuarios de Adobe ID se pueden reemplazar por un valor proporcionado por el usuario cuando este acepta la invitación.
    </td>
    <td rowspan="4">
      Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>lastName</td>
    <td>Apellidos del usuario administrador</td>
  </tr>

<tr>
    <td>correo electrónico</td>
    <td>Correo electrónico del usuario administrador. Esta es una clave principal para el usuario y debe ser única.</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
Código de país o región donde opera el usuario. Solo se aplica a los tipos Federated y Enterprise Id.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Uno de "Adobe ID", "Enterprise ID" o "Federated ID".</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>Uno de "GLOBAL ADMIN", "GLOBAL VIEWER", "SYSTEM ADMIN", "USER GROUP ADMIN", "PRODUCT ADMIN", "PRODUCT PROFILE ADMIN", "DEPLOYMENT ADMIN" y "STORAGE_ADMIN".</td>
    <td rowspan="4">Se puede establecer cuando operation=Create</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>ID del grupo del que es administrador este usuario. Relevante solo para administradores de grupos de usuarios y perfiles de productos.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>ID de licencia del producto del que es administrador este usuario. Relevante solo para administradores de productos.</td>

</tr>

<tr>
    <td>sector</td>
    <td>Nombre de dominio del usuario si no utiliza el dominio de correo electrónico</td>

</tr>

<tr>
    <td>userName</td>
    <td>Nombre de usuario del usuario si no utiliza la dirección de correo electrónico</td>
    <td></td>
  </tr>

<tr>
    <td>operación</td>
    <td>Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos.</td>
    <td></td>
  </tr>
</table>


**Requisitos de importación:**

- orgId, email, adminType y userType deben contener valores válidos.
- countryCode debe ser válido.
- Si el usuario ya existe y se está actualizando, userType debe coincidir con el usuario.
- Compruebe si hay direcciones de correo electrónico duplicadas en la organización.

### Perfiles de producto

Las exportaciones e importaciones de perfiles de producto constan de dos partes: los detalles del perfil de producto y un conjunto de recursos asociados al perfil de producto. Estos recursos identifican los servicios que se pueden configurar, normalmente solo para habilitarlos o deshabilitarlos.

- Los objetos de recurso están anidados dentro del perfil de producto en formato JSON.
- Cuando se utiliza CSV o XLSX con perfiles de producto, los perfiles y recursos se combinan en una tabla. Habrá varias entradas para el perfil del producto, una para cada recurso.
- El campo &quot;seleccionado&quot; del recurso controla si el servicio está habilitado.
- Al importar perfiles de producto, debe haber una operación Crear o Actualizar en el propio perfil de producto y en cualquier objeto de recurso que se vaya a actualizar o crear.


<table>
  <tr>
    <th>Nombre del campo</th>
    <th>Descripción</th>
    <th>Utilice </th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Identificador del perfil del producto
El valor de marcador de posición se puede utilizar en la creación para que otros objetos puedan hacer referencia al nuevo perfil.
    </td>
    <td>Se puede establecer en un valor temporal cuando operation=create</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Nombre del perfil del producto. No puede ser un duplicado de otros perfiles de producto o grupos de usuarios en la misma organización.
    </td>
    <td rowspan="2">
   Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Descripción de texto del perfil del producto</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Referencia del ID de licencia del producto</td>
    <td rowspan="2"> Se utiliza como referencia para buscar objetos asociados o que los contengan
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organización que contiene el grupo de usuarios
    </td>
  </tr>

<tr>
    <td>notificaciones</td>
    <td>Verdadero o falso para indicar si se debe enviar una notificación por correo electrónico a los usuarios cuando se agregan o eliminan de este perfil de producto</td>
    <td>Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente</td>
  </tr>

<tr>
    <td>recursos</td>
    <td> Matriz de recursos asociados a este perfil de producto.
El campo de recursos solo está presente para el formato JSON. Para los formatos CSV y XLSX, los recursos se representan con los siguientes campos adicionales: resourceName, resourceId, resourceDescription, icon, selected, quota, resourceType. Para obtener más información sobre estos campos, consulte [Productos y recursos](#products-and-resources).
Si el perfil de producto tiene más de un recurso, habrá varias filas presentes, una para cada recurso. Los demás campos tendrán los mismos valores para cada recurso. </td>
    <td></td>
  </tr>

<tr>
    <td>operación</td>
    <td>Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos.</td>  
    <td></td>
  </tr>
</table>



**Requisitos de importación:**

- productProfileId, licenseId y orgId deben tener valores válidos.
- Al crear un perfil de producto, productProfileName debe ser un nombre válido y no debe duplicar otro nombre de perfil de producto o nombre de grupo de usuarios en la misma organización.
- El campo de cuota debe tener un valor válido para el tipo de unidad. Es numérico o &quot;ilimitado&quot; cuando resourceType=QUOTA o en blanco en caso contrario.
- El campo de notificación debe ser true o false.
- Para las importaciones CSV y XLSX, valide productProfileId; todas sus entradas deben tener los mismos orgId, licenseId y productProfileName.
- Valide el productProfileName duplicado en el archivo de entrada y en la organización.
- Los perfiles que se van a actualizar y eliminar deben estar presentes en la organización.
- Los recursos que se van a actualizar y eliminar (desactivar) deben estar presentes en el perfil.
- Para que se creen los perfiles, asegúrese de lo siguiente:
   - El orgId debe ser una organización nueva o una existente.
   - El ID de licencia debe ser un producto nuevo o existente.
   - Valide los recursos del perfil.

### Recursos en perfiles de producto


<table>
  <tr>
    <th>Nombre del campo</th>
    <th>Descripción</th>
    <th>Utilice </th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>
     Nombre del recurso
    </td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>
   Identificador del recurso
    </td>
    <td>
   Solo lectura
    </td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Descripción de texto del recurso</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>icono</td>
    <td>URL de la imagen del recurso</td>
    <td> Solo lectura</td>
  </tr>

<tr>
    <td>seleccionado</td>
    <td>Para una entrada de configuración, si la función está habilitada. Este campo solo está presente en JSON.</td>
    <td rowspan ="2">Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente.</td>
  </tr>

<tr>
    <td>cuota</td>
    <td>Cantidad de recurso principal que se puede entregar a los usuarios a través de este perfil de producto. Este campo solo está presente en JSON.</td>
    <td></td>
  </tr>

<tr>
    <td>resourceType</td>
    <td> Si está presente, el valor es SERVICIO. Indica que este recurso representa un servicio que se puede habilitar o deshabilitar en función del valor del campo seleccionado. Este campo solo está presente en JSON.</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>operación</td>
    <td>Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos.</td>  
    <td></td>
  </tr>
</table>

**Requisitos de importación:**

- El campo de operación de los recursos se omite cuando el perfil de producto al que pertenecen tiene las operaciones establecidas como *Delete* o *Create*.
- No se debe marcar ningún recurso para eliminar; la operación no es válida.
- Para que se creen los perfiles de producto, el número de recursos debe coincidir con el número de recursos del perfil de producto de origen.
- Para los recursos con la operación *Update*, el recurso debe estar presente en el perfil del producto.

### Grupos de usuarios

<table>
  <tr>
    <th>Nombre del campo</th>
    <th>Descripción</th>
    <th>Utilice </th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
Identificador del grupo de usuarios
El valor de marcador de posición se puede utilizar en la creación para que otros objetos puedan hacer referencia al nuevo grupo de usuarios.
    </td>
    <td>Se puede establecer en un valor temporal cuando operation=create</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td> Nombre del grupo de usuarios</td>
    <td rowspan="2"> Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente</td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Descripción de texto del grupo de usuarios</td>
    <td></td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Número de usuarios en el grupo de usuarios</td>
    <td>Solo lectura</td>
  </tr>

<tr>
    <td>perfiles</td>
    <td>Matriz de ID de perfil de producto con los que está asociado el grupo de usuarios.
XLSX tiene una fila por valor con los mismos valores para otros campos.</td>
    <td>Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente</td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organización que contiene el grupo de usuarios.</td>
    <td>Se utiliza como referencia para buscar el objeto contenedor o asociado.</td>
  </tr>

<tr>
    <td>operación</td>
    <td>Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos.</td>
    <td></td>
  </tr>
</table>



**Requisitos de importación:**

- orgId debe hacer referencia a una organización existente o a una organización que se está creando en la misma importación.
- userGroupId debe hacer referencia a un grupo existente para actualizarlo o eliminarlo, y puede ser un id que defina para nuevos grupos de usuarios.
- Para la actualización o creación, userGroupName no debe estar en blanco y no debe duplicar otro nombre de grupo de usuarios o perfil de producto en la misma organización.
- Asegúrese de que userGroupName no esté duplicado en el archivo de entrada y en la organización.
- userGroups que se va a actualizar y eliminar debe estar presente en la organización.
- El perfil que se va a eliminar del grupo de usuarios debe estar presente en el grupo de usuarios. No se pueden realizar operaciones de actualización en el perfil de un grupo de usuarios.
- Para que se creen grupos de usuarios, asegúrese de lo siguiente:
   - El orgId debe ser una organización nueva o una existente.
   - El ID de licencia, si corresponde, debe ser un producto nuevo o uno existente.
   - productProfileId debe ser un perfil de producto nuevo o uno existente.

### Dominios

La información de dominio proporciona información de solo lectura sobre los dominios disponibles en cada organización. Estos datos no pueden editarse.


| Nombre del campo | Descripción | Utilice  |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Referencia a la organización en la que aparece este dominio | Se utiliza como referencia para buscar objetos asociados o que los contengan. |
| domainName | Nombre del dominio (por ejemplo, adobe.com). | Solo lectura |
| directoryName | Nombre del directorio en el que aparece el dominio | Solo lectura |
| directoryType | Uno de Federated ID o Enterprise ID. | Solo lectura |
| domainStatus | Uno de &quot;ACTIVO&quot;, &quot;RESERVADO&quot;, &quot;NO RECLAMADO&quot;, &quot;RECLAMADO&quot;, &quot;VALIDADO&quot;, &quot;RETIRADO&quot;, &quot;CADUCADO&quot;. | Solo lectura |


### Productos y recursos {#products-and-resources}

En los archivos XLSX, hay dos hojas: una para los productos y otra para los recursos. En JSON, los objetos de recursos están anidados en el objeto de producto.

**Productos**


| Nombre del campo | Descripción | Utilice  |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | ID que identifica el producto. Cada producto tiene un ID de licencia único en la organización en la que aparece. Al añadir un nuevo producto, puede estar vacío o utilizar un identificador de marcador de posición (por ejemplo, new_product_1). Después de la creación, se asigna un ID de licencia real que reemplaza todos los usos del ID de licencia de marcador de posición. | Se puede establecer en un valor temporal cuando operation=create |
| productName | Nombre del producto | Solo lectura |
| productDescription | Descripción de texto del producto | Solo lectura |
| allowOverallocation | Valor booleano que indica si se permite la sobreasignación de esta instancia de producto. La sobreasignación se refiere a la capacidad de conceder a una organización secundaria más cantidad de la que se le ha concedido. | Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente |
| icono | URL del icono del producto | Solo lectura |
| sourceLicenseId | ID de licencia de la instancia de producto en la organización desde la que se asignó este producto. El valor es nulo si esta instancia no es un producto asignado, sino un producto comprado. | Se puede establecer cuando operation=Create |
| productId | Identificador del producto. | Solo lectura |
| orgId | Identificador de organización que contiene esta instancia de producto | Se utiliza como referencia para buscar objetos asociados o que los contengan |
| redistribuible | Valor booleano que indica si este producto tiene recursos que se pueden conceder a organizaciones secundarias. | Solo lectura |
| recursos | Objeto que contiene un conjunto de objetos de recurso que representan los recursos y la configuración de este producto |                                                                               |
| operación | Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos. |                                                                               |


**Requisitos de importación:**

- Para crear, el ID de licencia debe ser un ID único que usted cree.
- Para la actualización, el ID de licencia debe ser el ID de un producto existente en la organización especificada.
- orgId debe hacer referencia a una organización existente o a una que se esté creando en la misma operación de importación.
- Para crear, sourceLicenseId debe hacer referencia a un producto existente o al ID definido para un producto que se está creando en la misma operación de importación.
- licenseId y sourceLicenseId no deben ser iguales para los productos con la operación *Create*.
- Validar organizaciones de productos; la organización debe ser una nueva o ya debe estar presente en la jerarquía de la organización.
- Para la operación *Actualizar* y *Eliminar*, el producto ya debe estar presente en la jerarquía de la organización.
- El ID de licencia marcado como *Delete* no debe usarse como sourceLicenseId de productos con las operaciones *Create* y *Update*.
- Para los productos con la operación *Create*, valide que sourceLicenseId debe estar presente en la organización principal.

**Recursos para productos**

Los objetos de recursos pueden aparecer en los productos y en los perfiles de producto.


| Nombre del campo | Descripción | Utilice  |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Nombre del recurso | Solo lectura |
| resourceId | Identificador del recurso | Solo lectura |
| resourceDescription | Descripción de texto del recurso | Solo lectura |
| icono | URL de la imagen del recurso | Solo lectura |
| productName | Nombre del producto del que forma parte este recurso. | Solo lectura |
| licenseId | ID de licencia (instancia de producto) del producto del que forma parte este recurso. | Se utiliza como referencia para buscar objetos asociados o que los contengan |
| grantedQuantity | Cantidad concedida de este recurso: cantidad de recursos que esta organización tiene disponibles para utilizar localmente o asignar a organizaciones secundarias. | Se puede establecer o actualizar cuando operation=create u operation=update, respectivamente |
| unidad | Nombre de la unidad de cantidad de la concesión. | Solo lectura |
| currentQuantity | Cantidad utilizable actual en esta organización. Esta es la cantidad concedida menos los recursos asignados a las organizaciones secundarias. Este es el valor que se muestra en Admin Console para este producto/recurso. | Solo lectura |
| provisionedQuantity | Cantidad aprovisionada realmente: puede ser inferior a concesión o actual, puede ser inferior a cantidad actual si se ha establecido alguna limitación. | Solo lectura |
| operación | Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos. |                                                                               |


**Requisitos de importación:**

El campo de operación de los recursos se omite cuando el producto al que pertenecen tiene las operaciones establecidas como *Delete* o *Create*.
- No se debe marcar ningún recurso para eliminar; la operación no es válida.
- Para que se creen los productos, el número de recursos debe coincidir con el número de recursos del producto de origen.
- Para los recursos con la operación *Update*, el recurso debe estar presente en el producto.

## Importar y exportar datos de asignación de productos

Como [Administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), puede exportar los datos de asignación de productos como un archivo JSON o CSV. A continuación, puede manipular estos datos y cargarlos de nuevo para importar los cambios. Cuando se cargan los datos potencialmente modificados, los nuevos datos se comparan con los datos actuales y cualquier cambio se aplica a los datos de asignación del producto. A continuación, puede revisar y enviar los cambios pendientes para que surtan efecto.

## Exportar el modelo de asignación de productos

Para exportar el modelo de asignación de productos, haga lo siguiente:

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/) y vaya a la pestaña **[!UICONTROL Asignación de productos]**.
2. Seleccione el icono de ⋮ **[!UICONTROL Más opciones]** y luego seleccione **[!UICONTROL Exportar CSV]** o **[!UICONTROL Exportar JSON]**. Se ha descargado el archivo. [Más información](#export-and-import-formats-for-product-allocation) sobre los formatos de exportación.

## Importar el modelo de asignación de productos

Puede exportar datos, modificarlos y, a continuación, importar el archivo modificado. Para importar el modelo de asignación de productos, haga lo siguiente:

1. Inicie sesión en [Global Admin Console](https://global-admin-console.adobe.com/) y vaya a la pestaña **[!UICONTROL Asignación de productos]**.
2. Seleccione el icono de ⋮ **[!UICONTROL Más opciones]** y seleccione **[!UICONTROL Importar]**.
3. Seleccione un archivo JSON o CSV para cargar.
4. Seleccione **[!UICONTROL Revisar cambios pendientes]**. Después de revisar los cambios, selecciona **[!UICONTROL Enviar cambios]** para [ejecutarlos](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Exportar e importar formatos para la asignación de productos

Los formatos de exportación e importación son los mismos. Al importar en formato CSV, los campos pueden aparecer en cualquier orden, pero deben coincidir con la fila de encabezado. Al importar en formato JSON, los campos pueden aparecer en cualquier orden.

Debe especificar la operación al importar los datos de asignación del producto. La operación puede ser una de las siguientes:

- Update: indica una edición (cambio a grantedQuantity, allowOverAllocation values).
- Crear: indica que se debe agregar un recurso de producto a la organización especificada.
- Eliminar: indica la eliminación del producto.

Si no se proporciona ninguna operación, no se producirán cambios cuando se importen datos para esa fila en CSV o un objeto en JSON.

En el archivo exportado, hay una fila o registro para cada recurso de producto. Algunos productos tienen más de un recurso.

Si un producto tiene más de un recurso, las operaciones de actualización se pueden aplicar a recursos independientes, una operación de eliminación elimina el producto, incluidos todos los recursos de una organización, y una operación de creación necesita un registro para cada uno de los recursos del archivo de importación para que se pueda especificar la cantidad adecuada de cada uno de ellos. El campo allowOverAllocation es para todo el producto y no importa en qué recurso se encuentre una actualización de este campo.

### Descripción de los encabezados


| Nombre del campo | Descripción | Utilice  |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Nombre del producto. | Solo lectura |
| licenseId | El ID de un producto (exclusivo de un producto en una organización). Al añadir un nuevo producto, esto puede estar vacío o establecerse en un identificador de marcador de posición (por ejemplo, new_product_1). El identificador del marcador de posición se utiliza en casos en los que otras entradas importadas deben hacer referencia a este producto. Después de la creación, se asigna un ID de licencia real y se reemplazan todos los usos del ID de licencia de marcador de posición. | Se puede establecer cuando operation=Create |
| sourceLicenseId | ID del producto principal. Está vacío o es nulo si representa una compra en lugar de una asignación. | Se puede establecer cuando operation=Create |
| productId | Id. que identifica esta clase de producto. Este ID se comparte entre productos del mismo tipo y difiere del ID de licencia que identifica una instancia de este producto. | Solo lectura |
| resourceName | Nombre de este recurso de producto. Por ejemplo, licencias de usuario. | Solo lectura |
| resourceId | Id que identifica este recurso de producto. | Se puede establecer cuando operation=Create |
| orgPathName | Nombre de ruta de la organización en la que se encuentra este recurso de producto. Segmentos separados por &quot;/&quot;. | Solo lectura |
| orgName | Nombre simple de la organización que contiene este recurso de producto. Este es el segmento final de orgPathName. | Solo lectura |
| orgId | ID de organización de la organización que contiene este recurso de producto. | Se puede establecer cuando operation=Create |
| grantedQuantity | Número de unidades de la cantidad de recursos concedida a esta organización por su principal o el importe comprado si este registro de recursos de producto representa una compra. Este campo es actualizable, excepto para productos comprados o asignaciones raíz para los que el administrador global no tiene permiso para cambiar. | Se puede actualizar cuando operation=Update u operation=Create |
| unidad | Nombre de la unidad de recurso. Por ejemplo, Usuarios. | Solo lectura |
| totalAllocations | Suma de las subvenciones a organizaciones secundarias de esta organización para este recurso de producto. Este valor incluye las subvenciones directas a los hijos inmediatos más las sobreasignaciones de esas organizaciones. Por ejemplo, si esta organización concediera a un niño 10 y el niño asignara a su hijo 25, el total de asignaciones sería de 25: los 10 concedidos al niño más un excedente de 15 años en ese niño. | Solo lectura |
| grantOverage | Importe por el que totalAllocations supera el valor de grantedQuantity. Si totalAllocations no supera grantedQuantity, este valor es nulo o cero. | Solo lectura |
| localLicensingQuantity | Cantidad de este recurso concedida a esta organización que queda para su uso después de deducir la cantidad asignada a los hijos. Esta es la cantidad que se muestra como disponible en Admin Console. Este valor puede ser cero, pero nunca negativo, aunque esta organización haya sobreasignado recursos a sus tareas secundarias. | Solo lectura |
| localUsage | Número de unidades del recurso utilizado en esta organización. Por ejemplo, delegar una licencia de usuario a un usuario contaría como 1 unidad de uso. | Solo lectura |
| totalUsage | Número de unidades del recurso utilizado por esta organización y todos los elementos secundarios. Esto muestra el uso de este recurso en la parte de la jerarquía de organizaciones a la que da origen esta organización. | Solo lectura |
| useOverage | Cantidad de uso total de la subvención de la organización (la organización y los niños han utilizado más recursos de los disponibles). Muestra un valor distinto de cero cuando totalUsage supera localLicenseQuantity. | Solo lectura |
| allowOverAllocation | Indica si se permite al usuario conceder más recursos a los hijos aunque no haya más que conceder (se permite conceder a pesar del exceso de subvención). Este valor se aplica a todos los recursos de este producto. Si se intenta actualizar allowOverallocation para más de un recurso del mismo producto a diferentes valores, el resultado es aleatorio. | Se puede actualizar cuando operation=Update |
| isPurchasedProduct | true si el producto es un producto de compra (no asignado por el principal). Esto equivale a que sourceLicenseId tenga un valor vacío. | Solo lectura |
| redistribuible | true si el producto se puede asignar a tareas secundarias, false significa que el producto solo está disponible en la organización en la que se muestra y que los recursos no se pueden asignar a otra organización. | Solo lectura |
| operación | Uno de los espacios en blanco, Crear, Actualizar o Eliminar. Acción que se debe realizar al importar datos. |                                                          |


**Requisitos de importación**

**Validación de datos**

- El campo de operación debe tener una operación válida.
- Los datos de importación del producto deben tener propiedades y valores para los campos obligatorios.
- Las propiedades de los datos de importación del producto deben ser del tipo correcto.
- El campo de directiva de producto (overAllocation) no debe proporcionarse para recursos diferentes.
- El campo grantedQuantity:
   - No se puede cambiar a *ilimitado* si aún no es *ilimitado*.
   - Debe ser un entero no negativo o el valor de cadena *ilimitado.*

**Validación de permiso/acceso**

- La organización asociada con los datos de importación debe existir. Si está actualizando, asegúrese de que el producto y el recurso asociados con los datos de importación existan realmente.

**Agregar validación de producto**

- SourceLicenseId debe existir.
- La organización asociada al nuevo producto debe existir.
- El producto que se está creando no debe existir (producto con el mismo ID de licencia).
- Los recursos asociados con un producto que se está creando deben tener un productId correspondiente que coincida con ese producto.

