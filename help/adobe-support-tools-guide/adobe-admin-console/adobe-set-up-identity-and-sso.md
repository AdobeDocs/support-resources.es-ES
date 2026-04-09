---
title: Configurar la identidad y el inicio de sesión único
description: Descubra cómo los administradores del sistema de la organización pueden configurar la identidad de usuario y el inicio de sesión único (SSO) en Adobe Admin Console mediante Adobe ID, Enterprise ID o Federated ID.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# Configurar la identidad y el inicio de sesión único

**Se aplica a:** Empresa

Obtenga información sobre cómo configurar la identidad en Adobe Admin Console. Compare Adobe ID, Enterprise ID y Federated ID, y configure el inicio de sesión único (SSO) para el acceso seguro a las aplicaciones de Adobe.

Configure la identidad y el inicio de sesión único (SSO) para que los empleados puedan [iniciar sesión](https://adminconsole.adobe.com/settings/) con las credenciales de la organización existentes.

Este es el tutorial en vídeo de cómo [configurar la identidad y el SSO (YouTube)](https://youtu.be/V57lU4zaSBs).

## Términos y conceptos clave

### Directorio

Un directorio en Admin Console es una entidad que contiene recursos como usuarios y directivas como autenticación. Estos directorios son similares a LDAP o Active Directories.

### Proveedor de identidad (IdP)

Un proveedor de identidad (IdP) es el proveedor de identidad de su organización, como:

- Active Directory
- Microsoft Azure
- Ping
- Okta
- InCommon
- Shibboleth

### Personas involucradas

| Función | Responsabilidad |
|------|----------------|
| Administrador del sistema | Funciona con administradores de directorios IdP y administradores DNS para configurar la identidad en Admin Console. |
| Administrador de DNS | Actualiza los tokens DNS para validar la propiedad del dominio. |
| Administrador del directorio del proveedor de identidad (IdP) | Controla el portal IdP y los conectores asociados. |

### Adobe ID

Creado, propiedad y administrado por el usuario final. Adobe realiza la autenticación y el usuario final la administra. Según el [modelo de almacenamiento](https://helpx.adobe.com/es/enterprise/using/storage-for-business.html), los usuarios o las empresas conservan el control sobre los archivos y los datos.

Para las organizaciones que se han actualizado al modelo de almacenamiento empresarial, los recursos y los datos están controlados por la organización. En el caso de las organizaciones que no se han actualizado, el individuo posee y controla recursos de Adobe ID.

### Enterprise ID

Creado, propiedad y administrado por una organización. Adobe aloja Enterprise ID y realiza la autenticación, pero la organización mantiene Enterprise ID. Los administradores crean un Enterprise ID y lo emiten a un usuario. Los administradores pueden revocar el acceso a los productos y servicios al hacerse cargo de la cuenta o eliminar Enterprise ID para bloquear permanentemente el acceso a los datos asociados. Para obtener más información, haga clic [aquí](https://helpx.adobe.com/es/enterprise/using/setup-enterprise-id.html).

### Federated ID

Creado y propiedad de una organización y vinculado al directorio empresarial mediante federación. La organización administra credenciales y procesa el inicio de sesión único a través de un proveedor de identidad SAML2 (IdP).

A continuación se indican algunos requisitos y escenarios en los que se recomiendan Federated ID:

- Si desea aprovisionar usuarios en función del directorio empresarial de su organización.
- Si desea administrar la autenticación de usuarios.
- Si necesita mantener un control estricto sobre las aplicaciones y los servicios disponibles para un usuario.

## Configurar la identidad sin inicio de sesión único

Puede utilizar Adobe ID o Enterprise ID si su organización no utiliza actualmente el SSO en otras aplicaciones.

## Uso de Adobe ID

Adobe está actualizando todas las organizaciones al [modelo de almacenamiento empresarial](https://helpx.adobe.com/es/enterprise/using/storage-for-business.html). Esto proporciona a su organización un mayor control sobre los recursos y los datos de los usuarios.

Empiece a [agregar usuarios](https://helpx.adobe.com/es/enterprise/using/users.html) a Admin Console.

## Configuración de la identidad con Enterprise ID

Puede configurar un directorio de Enterprise ID si desea tener más control sobre los datos de los usuarios sin utilizar SSO. Solo los administradores crean una Enterprise ID y la emiten a un usuario.

Consulte [Configurar la organización con Enterprise ID](https://helpx.adobe.com/es/enterprise/using/setup-enterprise-id.html) para conocer los requisitos y pasos para crear directorios de Enterprise ID.

## Configurar la identidad con el inicio de sesión único

Debe configurar la identidad del usuario con cuentas de Federated ID para utilizar SSO.

Se recomiendan los Federated ID cuando:

- Debe mantener un control estricto sobre las aplicaciones y los servicios disponibles para un usuario.
- Desea administrar la autenticación de los usuarios.
- Desea aprovisionar usuarios en función del directorio empresarial de su organización.

## Configuración de una nueva integración de SSO

Puede utilizar proveedores de identidad populares como Microsoft Azure AD, Google u otros ID basados en SAML para configurar el SSO entre su organización y los productos de Adobe.

**Azure AD** (recomendado) - [Configurar SSO y sincronización de usuarios con el conector de Azure AD](https://helpx.adobe.com/es/enterprise/using/sso-setup-azure.html)

**Otro IdP de SAML** - [Configurar SSO con otros proveedores de SAML](https://helpx.adobe.com/es/enterprise/using/create-directory.html)

**Google** (recomendado) - [Configurar SSO y sincronización de usuarios mediante el conector de Google](https://helpx.adobe.com/es/enterprise/using/setup-sso-google.html)

## Administrar configuración de SSO existente

Una vez configurado el SSO entre su organización y Adobe, utilice lo siguiente para administrar y cambiar la configuración.

Obtenga información sobre cómo administrar los dominios y directorios:

- [Administrar usuarios](https://helpx.adobe.com/es/enterprise/using/users.html) y [grupos](https://helpx.adobe.com/es/enterprise/using/user-groups..html)
- [Vincule dominios a directorios](https://helpx.adobe.com/es/enterprise/using/add-domains-directories.html#link-domains-to-directoies) para controlar el acceso de los usuarios a aplicaciones, servicios y configuración
- [Administrar confianza de directorio](https://helpx.adobe.com/es/enterprise/using/directory-trust.html) para usar dominios reclamados por otra organización

Aprenda a cambiar el proveedor de identidad:

- [Cambia tu IdP](https://helpx.adobe.com/es/enterprise/using/migrate-authentication-provider.html) sin interrumpir el trabajo de los usuarios
- [Mover dominios entre directorios](https://helpx.adobe.com/es/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [Quitar usuarios de directorio heredados](https://helpx.adobe.com/es/enterprise/using/manage-directory-users.html)
- [Eliminar dominios antiguos/no reclamados y directorios vacíos](https://helpx.adobe.com/es/enterprise/using/manage-domains-directories.html#delete)

## Errores y preguntas frecuentes

Soluciones para preguntas y errores comunes al configurar y administrar SSO:

### Azure AD: preguntas frecuentes y solución de problemas

#### Preguntas frecuentes

- [Preguntas frecuentes sobre el conector Azure AD](https://helpx.adobe.com/es/enterprise/using/azure-ad-connector-faq.html)
- [Cómo eliminar directorios y dominios](https://helpx.adobe.com/es/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### Solución de problemas

- [Usuarios con acceso denegado](https://helpx.adobe.com/es/enterprise/using/sso-setup-azure.html#sync-issues)
- [Problemas de sincronización](https://helpx.adobe.com/es/enterprise/using/sso-setup-azure.html#sync-issues)

### Otro ID de SAML: preguntas frecuentes y resolución de problemas

#### Preguntas frecuentes

[Preguntas frecuentes sobre la integración de SAML](https://helpx.adobe.com/es/enterprise/using/sso-faq.html)

#### Solución de problemas

- [Solución de problemas generales de SSO](https://helpx.adobe.com/es/enterprise/kb/tshoot-fed-id.html)
- [: error de &quot;Acceso denegado&quot;](https://helpx.adobe.com/es/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [&quot;Otro usuario ha iniciado sesión&quot; error](https://helpx.adobe.com/es/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [Realizar un seguimiento de SAML](https://helpx.adobe.com/es/enterprise/kb/perform-a-saml-trace.html)

### Google: Preguntas frecuentes

- [Preguntas frecuentes sobre el conector Google](https://helpx.adobe.com/es/enterprise/using/google-federation-faq.html)
- [Cómo eliminar directorios y dominios](https://helpx.adobe.com/es/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## Únase a la conversación

Para colaborar, hacer preguntas y charlar con otros administradores, usa la [Comunidad de empresas y equipos](https://www.adobe.com/go/entcom_es).

## Legal y privacidad

- [Avisos legales](https://helpx.adobe.com/es/legal/legal-notices.html)
- [Política de privacidad en línea](https://www.adobe.com/es/privacy.html)
