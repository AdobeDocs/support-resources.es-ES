---
title: Resumen de preparación para las fiestas de Adobe Commerce
description: Directrices de nivel ejecutivo para preparar Adobe Commerce en entornos de infraestructura en la nube para eventos de alto tráfico como la temporada de vacaciones.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Resumen de preparación para las fiestas de Adobe Commerce

Este manual proporciona instrucciones para preparar entornos de Adobe Commerce para eventos de alto tráfico, como la temporada de vacaciones. Consolida las recomendaciones técnicas en cinco áreas de enfoque estratégico:

- Optimización del rendimiento
- Prácticas recomendadas y estabilidad
- Monitorización y observabilidad
- Escalabilidad y planificación de capacidades
- Preparación operativa

Estas áreas de enfoque ayudan a garantizar que su plataforma permanezca estable, segura y con rendimiento bajo carga máxima.

## Optimización del rendimiento

A continuación se ofrece una descripción general de los pasos recomendados para garantizar un rendimiento optimizado. Para obtener más información, consulte [Preparación para las fiestas de Adobe Commerce > Optimización del rendimiento](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md).

* Optimizar el almacenamiento en caché de solicitudes de Fastly: normalice los parámetros de seguimiento promocional, confirme que las páginas de aterrizaje se pueden almacenar en caché y utilice GraphQL GET para PWA o tiendas sin encabezado para aumentar la proporción de visitas de caché de Fastly.
* Habilitar Fastly IO: active Fastly Image Optimization y Deep IO para que las transformaciones de imagen se ejecuten en el extremo de la CDN en lugar del origen, lo que reduce el tiempo de procesamiento de la página en tiendas con gran cantidad de imágenes.
* Habilitar la caché L2: almacene los datos de caché localmente en cada nodo web para reducir la latencia y las llamadas de red a Redis/Valkey, según la versión de Adobe Commerce. La caché de Redis no es compatible con Adobe Commerce 2.4.9 ni con versiones de parches posteriores a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 y 2.4.8-p4.
* Habilitar conexiones esclavas: enrute las consultas de lectura pesada a los nodos de réplica con `MYSQL_USE_SLAVE_CONNECTION` y `REDIS_USE_SLAVE_CONNECTION` o `VALKEY_USE_SLAVE_CONNECTION` para que las bases de datos maestras no sean el cuello de botella bajo carga.
* Habilite el procesamiento asincrónico de pedidos y correos electrónicos: coloque pedidos en cola, actualice la cuadrícula de datos de pedidos y cierre de compra de correos electrónicos para que se ejecuten en segundo plano en tres configuraciones independientes. De este modo, el cierre de compra permanece rápido en un volumen de pedido alto.
* Cambiar indexadores a Actualizar en el modo de programación: mueva los indexadores de Actualización al guardar al modo de actualización en el horario controlado por cron para evitar el bloqueo durante las actualizaciones frecuentes del catálogo, excepto para el indexador customer_grid.
* Considere la arquitectura escalada (dividida): si el ajuste y las correcciones de nivel de código siguen dejando CPU agotado al máximo en la carga, pase a una configuración de nivel dividido de seis nodos que escale los nodos web y de base de datos de forma independiente.

## Prácticas recomendadas y estabilidad

A continuación se ofrece una descripción general de las prácticas recomendadas para garantizar la estabilidad de las instancias. Para ver los pasos detallados para cada uno de ellos, consulte [Preparación para las fiestas de Adobe Commerce > Prácticas recomendadas y estabilidad](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md).

* Actualice a la última versión de Adobe Commerce: conserve una versión compatible para mantener las correcciones de seguridad y las mejoras de rendimiento que Adobe incluye en cada versión.
* Instale la última herramienta ECE-Tools y herramienta de parches de calidad (QPT): Actualice ece-tools con sus dependencias y confirme que se aplican las correcciones de la herramienta de parches de calidad aplicables, tanto para instalaciones en la nube como locales.
* Revisar y limpiar archivos de registro: elimine los registros de depuración y supervise los errores recurrentes para evitar el uso excesivo del disco y mejorar la visibilidad del registro.
* Supervisar el crecimiento del tamaño del disco: mantenga los volúmenes de bases de datos y archivos compartidos por debajo del 70% de uso para que el crecimiento del almacenamiento no se produzca en déclencheur de interrupción.
* Revise las consultas lentas de la base de datos: utilice las herramientas de APM y el registro de consultas lentas de MySQL para encontrar y corregir consultas costosas antes de que se agraven bajo el tráfico máximo.
* Configure los trabajos cron correctamente: Confirm cron se ejecuta cada minuto bajo el usuario correcto, ya que cada operación asincrónica en Commerce depende de ello.
* Optimizar la configuración del lado del cliente: active la minificación y el agrupamiento de CSS, JavaScript y HTML para acelerar los tiempos de carga de las tiendas.

## Monitorización y observabilidad

A continuación se indican las formas recomendadas de supervisar la instancia de Adobe Commerce durante la temporada alta. Para ver los pasos detallados para cada una de estas recomendaciones de supervisión y observabilidad, consulte [Preparación para las fiestas de Adobe Commerce > Supervisión y observabilidad](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md).

* Monitorizar el tráfico con New Relic: Utilice los registros de streaming de Fastly en New Relic para detectar anomalías de tráfico, IP abusivas, solicitudes maliciosas dirigidas a extremos como pago y tendencias de dispositivo/explorador.
* Personalizar alertas de New Relic: configure sus propias alertas basadas en NRQL para el tráfico inusual, las consultas de GraphQL lentas o las tasas de error en aumento, además de las alertas administradas de Adobe.
* Rastrear puntuación de Apdex: observe la puntuación de Apdex (objetivo ≥ 0,85) para mantener los tiempos de respuesta del back-end y el front-end en un rango que los usuarios consideren satisfactorio.
* Revisar perspectivas de soporte (Informe SWAT): Ejecute un informe SWAT antes y después de los eventos pico para identificar los riesgos y las áreas de mejora a nivel del sistema.

## Escalabilidad y planificación de capacidades

Para ver los pasos detallados para cada una de estas recomendaciones de escalabilidad y planificación de capacidad, consulte [Preparación para las fiestas de Adobe Commerce > Escalabilidad y planificación de la capacidad](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md).

* Planificar la actualización anticipada del clúster: Solicite una actualización temporal del equipo al servicio de asistencia de Adobe al menos 10 días hábiles antes de una promoción importante.
* Activar blindaje de origen de Fastly: enrute las solicitudes sin caché a través de un POP de Shield cerca del origen para que menos solicitudes lleguen directamente al servidor de origen.
* Realizar pruebas de carga y conmutación por error: probar los escenarios de carga y recuperación antes de las campañas principales para confirmar que los planes de escalado y reversión se mantienen.

## Preparación operativa

* Aplicar todos los parches de seguridad y rendimiento: finalice todos los parches antes de congelar el código para que las implementaciones no se interrumpan más adelante.
* Ejecute comprobaciones de estado antes de las vacaciones: pruebe las copias de seguridad, el estado de cron y los scripts de calentamiento de caché para que las operaciones se ejecuten sin problemas bajo carga.
* Establezca libros de reproducción de monitorización: Documente los umbrales de alerta, las rutas de escalación y los contactos ininterrumpidos para que el equipo pueda responder rápidamente durante el pico.
* Planes de reversión de documentos: mantenga preparadas las estrategias de reversión con versiones para que pueda recuperarse rápidamente de una implementación incorrecta.