---
title: Monitorización y observabilidad
description: Recomendaciones de monitorización y observabilidad para ayudar a los comerciantes de Adobe Commerce a preparar sus entornos para eventos de alto tráfico como la temporada de vacaciones.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
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
source-wordcount: '517'
ht-degree: 2%
---

# Monitorización y observabilidad

En esta sección se proporcionan recomendaciones técnicas para monitorizar los entornos de Adobe Commerce a fin de prepararse para eventos de alto tráfico como la temporada de vacaciones.

>[!NOTE]
>
>Los pasos marcados **(solo en la nube)** se aplican a Commerce en la infraestructura en la nube. La mayoría de las demás recomendaciones también se aplican a las implementaciones locales.

## Monitorización del tráfico con New Relic (solo en la nube) {#monitor-traffic-with-new-relic}

Adobe Commerce en la infraestructura en la nube incluye una suscripción a la plataforma de observabilidad [!DNL New Relic], que incorpora sin problemas [!DNL Fastly] registros de streaming a [!DNL New Relic] en tiempo casi real. Esta integración le permite monitorizar los patrones de tráfico y las tendencias en tiempo real, para que pueda tomar medidas correctivas.

Utilice estos registros para:

* Identifique los países desde donde se originan las solicitudes web.
* Encuentre direcciones IP o agentes de usuario abusivos que rastreen por su sitio.
* Identificar el tráfico malintencionado dirigido a extremos específicos, como el pago.
* Cree informes sobre los tipos de dispositivos y exploradores que utilizan sus clientes.

Por ejemplo, monitorice el país de origen del tráfico para confirmar que refleja la ubicación geográfica de las promociones y los clientes:

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

Modifique esta consulta para adaptarla a sus necesidades, segméntela más o conviértala en un tablero para el seguimiento centralizado. Para obtener más información, consulte [Administración de registros de New Relic](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Personalizar alertas de New Relic (solo en la nube) {#customize-new-relic-alerts}

Además de las alertas administradas configuradas por Adobe Commerce en la infraestructura en la nube, puede establecer una amplia gama de alertas y notificaciones para su plataforma durante la temporada de máxima venta, por ejemplo, para notificarle sobre el tráfico de bots o sobre un mayor tiempo de respuesta en una consulta de GraphQL. Consulte [Alertas administradas para Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce) para obtener la lista completa de alertas integradas.

[!DNL New Relic] alertas e IA admiten estructuras de consulta basadas en NRQL. Configure alertas personalizadas del panel [!DNL New Relic] en **[!UICONTROL Alertas e IA]**.

## Revisar puntuación de Apdex (solo en la nube) {#review-apdex-score}

La puntuación Apdex mide la satisfacción del usuario con el tiempo de respuesta de sus aplicaciones y servicios web. Puede revisar la puntuación de Apdex de su Adobe Commerce en la infraestructura en la nube mediante [!DNL New Relic].

Una puntuación Apdex varía de 0 a 1. Una puntuación de 0 es la peor puntuación posible, lo que significa que el 100 % de los tiempos de respuesta estaban **frustrados**. Una puntuación de 1 es la mejor puntuación posible, lo que significa que el 100 % de los tiempos de respuesta fueron **satisfechos**. [!DNL New Relic] informa de una puntuación del servidor de aplicaciones, que refleja el rendimiento del back-end, y de una puntuación del usuario final, que refleja el rendimiento del lado del cliente.

Una puntuación Apdex de 0,5 o inferior justifica una investigación. Una puntuación inferior a 0,4 se considera una interrupción del servicio.

Junto con Apdex, [!DNL New Relic] proporciona una serie de estadísticas para analizar los problemas de rendimiento en Adobe Commerce en la infraestructura en la nube. Para ver los pasos, consulte [Solucionar problemas de rendimiento con New Relic en Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce).

## Revisar perspectivas de asistencia (informe SWAT) {#review-support-insights-swat-report}

Para obtener un informe más detallado sobre su entorno, genere un informe de Herramienta de análisis de todo el sitio (SWAT). Para obtener más información acerca de la herramienta SWAT, vea [Herramienta de análisis de todo el sitio](https://experienceleague.adobe.com/es/docs/commerce-operations/tools/site-wide-analysis-tool/intro).