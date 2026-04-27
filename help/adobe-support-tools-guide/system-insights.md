---
title: System Insights
description: System Insights identifica de forma proactiva posibles problemas en entornos de Adobe Commerce. La revisión de las perspectivas durante la creación de casos reduce el tiempo de resolución, ayuda a evitar interrupciones y admite una implementación estable y segura.
source-git-commit: 4172c364c9bfffaae13759da882d03daa15d0754
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---

# System Insights

System Insights proporciona resultados proactivos que ayudan a identificar posibles problemas de rendimiento, seguridad y funcionalidad en una configuración de producto de Adobe. Estas perspectivas muestran riesgos como la degradación del rendimiento, vulnerabilidades de seguridad o configuraciones incorrectas basadas en datos de telemetría recopilados de herramientas de observabilidad, incluidas API, New Relic y [!DNL Splunk].

Las perspectivas del sistema aparecen durante el proceso de creación de casos y ayudan a acelerar el diagnóstico y la resolución.

## Cómo se crean las perspectivas del sistema

Los equipos de Adobe analizan continuamente los problemas de soporte comunes y las tendencias emergentes. En función de estos resultados, Adobe añade comprobaciones automatizadas al sistema.

Estas comprobaciones analizan la configuración del producto para detectar problemas como configuraciones incorrectas, trabajos atascados o condiciones que podrían provocar problemas funcionales o interrupciones del sistema.

Cuando una comprobación identifica un valor o estado fuera del intervalo seguro definido por los equipos de productos y soporte de Adobe, el sistema lo presenta como un Insight del sistema.

## Por qué importan las perspectivas del sistema

La revisión periódica de las perspectivas del sistema ayuda a identificar los problemas desde el principio, antes de que afecten a la estabilidad del sistema o a la experiencia del cliente. Este enfoque proactivo:

- Mejora la fiabilidad de la plataforma
- Reduce el tiempo de inactividad
- Ayuda a mantener las prácticas recomendadas por Adobe

## Disponibilidad y ámbito

Actualmente, Información del sistema solo está disponible para Adobe Commerce. Estas perspectivas aparecen durante el proceso de creación de casos en Soporte técnico de Experience League y también están disponibles a través de la [Herramienta de análisis de todo el sitio (SWAT)](https://experienceleague.adobe.com/es/docs/commerce-operations/tools/site-wide-analysis-tool/intro).

> [ !Note]
>
>System Insights solo muestra datos para entornos de producción.

## Acceder a System Insights

System Insights aparece en todo el flujo de trabajo de creación de casos. A medida que se introducen los detalles del problema, el panel **[!UICONTROL Información del sistema]** aparece a la derecha de la pantalla, debajo de la sección Recomendaciones con tecnología de IA. Para obtener más información acerca de las recomendaciones con tecnología de IA, consulte [Rellenar el ticket de asistencia](https://experienceleague.adobe.com/es/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket) en el artículo de la experiencia de asistencia al cliente de Adobe.

El panel muestra una lista desplazable de perspectivas enfocadas a la instancia de proyecto específica. El ámbito se basa en la información escrita en el campo **[!UICONTROL Dirección URL del proyecto]**. Escriba la **[!UICONTROL URL del proyecto]** con precisión para asegurarse de que las perspectivas reflejen el entorno correcto.

Una vez cargado el panel, muestra una lista desplazable de tarjetas de insight marcadas para su entorno. Cada tarjeta de insight incluye:

- Un título que resume el problema
- Breve descripción de insight

![Recursos de soporte de acceso](/help/adobe-support-tools-guide/assets/access-support-resources.png)

Para ver todos los detalles de insight, seleccione una tarjeta de insight en la lista. La vista detallada proporciona la siguiente información:

- Nombre de insight
- Producto de Adobe donde insight está marcado
- Tipo de insight, clasificado como:
   - [!UICONTROL Funcionalidad]
   - [!UICONTROL Rendimiento de]
   - [!UICONTROL Seguridad]
- [!UICONTROL Nivel de riesgo] que indica la gravedad
- [!UICONTROL Última ejecución de comprobación] indica cuándo se detectó el hallazgo.
- [!UICONTROL Insight Source], proporcionado por la herramienta de análisis de todo el sitio (SWAT)
- Una explicación detallada del problema y su impacto potencial, junto con pasos procesables para investigar y abordar el problema. En la vista detallada también se explican las causas típicas de este tipo de problemas e incluyen vínculos a la documentación de Adobe correspondiente para obtener más información.

![Tarjeta de caso de clic](/help/adobe-support-tools-guide/assets/click-case-card.png)

Revise todas las perspectivas en el panel antes de continuar, ya que un insight puede abordar directamente el problema que se está experimentando.

## Acción en un insight

Después de revisar una insight, elija una de las siguientes acciones.

### Continuar creación de casos

Si el problema persiste o requiere asistencia adicional, seleccione **[!UICONTROL Continuar creación de caso]**. El sistema conserva toda la información de mayúsculas y minúsculas introducida anteriormente.

### Marcar problema como resuelto

Si insight resuelve el problema y ya no se requiere un caso de soporte, seleccione **[!UICONTROL Problema resuelto]**.

Cuando se selecciona esta opción:

- Aparecerá un cuadro de diálogo de confirmación.
- El cuadro de diálogo indica que todos los datos de mayúsculas y minúsculas introducidos se borrarán de forma permanente.

![Acción en un insight](/help/adobe-support-tools-guide/assets/issue-resolved.png)

Seleccione **[!UICONTROL Listo]** para confirmar y volver a la página **[!UICONTROL Mis casos]**. Seleccione **[!UICONTROL Cancelar]** para volver a la vista de detalles de insight.

![Borrar formulario de caso](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## Proporcionar comentarios sobre una insight

En la parte inferior de cada vista de detalles de insight, se pueden proporcionar comentarios sobre si insight fue útil. Estos comentarios ayudan a Adobe a mejorar continuamente la relevancia y precisión de las Perspectivas del sistema.

![Proporcionar comentarios](/help/adobe-support-tools-guide/assets/submit-feedback.png)

Para proporcionar comentarios:

1. Abra una vista de detalles de insight.
2. Desplácese hasta la parte inferior del panel.
3. Busque el mensaje **[!UICONTROL ¿Le ha resultado útil? Enviar comentarios.]**
4. Seleccione una de las siguientes opciones:
   - **Pulsa** icono si el insight fue útil
   - **Icono de pulgar abajo** si insight no es útil
5. (Opcional) Introduzca comentarios adicionales.
6. Seleccione **[!UICONTROL Enviar]** para enviar comentarios o **[!UICONTROL Descartar]** para cerrar la sección de comentarios sin enviarlos.
