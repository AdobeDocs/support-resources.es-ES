---
title: 'Administración de resultados en el portal de [!DNL Adobe Success] '
description: Esta guía explica cómo consultar, interpretar y aprovechar los resultados del portal de [!DNL Adobe Success] para ayudarle a administrar de forma proactiva los riesgos de rendimiento, seguridad y funcionalidad del producto.
exl-id: c787ce29-993c-498c-9e39-8a04c2eeedda
source-git-commit: f23f0debcd6a0e2962524de321d436b854001495
workflow-type: ht
source-wordcount: '864'
ht-degree: 100%

---

# Administración de resultados en el portal de [!DNL Adobe Success]

Esta guía explica cómo acceder, interpretar y aprovechar los resultados del portal de [!DNL Adobe Success] para administrar de forma proactiva los riesgos de rendimiento, seguridad y funcionalidad del producto.

La página **[!UICONTROL Resultados]** del portal de [!DNL Adobe Success] muestra los problemas o riesgos detectados en la instancia de producto de Adobe. Los resultados incluyen problemas de rendimiento, seguridad y funcionalidad, así como su estado y nivel de riesgo. La monitorización de esta página ayuda a solucionar los problemas desde el principio, antes de que afecten a sus entornos.

**¿Qué son los resultados?**

Los resultados son alertas de Asistencia y datos mostradas en el portal de [!DNL Adobe Success]. Resaltan posibles problemas en la configuración del producto de Adobe, como ralentizaciones del rendimiento, riesgos de seguridad o configuraciones incorrectas. Estas alertas se basan en datos de telemetría recopilados de herramientas como las API, [!DNL New Relic] y [!DNL Splunk].

**¿Cómo se crean los resultados?**

Los equipos de Adobe estudian de forma regular los problemas y las tendencias de asistencia más comunes. En función de los datos, añaden nuevas comprobaciones al sistema. Una vez al día, el portal de [!DNL Adobe Success] analiza los datos de los productos para detectar problemas, como errores de configuración, trabajos atascados o cualquier elemento que pueda provocar una interrupción del sistema. Si una comprobación encuentra algo fuera del intervalo seguro (tal como lo definen los equipos de producto y asistencia de Adobe), se muestra como un resultado.

**Por qué son importantes los resultados**

La revisión periódica de los resultados ayuda a detectar los problemas desde el principio, antes de que afecten al sistema o a los clientes. Este enfoque proactivo mejora la estabilidad del sistema, reduce el tiempo de inactividad y apoya las prácticas recomendadas.

**Cómo corregir los resultados**

Cada resultado incluye recomendaciones e instrucciones claras sobre cómo resolver el problema, junto con vínculos a la documentación relevante, si está disponible. Comparta estos resultados con el equipo de TI o de ingeniería, o con su socio de Adobe, y colaboren para abordarlos. La solución temprana de estos problemas ayuda a evitar problemas mayores y mantiene el sistema funcionando sin problemas.


## Acceso a los resultados

Para ver los resultados de un producto, siga estos pasos:

1. Vaya a **[!UICONTROL Asistencia y datos]**.
1. Seleccione la tarjeta de producto correspondiente. Seleccione la pestaña **[!UICONTROL Resultados]**.

   ![Portal de Adobe Success que resalta los hallazgos en AEM as Cloud Service: Assets con tres elementos enumerados](../../assets/asp-support-inisghts-findings.png "Ver los resultados para AEM Assets en Cloud Service")


1. Verá una lista de todos los resultados del producto seleccionado.

   ![Portal de Adobe Success que muestra la pestaña Conclusiones para AEM Cloud Service: Assets con los problemas de almacenamiento en caché enumerados](../../assets/adobe-success-portal-findings.png "Vea los resultados relacionados con el almacenamiento en caché para AEM Assets en Cloud Service")

