---
title: Prácticas recomendadas y estabilidad
description: Prácticas recomendadas y recomendaciones de estabilidad para ayudar a los comerciantes de Adobe Commerce a preparar sus entornos para eventos de alto tráfico como la temporada de vacaciones.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# Prácticas recomendadas y estabilidad

En esta sección se proporcionan recomendaciones técnicas para la preparación de entornos de Adobe Commerce, tanto de Commerce en infraestructura en la nube como locales, para eventos de alto tráfico como la temporada de vacaciones.

>[!NOTE]
>
>Los pasos marcados **(solo en la nube)** se aplican a Commerce en la infraestructura en la nube. La mayoría de las demás recomendaciones también se aplican a las implementaciones locales.

## Actualice a la versión más reciente de Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

Asegúrese de que el sitio no tenga una versión no compatible de Adobe Commerce, lo que puede afectar al rendimiento del sitio y aumentar la vulnerabilidad a los problemas de seguridad. Actualice a la última versión de Adobe Commerce para estar seguro y listo para la temporada de vacaciones.

La [última versión](https://experienceleague.adobe.com/es/docs/commerce-operations/release/notes/overview) de Adobe Commerce incluye [correcciones de seguridad críticas](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/security-patches/overview), incluidas mejoras y problemas mitigados, que beneficiarán a su proyecto al actualizar desde una versión anterior.

Para obtener más información sobre las versiones no compatibles de Adobe Commerce, revise la [Directiva de ciclo de vida de Adobe Commerce](https://experienceleague.adobe.com/es/docs/commerce-operations/release/planning/lifecycle-policy).

## Instale las últimas herramientas ECE y herramienta de parche de calidad (QPT) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

Asegúrese de que el módulo `ece-tools` más reciente y sus módulos dependientes estén instalados mediante el conmutador `--with-dependencies`, de modo que todos los parches de nube necesarios estén correctamente instalados para su versión de Adobe Commerce. Para ver los pasos, consulte [Actualizar el paquete ECE-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package).

Revise la lista de parches disponible en la herramienta Parches de Calidad y asegúrese de que se han aplicado los parches de rendimiento compatibles con su versión de Adobe Commerce. Ver [Herramienta Parches de calidad: buscar parches](https://experienceleague.adobe.com/es/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview).

>[!NOTE]
>
>QPT está disponible tanto para Adobe Commerce en la infraestructura en la nube como para instalaciones locales. Los comandos de instalación y uso difieren entre los dos: para Cloud, QPT se incluye con el paquete ECE-Tools.

## Revisar y limpiar archivos de registro {#review-and-clean-log-files}

Revise los archivos de registro en el entorno de la nube (por ejemplo, los archivos de registro de la aplicación bajo `~/var/log`) e identifique los registros que se escriben con frecuencia en los archivos de registro personalizados o predeterminados. Para obtener más información, consulte [Ver y administrar registros](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

* Revise los siguientes archivos de registro predeterminados y corrija los errores recurrentes: `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* Quite los registros de depuración que se agregaron anteriormente para solucionar problemas anteriores.

Estos registros también están disponibles en [!DNL New Relic], consulte [Administración de registros de New Relic](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Monitorización del crecimiento del tamaño del disco {#monitor-disk-size-growth}

La infraestructura de Adobe Commerce en la nube tiene dos volúmenes de disco principales. Supervise estos volúmenes para asegurarse de que tienen suficiente espacio libre cuando hay mucho tráfico. Adobe Commerce proporciona una advertencia cuando cualquiera de los volúmenes supera el 70 % de uso.

* `/mnt/shared` (archivos compartidos, incluidos registros y archivos multimedia)
* `/data/mysql` (volumen de base de datos)

Para obtener más información, consulte [Administrar espacio en disco](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space).

## Revisar solicitudes de base de datos más lentas {#review-slowest-database-requests}

Es importante supervisar y revisar con regularidad las transacciones de base de datos que llevan más tiempo en [!DNL New Relic]. Investigue consultas y componentes significativamente lentos.

* **Comprueba las transacciones que consumen más tiempo:** Ve a **[!UICONTROL New Relic]** > **[!UICONTROL APM y servicios]** > selecciona entorno > **[!UICONTROL Bases de datos]** y, a continuación, ordénalas por las transacciones que consumen más tiempo.

* **Compruebe el registro de consultas lentas de MySQL:** Revise `mysql-slow.log` para consultas lentas registradas por el sistema. Estos registros también están disponibles en [!DNL New Relic]: vaya a **[!UICONTROL New Relic]** > **[!UICONTROL Registros]** y filtre por `filePath:"/var/log/mysql/mysql-slow.log"`.

Revise los [!DNL MySQL] registros de consultas lentas con regularidad para confirmar que las consultas lentas no se ejecutan con frecuencia. Para ver los pasos para resolver consultas que identifique como problemáticas, consulte [Resolver problemas de rendimiento de bases de datos](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues).

## Configuración de trabajos cron {#configure-cron-jobs}

Todas las operaciones asincrónicas en Commerce se realizan con el comando cron de Linux.

Commerce depende de la configuración adecuada del trabajo cron para las funciones importantes del sistema, incluidas las operaciones de indexación y de consumo en cola. Si no se configura correctamente, Commerce no funcionará como se espera.

Es fundamental que Commerce cron esté configurado correctamente, utilizando el usuario Unix adecuado en el archivo crontab de Unix. Cada usuario de Unix tiene su propio archivo crontab, que es la configuración utilizada para ejecutar trabajos cron para ese usuario. Para ver los pasos, consulte [Configurar y ejecutar trabajos cron](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs).

El script `dev/tools/cron.sh` ya no se puede ejecutar porque se ha eliminado.

## Optimizar configuración del lado del cliente {#optimize-client-side-settings}

Para mejorar la capacidad de respuesta de la tienda en su instancia de Commerce, configure las siguientes opciones en **[!UICONTROL Tiendas]** > **[!UICONTROL Configuración]** > **[!UICONTROL Avanzado]** > **[!UICONTROL Desarrollador]**, que solo está disponible en el modo de Desarrollador:

* **[!UICONTROL Configuración de cuadrícula]** > **[!UICONTROL Indexación asincrónica]**: *[!UICONTROL Habilitar]*
* **[!UICONTROL Configuración de CSS]** — **[!UICONTROL Minimizar archivos CSS]**: *[!UICONTROL Sí]*
* **[!UICONTROL Configuración de JavaScript]** — **[!UICONTROL Minimizar archivos de JavaScript]**: *[!UICONTROL Sí]*
* **[!UICONTROL Configuración de JavaScript]** — **[!UICONTROL Habilitar agrupación de JavaScript]**: *[!UICONTROL Sí]* (no habilitado de forma predeterminada)
* **[!UICONTROL Configuración de plantilla]** — **[!UICONTROL Minificar HTML]**: *[!UICONTROL Sí]*

Dado que Adobe Commerce en la nube siempre se ejecuta en el modo de producción, establezca cada opción en la línea de comandos (por ejemplo, `bin/magento config:set --lock-config dev/css/minify_files 1`), confirme el cambio `app/etc/config.php` resultante y vuelva a implementarla. Para obtener la lista completa de rutas CLI, consulte [Optimizar archivos de recursos](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files).
