---
title: Guía de preparación para las vacaciones unificadas de las soluciones Adobe DX
description: Este artículo proporciona una guía de preparación para las vacaciones para las soluciones DX.
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: b4b75c2c32f6265ce3fbac9f3bed888e08956982
workflow-type: tm+mt
source-wordcount: '3815'
ht-degree: 1%

---

# Guía de preparación para las vacaciones unificadas de las soluciones Adobe DX


La Guía de preparación unificada para las vacaciones de Adobe DX Solutions le ayuda a prepararse para la temporada de vacaciones, ya que se centra en la planificación proactiva en lugar de en la resolución reactiva de problemas. Proporciona pasos prácticos para garantizar que las instancias estén listas, minimizando los posibles problemas antes de que surjan. El equipo de Adobe ofrece experiencia técnica, una amplia gama de funciones y métodos probados para ofrecer el nivel adecuado de asistencia y orientación, tanto técnica como estratégica, de modo que su empresa esté bien preparada.

Siga estas prácticas recomendadas para garantizar que sus soluciones de Adobe Digital Experience sean resistentes, seguras y estén preparadas para el tráfico de las fiestas más importantes:

* Planifique el aumento del tráfico.
* Evite cambios importantes durante las horas de mayor actividad; programe actualizaciones antes o después de la temporada de vacaciones.
* Utilice paneles y alertas para monitorizar el rendimiento y detectar cuellos de botella de forma temprana.
* Asegúrese de que sus contactos de soporte autorizados estén actualizados.
* [Póngase en contacto con el soporte técnico de Adobe](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket) con antelación siempre que sea posible.

Para obtener recomendaciones de preparación para las fiestas específicas de la solución de Adobe, consulte las secciones siguientes.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Haga clic en cada sección para expandirla.


## Guía de preparación para las vacaciones de Adobe Experience Platform (AEP)

+++**Haga clic para ver las recomendaciones de preparación para las vacaciones de Adobe Experience Platform (AEP).**

Adobe Experience Platform (AEP) desempeña un papel fundamental para potenciar las experiencias de los clientes en tiempo real. A medida que se acerca la temporada de vacaciones, es esencial asegurarse de que la implementación de AEP esté optimizada para un mayor tráfico, un manejo de datos seguro y una ingesta escalable.

## Predecir la demanda estacional

Para prepararse para los picos de tráfico estacionales, Adobe recomienda planificar la capacidad y monitorizar la ingesta de perfiles de flujo continuo. Esto incluye prever los volúmenes de datos y garantizar que el sistema pueda gestionar un mayor rendimiento. Consulte [Plan de capacidad y tráfico estacional](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) como referencia.

## Preparar para la escala

Adobe proporciona varias estrategias para garantizar que su entorno esté listo para el tráfico de las fiestas:

* Aumente la capacidad asignada para las zonas protegidas.
* Identifique los flujos de datos de alto rendimiento en el [tablero de supervisión](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) y aplique restricciones o filtros donde sea necesario.
* Utilice la ingesta por lotes para casos de uso de baja latencia a fin de optimizar el rendimiento tal como se describe en [Uso de licencias y capacidades: Prácticas recomendadas de rendimiento de streaming](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions).

Estas prácticas ayudan a mantener la fiabilidad de la ingesta y a reducir la latencia durante los períodos de mayor actividad.

## Prácticas recomendadas y protecciones

Para mantenerse dentro de los límites operativos y evitar interrupciones en el servicio, Adobe recomienda las siguientes protecciones de ingesta y perfil:

