---
title: Contraer errores de secciones
description: Las secciones contraíbles UGP-13446 no se representan, tal vez debido a pestañas de página incrustadas
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# Secciones contraíbles

<http://jira.corp.adobe.com/browse/UGP-13446> Las secciones contraíbles UGP-13446 no se representan, tal vez debido a pestañas de página incrustadas

## Ejemplos

Primero con fichas de página; segundo sin fichas

### Opción 2: con fichas de página

+++ Instalación manual de revisión para 6.5.18.0 - 6.5.22.0

**Paso 1: Descargar y extraer el paquete de revisión**

- Descargar la revisión [para 6.5.18.0 - 6.5.22](https://www.adobe.com) desde el Portal de distribución de software de Adobe
- Extraerlo localmente

**Paso 2: Vaya a la carpeta de versiones correcta**

- En función de la versión del paquete de servicio instalada en su entorno, vaya a la carpeta correspondiente.

  Ejemplo de Service Pack 20: la carpeta es:

  ```
  <extracted-hotfix>/SP20/
  ```

**Paso 3: Busque el directorio de implementación**

- En el servidor AEM Forms en JEE, vaya a:

  ```
  [AEM installation directory]/deploy
  ```

  Ejemplo: `adobe/adobe-experience-manager-forms/deploy`



**Paso 4: actualizar y reemplazar los archivos EAR**

>[!BEGINTABS]

>[!TAB JBoss]

1. Abra `adobe-core-jboss.ear` y reemplace `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. Dentro de `adobe-core-jboss.ear`, vaya a la carpeta `lib/` y reemplace `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salva la OREJA. Asegúrese de que los cambios se hayan guardado correctamente.


1. Reemplazar `adobe-edcserver-jboss.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. Reemplazar `adobe-forms-jboss.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. Abra `adobe-core-weblogic.ear` y reemplace `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. Dentro de `adobe-core-weblogic.ear`, reemplazar `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salva la OREJA. Asegúrese de que los cambios se hayan guardado correctamente.


1. Reemplazar `adobe-edcserver-weblogic.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. Reemplazar `adobe-forms-weblogic.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. Abra `adobe-core-websphere.ear` y reemplace `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. Dentro de `adobe-core-websphere.ear`, reemplazar `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salva la OREJA. Asegúrese de que los cambios se hayan guardado correctamente.


1. Reemplazar `adobe-edcserver-websphere.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. Reemplazar `adobe-forms-websphere.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Paso 5: actualizar `adobe-rightsmanagement-<appserver>-dsc.jar`archivo con**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Paso 6: Configuración adicional para Document Security en WebSphere y WebLogic**:

Si utiliza Document Security (anteriormente Rights Management), establezca la siguiente propiedad del sistema Java (argumento JVM) antes de iniciar el servidor de AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Paso 7: Vuelva a ejecutar el Administrador de configuración**

- Inicie el Administrador de configuración para volver a implementar el EAR actualizado y aplicar la revisión

+++

### Opción 2: sin pestañas de página

+++ Instalación manual de revisión para 6.5.18.0 - 6.5.22.0

**Paso 1: Descargar y extraer el paquete de revisión**

- Descargar la revisión [para 6.5.18.0 - 6.5.22](https://www.adobe.com) desde el Portal de distribución de software de Adobe
- Extraerlo localmente

**Paso 2: Vaya a la carpeta de versiones correcta**

- En función de la versión del paquete de servicio instalada en su entorno, vaya a la carpeta correspondiente.

  Ejemplo de Service Pack 20: la carpeta es:

  ```
  <extracted-hotfix>/SP20/
  ```

**Paso 3: Busque el directorio de implementación**

- En el servidor AEM Forms en JEE, vaya a:

  ```
  [AEM installation directory]/deploy
  ```

  Ejemplo: `adobe/adobe-experience-manager-forms/deploy`



**Paso 4: actualizar y reemplazar los archivos EAR**

Fichas de página eliminadas

**Paso 5: actualizar `adobe-rightsmanagement-<appserver>-dsc.jar`archivo con**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Por ejemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Paso 6: Configuración adicional para Document Security en WebSphere y WebLogic**:

Si utiliza Document Security (anteriormente Rights Management), establezca la siguiente propiedad del sistema Java (argumento JVM) antes de iniciar el servidor de AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Paso 7: Vuelva a ejecutar el Administrador de configuración**

- Inicie el Administrador de configuración para volver a implementar el EAR actualizado y aplicar la revisión

+++

Fin
