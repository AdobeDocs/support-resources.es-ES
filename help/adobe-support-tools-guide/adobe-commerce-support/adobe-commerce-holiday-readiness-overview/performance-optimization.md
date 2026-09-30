---
title: Optimización del rendimiento
description: Recomendaciones de optimización de rendimiento para ayudar a los comerciantes de Adobe Commerce a preparar sus entornos para eventos de alto tráfico como la temporada de vacaciones.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
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
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# Optimización del rendimiento

En esta sección se proporcionan recomendaciones técnicas para la preparación de entornos de Adobe Commerce, tanto de Commerce en infraestructura en la nube como locales, para eventos de alto tráfico como la temporada de vacaciones.

>[!NOTE]
>
>Los pasos marcados **(solo en la nube)** se aplican a Commerce en la infraestructura en la nube. La mayoría de las demás recomendaciones también se aplican a las implementaciones locales.

## Optimizar el almacenamiento en caché de solicitudes de Fastly (solo en la nube) {#optimize-fastly-request-caching}

[!DNL Fastly] almacena en caché las respuestas en el perímetro para reducir la carga en el servidor de origen. Durante la temporada alta, algunas comprobaciones de configuración le ayudan a sacar el máximo partido a esa caché, especialmente cuando ejecuta promociones con parámetros de seguimiento o una tienda sin encabezado. Para obtener la referencia de configuración completa, consulte [Personalizar la configuración de la caché](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration).

* Normalice los parámetros de seguimiento: durante la temporada de vacaciones, es probable que ejecute campañas sociales y de pago, como Google Ads, Facebook y X, que adjuntan cadenas de seguimiento únicas a cada dirección URL. Cada cadena única crea una entrada de caché independiente para lo que, de lo contrario, es la misma página, lo que reduce la proporción de visitas de caché. Agregue estos parámetros a la lista **[!UICONTROL Parámetros de URL ignorados]** en la configuración de [!DNL Fastly] en el administrador de Adobe Commerce para que [!DNL Fastly] los trate como equivalentes.
* Confirme que las páginas de aterrizaje se puedan almacenar en caché: Compruebe el encabezado de respuesta `x-cache` en cada página de aterrizaje de promoción. Una página que se puede almacenar en caché devuelve `HIT` o un par `HIT`/`MISS` en cargas posteriores. Si el encabezado devuelve `MISS, MISS`, la página no se está almacenando en caché y requiere investigación.
* Utilice solicitudes GET para consultas de GraphQL: Si ejecuta una tienda PWA o sin encabezado, envíe consultas GraphQL como `GET` solicitudes con la consulta incluida en la dirección URL, en lugar de como `POST` solicitudes. [!DNL Fastly] almacena en caché solo `GET` solicitudes donde la consulta es parte de la dirección URL. Una solicitud `GET` con la consulta enviada en el cuerpo no se almacena en caché.

