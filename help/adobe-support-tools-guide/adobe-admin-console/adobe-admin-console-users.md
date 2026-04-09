---
title: Usuarios de Adobe Admin Console
description: 'Planifique su estrategia para administrar usuarios en Adobe Admin Console: añada administradores y usuarios finales, elija un método de administración de usuarios y asigne licencias.'
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Usuarios de Adobe Admin Console

Se aplica a empresas y equipos.

¿Enfrentando uno de estos problemas? Seleccione un problema para ver su resolución.

- [Administrar roles de administrador](https://helpx.adobe.com/enterprise/using/admin-roles.html)
- [Problemas de descarga e instalación](https://helpx.adobe.com/download-install.html)
- [Restablecer contraseña de usuario de Enterprise ID](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#faq)
- [Resolver errores de Federated ID](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [Eliminar usuario o restaurar usuario eliminado](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - Usuarios** — [Ver en YouTube](https://youtu.be/w8b36YX2TEM)

## Razones para añadir usuarios a Adobe Admin Console

>[!NOTE]
>
>Como administrador en Adobe Admin Console, después de elegir tu [tipo de identidad](https://helpx.adobe.com/es/enterprise/using/identity.html) y [configurar identidad](https://helpx.adobe.com/es/enterprise/using/set-up-identity.html), tu siguiente tarea es agregar usuarios a Admin Console.

Los equipos de Adobe enterprise y definen, en términos generales, dos tipos de usuarios:

### Administradores (administradores)

Los administradores de empresa o de equipos realizan tareas administrativas en Admin Console. Agregue administradores para definir una jerarquía administrativa flexible que permita una administración precisa del acceso a los productos de Adobe, su uso y otras tareas administrativas.

Todos los administradores deben añadirse a Admin Console. Al agregarlos, los privilegios administrativos se basan en sus [roles administrativos](https://helpx.adobe.com/enterprise/using/admin-roles.html).

### Usuarios finales

Los usuarios finales son los usuarios de su organización o institución que utilizan los productos y servicios de Adobe que su organización o institución ha obtenido como parte del acuerdo con Adobe.

## Decida su estrategia de administración de usuarios

Según sus necesidades, agrega, quita o actualiza a los usuarios *individualmente* o usa uno de los *métodos de carga en lotes* disponibles. Utilice la siguiente matriz como guía para planificar la administración de usuarios.

>[!NOTE]
>
>Si es un nuevo cliente empresarial o de equipos de Adobe, le recomendamos que revise esta tabla antes de empezar a administrar los usuarios en Admin Console. Los clientes existentes pueden usar esto, especialmente si planean migrar de un tipo de identidad a otro (consulte [Editar tipo de identidad](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>Individualmente (Admin Console)</strong></th>
<th scope="col"><strong>Carga masiva de CSV (Admin Console)</strong></th>
<th scope="col"><strong>Conectores Azure/Google</strong></th>
<th scope="col"><strong>Herramienta de sincronización de usuarios</strong></th>
<th scope="col"><strong>API de REST de administración de usuarios</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Se aplica a</strong></th>
<td colspan="2">Equipos de Adobe y clientes empresariales</td>
<td colspan="3">clientes empresariales de Adobe</td>
</tr>
<tr>
<th scope="row"><strong>Descripción</strong></th>
<td>Administre a los usuarios individualmente en Admin Console.</td>
<td>Administre usuarios con carga de archivo CSV en Admin Console.</td>
<td>Administre usuarios (y grupos) según el portal de Azure AD o la federación de Google existentes.</td>
<td colspan="2">Administre usuarios (y grupos) según el LDAP de su organización.</td>
</tr>
<tr>
<th scope="row"><strong>Agregar usuarios</strong></th>
<td>Pestaña <strong>Usuarios</strong> en <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#add-users">Más información</a>.</td>
<td>Use <strong>Agregar usuarios mediante CSV</strong> en <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">Más información</a>. <em>(Usar plantilla CSV predeterminada.)</em></td>
<td>Agregar usuarios en <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>. O mediante <strong>Admin Console</strong>.</td>
<td colspan="2">Los usuarios deben añadirse al LDAP de su organización.</td>
</tr>
<tr>
<th scope="row"><strong>Quitar usuarios</strong></th>
<td>Seleccione y elimine un usuario en <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#remove-users">Más información</a>.</td>
<td>Elija <strong>Quitar usuarios con el CSV</strong> en la ficha <strong>Usuarios</strong> de <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#remove-users">Más información</a>. <em>(Usar plantilla CSV predeterminada.)</em></td>
<td>Los usuarios deben ser eliminados en <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Asegúrese de que la información del usuario esté sincronizada. <strong>Precaución:</strong> Los usuarios que no están en el LDAP de su organización se eliminan de Admin Console.</td>
</tr>
<tr>
<th scope="row"><strong>Editar detalles del usuario</strong></th>
<td>Seleccione al usuario y luego <strong>Editar detalles del usuario</strong> en Admin Console. <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#edit-user-details">Más información</a>.</td>
<td>Elija <strong>Editar detalles del usuario mediante CSV</strong> en la ficha <strong>Usuarios</strong> de <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#edit-user-details">Más información</a>. <em>(Usar plantilla CSV predeterminada.)</em></td>
<td>Toda la información del usuario debe cambiarse en <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Asegúrese de que la información del usuario esté sincronizada.</td>
</tr>
<tr>
<th scope="row"><strong>Tipos de identidad admitidos</strong></th>
<td colspan="2">Todas</td>
<td>Federated ID</td>
<td colspan="2">FEDERATED ID y ENTERPRISE ID</td>
</tr>
<tr>
<th scope="row"><strong>Máx. actualizaciones por operación</strong></th>
<td>10</td>
<td>25.000 (<em>5.000 para un rendimiento óptimo</em>)</td>
<td colspan="3">Ilimitado (se asigna al LDAP de su organización)</td>
</tr>
<tr>
<th scope="row"><strong>Requiere</strong></th>
<td>Adobe Admin Console</td>
<td>Crear y actualizar formatos de archivo .csv, preferiblemente con Microsoft Excel</td>
<td>Debe configurar Azure AD o la federación de Google</td>

<td>
  <ul>
    <li>Terminal de macOS o Símbolo del sistema de Windows</li>
    <li>Comprensión de LDAP</li>
  </ul>
</td>

<td>Conocimientos prácticos de un lenguaje de programación (como Python) para consumir API de REST</td>
</tr>
<tr>
<th scope="row"><strong>Más información</strong></th>
<td><a href="https://helpx.adobe.com/es/enterprise/using/manage-users-individually.html">Administración de usuarios individuales</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">
        Administración de usuarios | Cargar CSV en lotes
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        Solución de problemas de carga masiva de CSV de usuario
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">
        Conector de Azure AD
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">
        Conector de federación de Google
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        Acerca de la sincronización de usuarios
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Repositorio Git
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/user-sync.html">
        Guía paso a paso
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">Acerca de UMAPI</a></td>
</tr>
</tbody>
</table>

## Próximos pasos

### Creación de paquetes

Una vez añadidos, los usuarios están listos para recibir sus aplicaciones y servicios designados.

Asigne licencias a los usuarios finales en función de su método de licencia:

- **Licencias de usuario con nombre:** Agregue estos usuarios a **productos** ([para equipos](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)) o a **perfiles de producto** ([para empresas](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html)) para darles derechos de producto y servicio de Adobe. Para obtener más información, vea cómo [crear paquetes de licencias de usuario con nombre](https://helpx.adobe.com/enterprise/using/create-nul-packages.html) y [perfiles de producto](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#create-product-profile).
- **Licencias de dispositivos compartidos:** [Se agregaron usuarios](https://helpx.adobe.com/enterprise/using/sdl-deployment-guide.html#add-users-admin-console) que pueden usar los dispositivos compartidos configurados a los que solo tienen acceso **usuarios de la organización**. Para obtener más información, consulte [Crear paquetes de SDL](https://helpx.adobe.com/enterprise/using/create-sdl-packages.html).

### Implementación de paquetes

Una vez creado el paquete, impleméntelo en los equipos cliente mediante uno de estos métodos:

- Vaya al equipo cliente y haga doble clic en el archivo del paquete (Windows o macOS).
- Utilice el símbolo del sistema de Windows o el terminal de macOS.
- Utilice herramientas de terceros:
   - [Microsoft Intune](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Administrador de configuración de Microsoft System Center (SCCM)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-sccm.html)
   - [Escritorio remoto de Apple (ARD)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-munki.html)

## Lectura relacionada

- [Administrar usuarios | Individualmente](https://helpx.adobe.com/es/enterprise/using/manage-users-individually.html)
- [Administrar usuarios | Cargar CSV en lotes](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)
- [Administrar usuarios de directorio](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html)
- [Asignar usuarios a perfiles de producto (para empresas e instituciones)](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#assign-users)
- [Asignar licencias a equipos y usuarios](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)
- [Modelo de almacenamiento empresarial](https://helpx.adobe.com/enterprise/kb/business-storage-model-introduction.html)