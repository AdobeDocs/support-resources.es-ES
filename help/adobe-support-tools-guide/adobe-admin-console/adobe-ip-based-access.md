---
title: Limitar el acceso al producto por direcciones IP
description: Utilice el acceso basado en IP para controlar el acceso de los usuarios a los productos de Adobe y restringir el uso a intervalos de IP públicos aprobados.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# Limitar el acceso al producto por direcciones IP

Se aplica a la empresa.

Utilice el acceso basado en IP para controlar el acceso de los usuarios a los productos de Adobe y evitar el uso no autorizado de direcciones IP públicas que no estén incluidas en la lista.

Vaya a [Admin Console](https://adminconsole.adobe.com/settings/identity) para agregar direcciones IP públicas de confianza a la lista de permitidos de **acceso basado en IP** para un uso seguro de las aplicaciones y los servicios de Adobe.

## Ventajas del acceso basado en IP

El control de acceso basado en IP utiliza una lista de permitidos de direcciones IP para limitar el uso de productos de Adobe de direcciones IP públicas aleatorias. El acceso basado en IP se aplica a todos los directorios y a los productos asociados en su Adobe Admin Console.

Puede agregar IP públicas de confianza a la lista **Direcciones IP permitidas** para impedir que los usuarios hagan lo siguiente:

- Acceder a productos desde direcciones IP públicas que están fuera de los intervalos de IP permitidos
- Iniciando sesión en Adobe [perfiles de usuario](https://helpx.adobe.com/es/enterprise/using/manage-adobe-profiles.html) desde IP públicas fuera de los intervalos de IP permitidos
- Cambiar perfiles de usuario en aplicaciones web fuera de los intervalos de IP permitidos

  ![Exportar estructura organizativa](./assets/ip-based-access.avif)

## Habilitar el acceso basado en IP

### Consideraciones importantes

>[ !IConsideraciones importantes]
>
>- Los administradores deben empezar agregando su propia dirección IP pública y solo después agregar otros intervalos de IP. De lo contrario, podría sufrir un error.
>- El acceso basado en IP no se aplica a direcciones IP privadas.

Puede añadir hasta 150 intervalos de IP públicas diferentes solo en formato CIDR.

Siga estos pasos para habilitar el acceso basado en IP en Adobe Admin Console:

1. Vaya a la sección **[[!UICONTROL Configuración de Adobe Admin Console]](https://adminconsole.adobe.com/settings/identity)**.
2. Seleccione y expanda **[!UICONTROL Privacidad y seguridad]** en el menú de selección, luego seleccione **[!UICONTROL Configuración de autenticación]**.
3. En la sección **[!UICONTROL Acceso basado en IP]**, seleccione el botón **[!UICONTROL Agregar dirección IP]**.
4. En la ventana **[!UICONTROL Agregar dirección IP]**:
   - Introduzca las direcciones IP públicas o el bloque CIDR que desea añadir a su lista de permitidos.
   - Utilice una coma para separar varias direcciones IP.
   - Seleccione **[!UICONTROL Guardar]**.

   Actualmente sólo se admite el formato IPv4. A continuación se muestran algunos ejemplos:
   - Dirección IP v4: 1.3.4.6
   - Dirección de subred IP v4: 1.2.0.0/24

Sus direcciones IP se añaden en unos minutos. Los usuarios asociados verán la restricción la próxima vez que intenten iniciar sesión o cambiar de perfil fuera de las direcciones IP públicas permitidas. Le recomendamos que informe a sus usuarios con antelación de este cambio.

Puede editar o eliminar cualquier dirección IP de la lista seleccionando las opciones de edición o eliminación junto a cada entrada.

>[!NOTE]
>
>- Cuando el acceso basado en IP está habilitado, **no se produce ningún cierre de sesión forzado**. Los usuarios solo se ven afectados cuando intentan seleccionar el perfil restringido al iniciar sesión o cambiar de perfil en la web.
>- Si utiliza una puerta de enlace web segura, asegúrese de que todo el tráfico se enrute a través de ella. Ver la [lista de dominios a los que se permitirá](https://helpx.adobe.com/es/enterprise/kb/network-endpoints.html) que las aplicaciones y servicios de Adobe funcionen correctamente.
>- Si no puedes acceder a Admin Console porque has escrito una dirección IP no válida, ponte en contacto con el [Servicio de atención al cliente de Adobe](https://helpx.adobe.com/es/enterprise/using/support-for-enterprise.html).

## Únase a la conversación

Para colaborar, hacer preguntas y charlar con otros administradores, visita nuestra [Comunidad de empresas y equipos](https://www.adobe.com/go/entcom_es).