>[!NOTE]
>
>El blindaje de origen [!DNL Fastly] también afecta al rendimiento de la caché. Para obtener detalles de configuración, consulte [Protección de origen de Fastly](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

## Habilitar Fastly IO (solo en la nube) {#enable-fastly-io}

[!DNL Fastly] IO descarga el cambio de tamaño de la imagen y la conversión de formato a la red perimetral [!DNL Fastly] en lugar del origen de Adobe Commerce. Esto reduce la carga del servidor y mejora la velocidad de procesamiento de páginas en tiendas con mucha imagen, un cuello de botella común durante los períodos de alto tráfico. Para ver las opciones de configuración, consulte [Optimización rápida de imágenes](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization).

Antes de empezar, confirme que el blindaje de origen está configurado. [!DNL Fastly] IO requiere blindaje de origen como requisito previo. Para obtener detalles de configuración, consulte [Protección de origen de Fastly](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

Para habilitar [!DNL Fastly] E/S:

1. En el Administrador, vaya a la página **[!UICONTROL Configuración rápida]** y seleccione **[!UICONTROL Configurar]** junto a **[!UICONTROL Opciones de configuración de E/S predeterminadas]**.
1. Confirme que el fragmento de E/S [!DNL Fastly] esté habilitado.
1. En la configuración de **[!UICONTROL Optimización de imagen]**, establezca **[!UICONTROL Habilitar optimización de imagen profunda]** en *[!UICONTROL Sí]*. Esta configuración deshabilita el cambio de tamaño de la imagen integrada de Adobe Commerce y transfiere la tarea a [!DNL Fastly].
1. Confirme que la posición de la pantalla está ajustada correctamente. Para obtener detalles de configuración, consulte [Protección de origen de Fastly](#fastly-origin-shielding).

>[!NOTE]
>
>La optimización de imágenes profundas cambia el tamaño de las imágenes del producto únicamente. Las imágenes de CMS, como los titulares y los bloques de contenido, no se ven afectadas y siguen utilizando el cambio de tamaño integrado de Adobe Commerce.

Para comprobar que [!DNL Fastly] IO funciona, compruebe los encabezados de respuesta en una solicitud de imagen de producto:

* El encabezado `x-cache` devuelve `HIT`.
* Los encabezados `fastly-io-info` y `fastly-stats` están rellenados.
* La dirección URL de la imagen no incluye un directorio `/cache/` en la ruta.

## Implementar la caché de Redis L2 {#implement-redis-l2-cache}

Implemente prácticas de almacenamiento en caché eficaces para que su tienda funcione de forma fiable durante las temporadas de tráfico máximo. [!DNL Redis] La caché L2 reduce el ancho de banda de red a [!DNL Redis] al almacenar los datos de la caché localmente en cada nodo web. Para obtener información general sobre cómo funciona la caché L2, consulte [Caché de nivel dos](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/level-two-cache).

En Commerce en la infraestructura de la nube, habilite esto configurando la variable de implementación `REDIS_BACKEND`. Para ver los pasos de configuración, consulte [REDIS_BACKEND](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend) en la Guía de Commerce sobre infraestructura en la nube. De forma local, configúrelo directamente en `app/etc/env.php`.

>[!NOTE]
>
>[!DNL Redis] no se admite como servidor de caché L2 en Adobe Commerce 2.4.9 o posterior, ni en versiones de parches posteriores a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 o 2.4.8-p4. En estas versiones, use `VALKEY_BACKEND` en su lugar.

## Habilitar conexiones esclavas MySQL y Redis (solo en la nube) {#enable-mysql-and-redis-slave-connections}

Las conexiones esclavas [!DNL Redis] y [!DNL MySQL] descargan el tráfico de lectura a los nodos de réplica, lo que reduce la carga en la conexión maestra durante los períodos de alto tráfico. Para ver los pasos de configuración, consulta [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) y [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) o [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection), según tu versión de Adobe Commerce.

### Conexiones esclavas de Redis

Una conexión esclava de [!DNL Redis] es una conexión de solo lectura a una instancia de [!DNL Redis], lo que permite que el tráfico de lectura se proporcione desde un nodo que no es maestro. Si no se habilita, [!DNL MySQL] puede sufrir un cuello de botella de carga alta. Compruebe el gráfico de información general de APM de [!DNL New Relic] para ver los tiempos de respuesta crecientes como una señal temprana y, a continuación, confirme en la pestaña **[!UICONTROL Base de datos]** ordenando por la transacción que más tiempo consume para identificar consultas [!DNL MySQL] `SELECT` lentas. Habilite esto estableciendo la variable de implementación `REDIS_USE_SLAVE_CONNECTION` en `true`.

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION` solo es compatible con los entornos de clúster de Staging y Production Pro. No es compatible con proyectos de arquitectura Starter o Scaled (split). Si se habilita en una arquitectura escalada, se producen [!DNL Redis] errores de conexión: use la caché de L2 [!DNL Redis] en lugar de esa arquitectura. Consulte [Implementar la caché de L2 de Redis](#implement-redis-l2-cache-implement-redis-l2-cache) más arriba.

### Conexiones esclavas de MySQL

Habilite el indicador `MYSQL_USE_SLAVE_CONNECTION` en los entornos de clúster de Pro para dirigir consultas de base de datos específicas de solo lectura a una conexión esclava y descargar la ejecución de consultas de la conexión maestra.

>[!CAUTION]
>
>Realice una prueba de carga antes de habilitar cualquiera de las opciones en producción. En entornos con carga normal, las conexiones esclavas pueden ralentizar el rendimiento en un 10 a 15 por ciento. En entornos con una carga pesada y sostenida, pueden mejorar el rendimiento por un margen similar. Evalúe el tráfico en temporada alta antes de habilitar la.

## Habilitar procesamiento asincrónico de pedidos y correo electrónico {#enable-asynchronous-order-and-email-processing}

Utilice el procesamiento asincrónico para poner en cola y ejecutar operaciones relacionadas con pedidos de gran volumen en segundo plano, lo que reduce la latencia de front-end durante el tráfico máximo. Esto cubre tres configuraciones relacionadas pero distintas—vea [Prácticas recomendadas de configuración](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration) para obtener una descripción general.

* Colocación de pedidos asincrónicos: el módulo Pedidos asincrónicos marca un pedido como recibido, lo coloca en cola y procesa los pedidos que entran por primera vez. Está desactivada de forma predeterminada. Habilítelo desde la línea de comandos:

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  Una vez activado, los detalles del pedido no están disponibles inmediatamente: el pedido permanece en cola hasta que el consumidor de `placeOrderProcess` lo verifica con el inventario (activado de forma predeterminada) y lo actualiza. Antes de deshabilitar este módulo, compruebe que todos los pedidos asincrónicos en vuelo han finalizado el procesamiento. Para obtener más información, consulte [Prácticas recomendadas de rendimiento de cierre de compra](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/high-throughput-order-processing).

* Procesamiento asincrónico de datos de pedidos: Las ventas intensivas de tiendas y el procesamiento intensivo de pedidos pueden entrar en conflicto en el nivel de base de datos. Al habilitar esta configuración se distinguen los dos patrones de tráfico, por lo que los pedidos se colocan en almacenamiento temporal y se mueven de forma masiva a la cuadrícula de Order Management sin colisiones. Esto programa las actualizaciones, por cron, de las cuadrículas Pedidos, Facturas, Envíos y Notas de Abono, evitando bloqueos y reduciendo el tiempo de procesamiento. Para obtener los mejores resultados, configure cron para que se ejecute una vez cada minuto.

  >[!NOTE]
  > 
  >La forma de habilitarlo depende del modo de implementación. Los entornos de ensayo y producción de Adobe Commerce en la infraestructura en la nube se ejecutan en el modo de producción de forma predeterminada, donde esta configuración no está disponible a través del administrador. En el modo de producción, ejecute `bin/magento config:set dev/grid/async_indexing 1` en su lugar. En el modo predeterminado, vaya a **[!UICONTROL Tiendas]** > **[!UICONTROL Configuración]** > **[!UICONTROL Avanzado]** > **[!UICONTROL Desarrollador]** > **[!UICONTROL Configuración de cuadrícula]** y establezca **[!UICONTROL Indexación asincrónica]** en *[!UICONTROL Habilitar]*.

  Para obtener más información, consulte [Operaciones de pedido programadas](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations).

* Notificaciones de correo electrónico asíncronas: esta configuración mueve las notificaciones de correo electrónico de cierre de compra y procesamiento de pedidos al segundo plano. Habilitarlo en **[!UICONTROL Tiendas]** > **[!UICONTROL Configuración]** > **[!UICONTROL Ventas]** > **[!UICONTROL Correos electrónicos de ventas]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Envío asincrónico]**.

## Configuración de indexadores para actualizar según lo programado {#configure-indexers-for-update-on-schedule}

Configure los indexadores para que se ejecuten en modo programado para evitar el bloqueo de la base de datos y mejorar la capacidad de respuesta durante las frecuentes actualizaciones de catálogo. Para obtener más información, consulte [Prácticas recomendadas para la configuración del indizador](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration).

Un indizador se puede ejecutar en modo **[!UICONTROL Actualizar al guardar]** o **[!UICONTROL Actualizar al programar]**.

* **[!UICONTROL Actualizar al guardar]** índices inmediatamente cada vez que cambie el catálogo u otros datos. Supone una baja intensidad de actualización y exploración, y puede causar retrasos significativos y la no disponibilidad de datos bajo una carga alta.
* Se recomienda **[!UICONTROL actualizar el horario]** para la producción. Almacena información sobre actualizaciones de datos y reíndices en segundo plano a través de un trabajo cron dedicado.

Establezca el modo de actualización de cada indizador de forma independiente en **[!UICONTROL Sistema]** > **[!UICONTROL Herramientas]** > **[!UICONTROL Administración de índices]**.

>[!IMPORTANT]
>
>Los modos compatibles con el indizador `customer_grid` dependen de la versión de Adobe Commerce. En las versiones anteriores a la 2.4.8, la cuadrícula del cliente solo admite **[!UICONTROL Actualizar al guardar]**; no la establezca en **[!UICONTROL Actualizar según lo programado]**. En Adobe Commerce 2.4.8 y versiones posteriores, Customer Grid admite ambos modos y ahora establece de forma predeterminada **[!UICONTROL Actualizar según lo programado]**.

## Desactivar y evaluar la tabla plana del catálogo {#disable-and-evaluate-catalog-flat-table}

No se recomienda el uso de mesas planas para productos y categorías. Esta función en desuso puede causar problemas de degradación del rendimiento y de indexación. Para obtener más información, consulte [Catálogos planos](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/catalog-flat).

Para deshabilitar el catálogo plano, ve a **[!UICONTROL Tiendas]** > **[!UICONTROL Configuración]** > **[!UICONTROL Catálogo]** > **[!UICONTROL Catálogo]** > **[!UICONTROL Tienda]**, establece **[!UICONTROL Usar catálogo plano]** en *[!UICONTROL No]*, establece **[!UICONTROL Usar catálogo plano]** en *[!UICONTROL No]* y, a continuación, haz clic en **[!UICONTROL Guardar configuración]**.

Algunos módulos y personalizaciones de terceros no requieren tablas planas para funcionar correctamente. Evalúe el impacto y el riesgo de seguir utilizando esas extensiones antes de deshabilitar las tablas planas.

## Considere la arquitectura escalada (dividida) (solo en la nube) {#consider-scaled-split-architecture}

Si, después de aplicar la configuración anterior y las optimizaciones de nivel de código, las pruebas de carga o el rendimiento de la infraestructura activa siguen mostrando CPU y otros recursos con el máximo, considere la posibilidad de pasar a una arquitectura escalada (dividida). Para obtener más información, consulte [Arquitectura a escala](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture).

>[!NOTE]
>
>La arquitectura a escala solo está disponible para cuentas con un clúster Pro 48 o superior.

La arquitectura de nivel dividido utiliza un mínimo de seis nodos: tres nodos de servicio que ejecutan [!DNL OpenSearch] o [!DNL Elasticsearch], [!DNL MariaDB] y [!DNL Redis] o [!DNL Valkey], y tres nodos web que ejecutan `php-fpm` y `NGINX`.

* Los nodos de servicio solo se pueden escalar verticalmente si aumenta el tamaño del servidor (CPU y memoria). Debido a que el clúster de base de datos está creado para alta disponibilidad, los nodos de servicio no pueden escalarse horizontalmente de forma fiable.
* Los nodos web se pueden escalar tanto vertical como horizontalmente, lo que agrega servidores web para gestionar un mayor volumen de solicitudes.

Esto le permite ampliar la infraestructura bajo demanda durante períodos de carga alta, adaptando cada nivel de forma independiente. Para cambiar a la arquitectura de nivel dividido antes de un período de carga pesada esperado, póngase en contacto con el equipo de cuenta de Adobe.