* [Prácticas recomendadas de rendimiento de streaming](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)
* [Protecciones para la ingesta de datos](https://experienceleague.adobe.com/es/docs/experience-platform/ingestion/guardrails)
* [Protecciones predeterminadas para la segmentación y los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails)
* [Modelos de AEP: Protecciones](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails)

## Seguridad y gobernanza

Adobe hace hincapié en las sólidas prácticas de seguridad y gobernanza, especialmente durante las temporadas de alto tráfico en las que se aumenta la confidencialidad de los datos.

Consulte [Gobernanza, privacidad y seguridad en Adobe Experience Platform: Security](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/overview#security) para obtener recomendaciones sobre cómo proteger los datos de los clientes, aplicar controles de privacidad y mantener el cumplimiento en la implementación de AEP.

Siguiendo estas directrices y aprovechando la documentación pública de Adobe, las organizaciones pueden garantizar que su Adobe Experience Platform sea resistente, seguro y esté listo para ofrecer experiencias de cliente excepcionales durante la temporada de vacaciones.

+++

## Guía de preparación para las vacaciones de Adobe Journey Optimizer (AJO)

+++**Haga clic para ver las recomendaciones de preparación para las vacaciones de Adobe Journey Optimizer (AJO).**


Para preparar Adobe Journey Optimizer para la temporada de vacaciones, las organizaciones deben anticipar los picos de eventos y la complejidad en canales múltiples, configurar las reglas de recorrido y frecuencia, y garantizar la higiene de los datos y la lógica de toma de decisiones. También deben validar el rendimiento a escala, aplicar protecciones de seguridad y API y aplicar perspectivas posteriores al pico para refinar las campañas futuras.

## Predecir demanda

* En función de las compresiones de la temporada de vacaciones y el mayor volumen de campaña, espere lo siguiente:
   * Un pico en eventos en tiempo real y recorridos activados (abandono del carro de compras, ofertas de último minuto)
   * Riesgos de saturación de mensajes (mayores exclusiones, fatiga)
   * Mayor complejidad en canales múltiples (correo electrónico + push + SMS + en la aplicación)
* Utilice las métricas del año pasado (tasas de apertura/clic/exclusión, volúmenes de entrada de recorridos) para modelar las cargas esperadas y establecer umbrales para sus sistemas de mensajería.
* Identifique las probables &quot;ventanas silenciosas&quot; o los períodos de bajo rendimiento (por ejemplo: fines de semana, días festivos) y planifique los volúmenes de envío en consecuencia.

## Preparar para la escala

* Asegúrese de que todas las configuraciones de canal en AJO estén correctamente configuradas: correo electrónico, push, SMS, web, en la aplicación. Consulte [Configurar configuraciones de canal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces).
* Configure reglas de límite de frecuencia y límite para controlar los volúmenes de mensajes. Consulte el artículo [Límite de frecuencia](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules).
* Configuración de conjuntos de reglas de canal/recorrido: Consulte [Trabajar con conjuntos de reglas](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Prepare sus flujos de eventos en tiempo real, higiene de los datos y marcos de segmentación.
* Asegúrese de haber definido las audiencias de destino para las campañas de días festivos, como:
   * clientes de alto valor
   * segmentos fieles
   * abandonadores del carro
   * compradores nuevos
* Precargue o prepare plantillas para recorridos de vacaciones, aproveche la lógica de toma de decisiones (ofertas/restricciones) para que pueda adaptarse dinámicamente en función del inventario, las ofertas con distinción de tiempo y las preferencias de canal. Vea el ejemplo en el artículo [Agregar restricciones a una oferta](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints).
* Preparación técnica: Confirme la capacidad de carga de la API/punto final, las reglas de acelerador/límite para acciones personalizadas e integraciones externas. Consulte [Protecciones y limitaciones](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails).

## Prueba y validación

* Utilice el marco de experimentación para probar los cambios clave en las variables:
   * tiempo de envío
   * tipo de oferta
   * mezcla de canales
Consulte [Prácticas recomendadas de AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* Realice una validación de recorrido de extremo a extremo:
   * déclencheur de eventos
   * entrada de segmentación
   * Flujos de ruta de recorrido
   * lógica de personalización
   * restricciones de oferta
   * criterios de salida
* Compruebe las reglas de restricción y conflicto. Consulte el artículo [límite y arbitraje del Recorrido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping).
* Volúmenes escalados de prueba de esfuerzo para envíos o picos máximos: simule volúmenes de déclencheur altos para validar el comportamiento del sistema bajo carga.
* Validar la capacidad de entrega: caliente los dominios y remitentes de los correos electrónicos, confirme las configuraciones de push móviles y compruebe los canales de reserva para SMS/en la aplicación.

## Prácticas recomendadas

* Utilice la orquestación omnicanal. Consulte el artículo del blog [recorridos esenciales de los clientes omnicanal para la participación y el crecimiento](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) que muestra un ejemplo de temporada de vacaciones con AJO.
* Priorice los déclencheur en tiempo real donde corresponda. Por ejemplo: abandonos del carro de compras, abandonos de exploración y alertas de stock, ya que los compradores de vacaciones son más reactivos.
* Aproveche la segmentación y personalización: Segmente segmentos de alta intención, adapte ofertas basadas en el comportamiento de compras anteriores y preferencias.
* Fatiga mínima de la mensajería: aplique límites y horas de silencio para evitar solicitar en exceso. Consulte [Elevar la experiencia del cliente con límite de frecuencia diario en la publicación de blog de AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510).
* El tiempo importa: el plan envía mensajes antes en la ventana de días festivos (dada la temporada comprimida) y alinea los canales con los husos horarios y el comportamiento de la audiencia local.
* Ofrecer ofertas dinámicas/de tiempo limitado para crear urgencia, pero coordinarse entre canales para evitar duplicaciones y conflictos.
* Utilice la lógica de supresión: Suprima las audiencias que acaban de comprar o aplique recorridos posteriores a la compra para evitar mensajes redundantes.

## Seguridad y gobernanza

* Asegúrese de que el control de acceso y los permisos estén configurados de modo que solo los usuarios necesarios puedan implementar recorridos o modificar reglas empresariales.
* Supervise y aplique límites de llamada/conexión API: Por ejemplo, consulte la API [Límite | Artículo de Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping).
* Utilice datos de origen limpios y asegúrese de que la vinculación de identidad adecuada sea correcta, de modo que la mensajería esté centrada en el cliente y no esté duplicada o desalineada.
* Asegúrese de que los dominios de envío estén calientes y de que se apliquen medidas antispam, especialmente para envíos de vacaciones de gran volumen.
* Revise los registros de auditoría y los cambios de recorrido con frecuencia durante la temporada alta para detectar tempranamente ejecuciones incorrectas o recorridos erróneos.

## Aprendizajes después del pico

* Después de las cargas máximas, realice una revisión de los recuentos de entradas de recorridos, los recuentos de supresión, las tasas de exclusión, las métricas de capacidad de entrega y el rendimiento del canal.
* Limpie los segmentos suprimidos y ponga en pausa o retire los recorridos creados para la ventana de días festivos para evitar la fatiga de arrastre.
* Utilice datos del rendimiento en tiempo real para refinar la planificación del próximo año (por ejemplo: enviar ajustes de tiempo, mezcla de canales y volumen de mensajes).

Mediante la previsión proactiva de la demanda estacional, la configuración de canales y reglas, la validación del rendimiento del recorrido y la aplicación de la seguridad y la gobernanza, las organizaciones pueden garantizar que Adobe Journey Optimizer ofrezca experiencias de cliente sin problemas, personalizadas y resistentes durante esta temporada de vacaciones y más allá.

+++

## Guía de preparación para las vacaciones de Customer Journey Analytics (CJA)

+++**Haga clic para ver las recomendaciones de preparación para las vacaciones de Customer Journey Analytics (CJA).**

Customer Journey Analytics utiliza las 5 P para lograr la preparación para las vacaciones y la temporada alta.

### Preparar para la escala

* Revise las conexiones de CJA y las vistas de datos; determine qué conexiones y vistas de datos requieren una supervisión y un aprovisionamiento mejorados.
* Confirme que el aprovisionamiento es suficiente para la escala de días festivos; amplíe las conexiones críticas y las vistas de datos según sea necesario. Consulte [Administrar conexiones](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections) para obtener más información.

### Monitorización del rendimiento

* Aproveche la RAM ([[!UICONTROL Administrador de actividades de creación de informes] información general](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para supervisar las solicitudes de creación de informes activas y en cola en tiempo real, identificar conexiones de capacidad insuficiente y detectar cuellos de botella.
* Observe el aumento de latencia durante la carga máxima con los artículos [Errores y solución de problemas](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) y [Limitaciones conocidas](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations).
* Permita a los administradores suspender o cancelar de forma preventiva las solicitudes bloqueadas o de larga ejecución a través de la RAM. Consulte el artículo [Cancelar solicitudes de informes en CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Prácticas recomendadas

* Programe exportaciones e informes durante períodos de poco tráfico para suavizar la carga y minimizar la latencia. Consulte el artículo [Informes programados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager).
* Distribuir solicitudes: Programe informes a diferentes intervalos a lo largo del día.
* Reduzca los paneles, simplifique los segmentos, acorte los intervalos de fechas y evite el exceso de trabajos simultáneos. Consulte el artículo [Optimización del rendimiento de CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) para obtener más información.

### Resolución de problemas

* Cuando solucione errores del espacio de trabajo, consulte los mensajes de error para conocer la causa y las acciones recomendadas; use RAM ([!UICONTROL Administrador de actividades de creación de informes]) para borrar cuellos de botella y administrar la concurrencia de forma eficaz. Consulte [Control de errores de CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) para obtener más información.
* Use la memoria RAM ([[!UICONTROL Administrador de actividades de creación de informes] en CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para identificar usuarios, consultas o proyectos problemáticos; dé prioridad y finalice o cancele según sea necesario.

### Aprendizajes después del pico

* Después del período festivo/de mayor actividad, revise los registros de rendimiento e incidencias para evaluar el impacto de las prácticas recomendadas proporcionadas.
* Revise las consultas lentas y las tareas del usuario para identificar patrones/tendencias que se puedan optimizar para la próxima temporada.
* Recopile comentarios de usuarios e interesados: actualice sus propios Runbooks y planes de preparación con las perspectivas recién obtenidas.
* Proporcione comentarios a los equipos de Adobe a través de su equipo de cuenta.

+++

## Guía de preparación para las fiestas de Adobe Commerce

+++**Haga clic para ver las recomendaciones de preparación para las fiestas de Adobe Commerce.**

Para garantizar el éxito de la temporada alta de su organización, es esencial preparar su tienda digital de Adobe Commerce para el alto tráfico.

## Predecir demanda

* Durante el período de ventas máximas de los festivos (de mediados de noviembre a mediados de enero), Adobe recomienda que todos los comerciantes de Adobe Commerce alojados en nuestra infraestructura en la nube planifiquen de forma proactiva un aumento de visitantes enviando solicitudes de capacidad de aumento de festivos. Consulte las [Solicitudes de capacidad de Holiday Surge para Adobe Commerce en nuestra infraestructura en la nube](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud) para obtener detalles.

## Preparar para la escala

Siga las recomendaciones de la guía [Planificación y pivotación: un enfoque estratégico para la temporada alta de 2025](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025), que proporciona estrategias procesables mediante Adobe Commerce (y herramientas opcionales de Adobe Experience Cloud) para ayudarle a planificar, pivotar y ofrecer experiencias de cliente excepcionales en las épocas de mayor actividad del año.

## Prácticas recomendadas

* Siga la guía de Adobe [Cómo preparar su infraestructura para el alto tráfico: las 5 P del rendimiento de la temporada alta](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Consulte [Sugerencias técnicas para la preparación para las vacaciones de Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) para obtener sugerencias sobre cómo preparar su infraestructura para el alto tráfico, evitar el tiempo de inactividad y optimizar el rendimiento en el período de vacaciones.

+++

## Guía de preparación de Adobe Experience Manager (AEM) Cloud Services

+++**Haga clic para ver las recomendaciones de preparación de Adobe Experience Manager (AEM) Cloud Services.**

La temporada de vacaciones se está acercando rápidamente y, para muchos clientes de Adobe, esto significa el inicio de los períodos de mayor volumen de ventas. En nuestro compromiso con su éxito, queremos asegurarnos de que esté completamente preparado para el próximo aumento del tráfico.

## Servicios en la nube de Adobe Experience Manager (AEM)

Si su organización experimenta los momentos más ajetreados durante la temporada de vacaciones, puede que esté pensando en cómo optimizar su sitio de Adobe Experience Manager para dar cabida al tráfico máximo. Afortunadamente, con Adobe Experience Manager Cloud Services, su sitio ya está equipado con la capacidad de escalado automático, lo que garantiza una experiencia perfecta para los visitantes, independientemente de si hay cambios repentinos en el tráfico.

## Preparar para la escala

* Para obtener información detallada y orientación sobre la preparación para un alto tráfico con Adobe Experience Manager Cloud Services, consulte los siguientes vínculos:

   * [CDN en AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [Almacenamiento en caché de AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview)

* Si es cliente de Ultimate Success y ha compartido recientemente información de previsión de volumen con su equipo de cuenta de Adobe, no se preocupe por enviárnosla de nuevo, ya que ya tenemos una vista.

Estamos aquí para apoyarle en cada paso de su recorrido. Si tiene preguntas o inquietudes, no dude en [enviar un ticket de asistencia](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Para prepararse para una campaña de marketing en temporada de vacaciones, consulte la [Guía del usuario de AEMaaCS: Introducción: Parámetros de campaña de marketing](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters).

## Seguridad y gobernanza

Para obtener información sobre la protección y la seguridad del tráfico en el sitio web de AEM, consulte el artículo [Información general: Protección de sitios web de AEM](https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) en los Tutoriales de AEM as a Cloud Service.

## Planificación de mantenimiento de vacaciones

Adobe tiene períodos de exclusión de mantenimiento programados para garantizar un servicio ininterrumpido durante los períodos vacacionales críticos:

* **No se producirán actualizaciones automáticas** entre:
   * 24 de noviembre de 2025 - 2 de diciembre de 2025
   * 15 de diciembre de 2025: 2 de enero de 2026

Esto garantiza la estabilidad durante los períodos de alto tráfico. Para ver las programaciones de versiones completas y las ventanas de mantenimiento, consulte la [hoja de ruta de versiones de AEM](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).


## Adobe Experience Manager (AEM) con Adobe Managed Services (AMS)

Los clientes de AEM que aprovechan Adobe Managed Services pueden trabajar de forma proactiva con sus CSE para planificar las necesidades de cobertura de los días festivos.

++++

## Guía de preparación para las vacaciones de Adobe Marketo

+++**Haga clic para ver las recomendaciones de preparación para las vacaciones de Adobe Marketo.**

Para garantizar el éxito de las campañas de días festivos con Adobe Marketo, los equipos deben verificar la configuración de autenticación de correo electrónico, limpiar y asegurar su base de datos, optimizar la lógica y la programación de las campañas, probar a fondo el procesamiento y la capacidad de entrega de los correos electrónicos y optimizar la preparación para la asistencia para lograr el máximo rendimiento y participación.

## Preparar para la escala

* Compruebe la configuración de SPF/DKIM y asegúrese de que todo sigue configurado y funciona correctamente. Consulte el artículo [Configurar SPF y DKIM para la capacidad de envío de correo electrónico](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) para obtener más información.
* Audite y limpie la base de datos de Marketo purgando registros inactivos/no válidos. Esto aumentará las posibilidades de que sus envíos lleguen a las bandejas de entrada de los posibles clientes más preparados para ventas. Consulte el artículo [Comprobación del estado de la base de datos de Marketo y cómo mantenerla limpia](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563) para obtener más información.
* Confirme que los integrantes del equipo tienen los permisos adecuados para realizar tareas y evitar el acceso no deseado o los cambios en los correos electrónicos. Ya sea que estés haciendo cambios a través de **[!UICONTROL Admin]** o a través de **[!UICONTROL Admin Console]**, te tenemos cubierto. Consulte el artículo [Administrar roles de usuario y permisos](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions).
* Revise las integraciones de Launchpad para garantizar la autenticación correcta y resolver cualquier posible error antes de utilizarlas. Consulte el artículo [Guía para desarrolladores de Marketo: Authentication](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication).

## Prácticas recomendadas

La eficiencia comienza con comprender exactamente cómo Marketo prioriza y procesa las campañas. Dele a sus campañas el don de la velocidad con estos consejos de optimización.

* Comprender cómo Marketo prioriza el procesamiento de los pasos del flujo de campaña es crucial para evitar retrasar involuntariamente cualquier correo electrónico urgente o de alta prioridad. Consulte el artículo [Funcionamiento del procesamiento de Campaign](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Tener en cuenta la lógica de las listas inteligentes ayuda a garantizar que las campañas se ejecuten de forma rápida y con el máximo rendimiento. Consulte el artículo [Prácticas recomendadas para listas inteligentes](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists).
* **[!UICONTROL Head Start]** o **[!UICONTROL Zona horaria del destinatario]** pueden empezar a crear correos electrónicos antes del envío, reducir los retrasos y proporcionar tiempo de preparación adicional para calificar a los posibles clientes con lógica de recursos altos. Consulte los artículos [Head Start para programas de correo electrónico](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) y [Programar programas de correo electrónico con zona horaria de destinatario](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone) para obtener más información.
* La campaña está activa, los posibles clientes siguen su curso y se da cuenta de un error en el paso de flujo. Es tentador solucionarlo con un ajuste rápido, pero tener en cuenta lo que sucede cuando cambia un paso de espera activo o reordena los flujos puede ayudarle a evitar muchos dolores de cabeza y realizar una limpieza más tarde. Consulte el artículo [Edición del flujo de campaña con miembros en pasos de espera](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

## Prueba y validación

Antes de pulsar **[!UICONTROL Enviar]**, asegúrate de que tus correos electrónicos tengan el aspecto y el rendimiento que esperabas.

* Marketo ofrece varias formas de probar el aspecto de un correo electrónico para asegurarse de que tiene exactamente el aspecto que usted imaginaba.
   * Utilice la función **[!UICONTROL Preview]** para asegurarse de que el contenido dinámico y los tokens se representen correctamente mediante la vista previa mediante la segmentación o posibles clientes individuales. Consulte el artículo [Vista previa de un correo electrónico con contenido dinámico](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Envíe un correo electrónico directo a los registros de prueba de forma rápida y sencilla para ver cómo aparece el correo electrónico en diferentes clientes o dispositivos. Consulte el artículo [Ejecutar un solo paso de flujo desde una lista inteligente](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * Para los usuarios de [!DNL Litmus], ahora es más fácil que nunca integrar su cuenta e iniciar pruebas de procesamiento directamente desde el editor de correo electrónico. Consulte el artículo [Probar el procesamiento de correo electrónico con [!DNL Litmus]](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Consulte la función Informe de correo no deseado, que se integra con [!DNL SpamAssassin] para revisar el contenido del correo electrónico y asignar una puntuación sobre la probabilidad de que llegue a la bandeja de entrada o de que se marque como *correo no deseado*. Consulte el artículo [Informe de correo no deseado](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report).
* Vigile [!UICONTROL Cola de campaña] para verificar que sus campañas estén procesando y priorizando correctamente los elementos de alta urgencia. Ver [&#x200B; ¿Se está ejecutando mi campaña?](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662) artículo.

## Optimice su experiencia de asistencia

Cuando algo sale mal, la velocidad importa, y el Soporte de Marketo está aquí para ayudarle. Incluya estos detalles en su caso de asistencia para evitar idas y vueltas y ayudar a nuestro equipo a trabajar para lograr una resolución más rápida. Consulte el artículo [Prácticas recomendadas para trabajar con soporte de Marketo](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Con esta guía, puede descansar un poco más tranquilo sabiendo que está empezando desde una posición sólida para impulsar la participación y las conversiones durante esta ventana crítica. Hay mucho en juego, pero tu estrés no tiene por qué serlo. Empiece sus preparativos hoy y haga de esta temporada de vacaciones su más exitosa todavía.

+++

## Guía de preparación para las fiestas de Adobe Workfront

+++**Haga clic para ver las recomendaciones de preparación para las fiestas de Adobe Workfront.**

Para preparar Adobe Workfront para la temporada de vacaciones, los equipos deben actualizar los contactos de asistencia, alinear los horarios internos con Adobe, evitar cambios importantes durante las ventanas de mayor actividad y supervisar de forma proactiva las automatizaciones y las integraciones para garantizar un funcionamiento sin problemas.

## Preparar para la escala

Para garantizar una experiencia de asistencia sin problemas durante las vacaciones:

* Revise y actualice sus contactos de asistencia autorizados con antelación.
* Compruebe que las partes interesadas clave estén disponibles para colaborar con el servicio de asistencia si surgen problemas críticos.
* Si planea cambios de producto o flujo de trabajo durante la ventana de días festivos, considere programarlos antes de mediados de noviembre o después de principios de enero para obtener los mejores tiempos de respuesta.
* Comunique los horarios de vacaciones internos a sus contactos de Adobe para garantizar la alineación.

## Prueba y validación

Manténgase informado sobre las versiones de Workfront y pruebe las nuevas funciones en entornos de zonas protegidas:

* [Prepararse para una versión de Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Archivo de notas de la versión de Workfront](https://experienceleague.adobe.com/es/docs/workfront/using/product-announcements/product-releases/product-releases)
* [Información general sobre la versión del primer trimestre de 2025](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Grabación del seminario web sobre la versión de Workfront](https://experienceleague.adobe.com/en/docs/events/workfront-recordings/releases/25-1-release-webinar)

## Prácticas recomendadas

* Planificación proactiva: identifique las dependencias del sistema o automatizaciones programadas que puedan verse afectadas por las programaciones de tiempo de espera internas.
* Comunicación continua: Mantenga a sus equipos internos y al Soporte de Adobe informados sobre el mantenimiento planificado o los eventos clave.
* Use Paneles: Monitorice las integraciones y automatizaciones clave para captar los primeros signos de problemas de rendimiento.
* Escalar antes: si prevé u observa la degradación del servicio, abra un ticket de asistencia inmediatamente, no espere a que se vuelva crítico.

Si planifican con anticipación, mantienen una comunicación clara y escalan los problemas con antelación, las organizaciones pueden minimizar las interrupciones y garantizar que Workfront siga admitiendo flujos de trabajo críticos durante todo el periodo festivo.

+++

## Guía de preparación para las fiestas de Adobe Campaign

+++**Haga clic para ver las recomendaciones de preparación para las fiestas de Adobe Campaign.**


Para preparar Adobe Campaign para la preparación para las fiestas, los equipos deben validar de forma proactiva la configuración de capacidad de entrega, optimizar la segmentación de audiencia y la frecuencia de los mensajes, garantizar la escalabilidad de la infraestructura y probar la orquestación de campañas en canales múltiples para gestionar de forma eficaz los picos de volumen y participación estacionales.

## Sugerencias de los expertos para que sus campañas de días festivos se destaquen

Al igual que nunca es demasiado pronto para comenzar sus compras de días festivos, tampoco lo es para empezar a planificar una campaña de marketing de días festivos con gran éxito. Con Adobe Campaign, puede diseñar, planificar y ejecutar campañas que hagan realidad todos los deseos de los días festivos de su organización. Pero, ¿conoce todos los consejos para realizar campañas que terminen el año con éxito? Consulte este vídeo, [Sugerencias de los expertos para que sus campañas de días festivos se destaquen](https://experienceleague.adobe.com/en/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03), en el que se tratan las prácticas recomendadas de envío y ejecución, y se muestra cómo hacerlo todo en Adobe Campaign.

## Consideraciones y preparativos para el período de vacaciones

Este vídeo, [Adobe Campaign: Preparación para las vacaciones - Consideraciones y preparativos para el período festivo](https://helpx.adobe.com/customer-care-office-hours/campaign/campaign-holiday-readiness.html), trata sobre:

* Participación de la comunidad de Campaign
* Entrega - Consideraciones para las vacaciones y más allá!
* Recomendaciones técnicas para Adobe Campaign Classic (ACC) y Adobe Campaign Standard (ACS)

Para que Adobe Campaign esté listo para la temporada alta de vacaciones, las organizaciones deben finalizar las comprobaciones de capacidad de entrega, validar las configuraciones de campaña y garantizar que la infraestructura escalable y la orquestación multicanal estén implementadas para ejecutar con seguridad campañas de alto volumen que requieran mucho tiempo durante la temporada de vacaciones.

+++

## Guía de preparación para las fiestas de Adobe Analytics

+++**Haga clic para ver las recomendaciones de preparación para las fiestas de Adobe Analytics.**

A medida que se acerca la temporada de vacaciones, las organizaciones que utilizan Adobe Analytics deben tomar medidas proactivas para garantizar la precisión de los datos, el rendimiento de la plataforma y la fiabilidad de los informes durante los períodos de tráfico máximo. Adobe proporciona varios recursos y prácticas recomendadas para ayudar a los equipos a prepararse de forma eficaz.

## Predecir tráfico

Para garantizar la asignación de hardware y la capacidad de respuesta del sistema adecuadas, Adobe recomienda enviar **volúmenes máximos de visitas/llamadas al servidor** por hora y por día con antelación.

* Compruebe la programación de [picos de tráfico y los plazos de asignación de hardware](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times), ya que comprender la rapidez con la que los datos están disponibles es fundamental para la toma de decisiones en tiempo real durante períodos de gran volumen.

* Conozca qué afecta a la disponibilidad y latencia de los datos en Adobe Analytics en [Información general sobre la latencia de datos en Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency), incluidos los picos de tráfico inesperados y los problemas de hardware, y descubra las estrategias recomendadas para reducir los retrasos de los datos.

## Prácticas recomendadas

Para los equipos que utilizan fuentes de datos para exportar datos de análisis sin procesar, Adobe proporciona instrucciones para optimizar las configuraciones de fuentes y evitar escollos comunes.

* [Prácticas recomendadas para fuentes de datos de Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

Para mantener una creación de informes rápida y fiable durante los festivos, Adobe recomienda:

* [Optimizando el rendimiento de Analysis Workspace](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Solución de problemas y prácticas recomendadas para Report Builder: Recommendations para optimizar solicitudes](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Guía de componentes de Analytics: cola de informes programados](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin)

## Planificación de mantenimiento de vacaciones

Adobe normalmente aplica **ventanas de exclusión de mantenimiento** durante los períodos de vacaciones de mayor actividad para garantizar un servicio ininterrumpido. Los clientes deben monitorizar los programas de versiones y mantenimiento de Adobe a través de Experience League y coordinarse con sus equipos de cuenta de Adobe para la planificación de la asistencia.

Siguiendo estas directrices y aprovechando la documentación pública de Adobe, las organizaciones pueden asegurarse de que su implementación de Adobe Analytics sea sólida, adaptable y esté lista para las demandas de la temporada de vacaciones.

+++

## Guía de preparación para las fiestas de Adobe Target

+++**Haga clic para ver las recomendaciones de preparación para las fiestas de Adobe Target.**

La temporada de vacaciones ofrece interesantes oportunidades de participación, pero también conlleva desafíos como aumentos en el tráfico y una mayor demanda de sistemas de personalización. Para ayudarle a ofrecer experiencias sin problemas durante este periodo crítico, hemos recopilado recomendaciones clave para garantizar que la implementación de Adobe Target esté lista.

## Predecir demanda

Comience por anticipar picos de tráfico de entre el 20 y el 50 % o más y validar que su infraestructura pueda gestionar la carga. Prevea la actividad y los volúmenes de datos en Adobe Target, Analytics y AEP para evitar sorpresas.

También es importante identificar recorridos esenciales, como el cierre de compra, las recomendaciones de productos y las ofertas promocionales, para que los esfuerzos de personalización se centren en dónde más importan.

Consulte [Prácticas recomendadas para la optimización con Adobe Target](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

## Preparar para la escala

* Planifique el aumento del tráfico en el sitio web y los dispositivos móviles e informe al equipo de asistencia de Target para aumentar la capacidad del servidor y evitar llamadas bloqueadas.
* Para cualquier prueba de carga/apertura, se debe informar al equipo de asistencia de Target con antelación.
* Actualice a las últimas `at.js`/versiones de la API de envío.
* Inmovilizar cambios no críticos; prepararse para experiencias de reserva.
* Alinee los procesos de soporte y escalación y habilite alertas proactivas.

## Prueba y validación

Valide la entrega de contenido con [vínculos de control de calidad](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa) para confirmar que todo funciona según lo esperado. Use **[!UICONTROL Coincidir reglas de audiencia para ver las experiencias]** para asegurarse de que la audiencia correcta cumpla los requisitos de la actividad que está probando. Compruebe que su configuración de **[!UICONTROL Métrica de objetivos]** esté alineada con el **[!UICONTROL Objetivo]** de la actividad. Y siempre tener un plan de respaldo listo, por si acaso.

## Prácticas recomendadas

Mantenga su implementación dentro de los [límites de Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits) y compruebe el [cumplimiento del RGPD y la CCPA](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) con antelación antes de iniciar. Mantenga menos de 100 actividades activas y archive las más antiguas para optimizar las cosas. Aproveche **[!UICONTROL Asignación automática]**/**[!UICONTROL Segmentación automática]** para la optimización impulsada por IA. Establezca planes de reversión y paneles de monitorización en tiempo real.

## Seguridad y gobernanza

Antes de personalizar las experiencias, confirme el cumplimiento del consentimiento según el RGPD y la CCPA. Evite almacenar información de identificación personal (PII) en parámetros de perfil y valide la seguridad de la API para proteger los datos de los clientes.

+++