1. Desde ahí, puede realizar lo siguiente:

   ![La interfaz del portal de Adobe Success resalta la barra de búsqueda, el botón de descarga y un resultado de riesgo grave en AEM Sites](../../assets/adobe-success-portal-download.png "Buscar, descargar o ver los resultados de AEM Sites en Cloud Service")

   * Buscar entradas específicas.
   * Exportar la lista de resultados seleccionando **[!UICONTROL Descargar resultados]**. Para exportar un informe de un resultado, seleccione la casilla de verificación situada junto al resultado correspondiente en la columna **[!UICONTROL Nombre del resultado]**. Si no selecciona un resultado, el PDF contiene de forma predeterminada una lista de todos los resultados.
   * Vea los detalles de un resultado, incluida una resolución recomendada, seleccionando un resultado en **[!UICONTROL Nombre del resultado]**. La página Detalles del resultado muestra el resultado seleccionado con contexto adicional y una recomendación. Para ver este informe, seleccione la flecha de descarga.


     ![Botón de descarga para exportar los detalles de búsqueda en el portal de Adobe Success](../../assets/findings-details.png "Descargar el informe de este hallazgo")


## Acciones de resultados

Siga estos pasos para validar si cada resultado sigue siendo aplicable o puede ignorarse.

>[!NOTE]:
>
>Las comprobaciones estándar se ejecutan en las instancias. Si las comprobaciones no determinan que el problema está presente en su instancia, existe un estado de **[!UICONTROL No detectado]**.

1. Vaya a **[!UICONTROL Asistencia y datos]**.
1. Seleccione la tarjeta de producto correspondiente.
1. Abra la pestaña **[!UICONTROL Resultados]**. Verá todos los resultados del producto seleccionado.
1. Seleccione una entrada en **[!UICONTROL Nombre del resultado]**. En la página Detalles del resultado puede hacer lo siguiente:
   * Seleccione **[!UICONTROL Validar]** para comprobar si el problema sigue presente (el botón **[!UICONTROL Validar]** está diseñado para confirmar que el problema se ha resuelto):

   ![Botón Validar en el panel Conclusiones para confirmar la resolución del problema en el portal de Adobe Success](../../assets/adobe-success-portal-validate.png "Botón Validar")


   * Si el problema persiste, se mostrará el siguiente mensaje: *[!UICONTROL Validación completada. El resultado sigue detectándose]*. Utilice la información y la recomendación de la página Detalles del resultado para investigarlo y resolverlo.
   * Si el problema ya no está presente, se muestra el siguiente mensaje: *[!UICONTROL Validación completada. El resultado ya no se detecta]*. Cuando el resultado ya no se detecta, se atenúa y el estado cambia a **[!UICONTROL No detectado]**. Los resultados con el estado **[!UICONTROL No detectado]** se encuentran en la parte inferior de la lista de resultados.
   * Si el problema no es aplicable ni relevante para usted, puede descartarlo seleccionando **[!UICONTROL Descartar]**. Cuando se descarta el resultado, se atenúa y el estado cambia a **[!UICONTROL Descartado]**.  Los resultados con el estado **[!UICONTROL Descartado]** se encuentran en la parte inferior de la lista de resultados.

## Comprensión de los resultados

* **[!UICONTROL Nombre del resultado]**: selecciónelo para obtener información detallada y los pasos de resolución recomendados.
* **[!UICONTROL Tipo]**: clasificado como *Funcionalidad*, *Rendimiento* y *Seguridad*.
* **[!UICONTROL Nivel de riesgo]**: indicador de gravedad, con indicadores visuales.
* **[!UICONTROL Estado]**: estado actual del resultado (p. ej., *Detectado*, *No detectado*, *Descartado*).
* **[!UICONTROL Comprobar última ejecución]**: marca de tiempo de la última comprobación que actualizó el resultado.


## Prácticas recomendadas

La página **[!UICONTROL Resultados]** enumera recomendaciones con los siguientes niveles de riesgo: **[!UICONTROL Alto]**, **[!UICONTROL Elevado]** y **[!UICONTROL Medio]**. **[!UICONTROL Alto]** es crítico, **[!UICONTROL Elevado]** es urgente y **[!UICONTROL Medio]** no es crítico. Para mantener el estado y el rendimiento del sitio, siga estos pasos:

* Aborde los resultados de **[!UICONTROL riesgo Alto]** con celeridad, ya que representan amenazas críticas.
* Resuelva los problemas de riesgo **[!UICONTROL Elevado]** pronto para evitar que se escalen.
* Monitorice los resultados de riesgo **[!UICONTROL Medio]** con regularidad y actúe según sea necesario.
