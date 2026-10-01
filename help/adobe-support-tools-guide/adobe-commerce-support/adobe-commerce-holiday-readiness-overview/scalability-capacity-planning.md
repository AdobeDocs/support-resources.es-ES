---
title: Escalabilidad y planificación de capacidades
description: Recomendaciones de escalabilidad y planificación de la capacidad para ayudar a los comerciantes de Adobe Commerce a preparar sus entornos para eventos de alto tráfico como la temporada de vacaciones.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-wordcount: '413'
ht-degree: 0%
---

# Escalabilidad y planificación de capacidades

En esta sección se proporcionan recomendaciones técnicas para escalar los entornos de Adobe Commerce con el fin de prepararse para eventos de alto tráfico como la temporada de vacaciones.

>[!NOTE]
>
>Los pasos marcados **(solo en la nube)** se aplican a Commerce en la infraestructura en la nube. La mayoría de las demás recomendaciones también se aplican a las implementaciones locales.

## Planificar la actualización anticipada del clúster (solo en la nube) {#plan-cluster-upsize-early}

Para los clientes de Commerce en infraestructura en la nube, un aumento temporal del tamaño del clúster asigna más recursos informáticos para gestionar los aumentos repentinos del tráfico en temporada alta. Genere un ticket de asistencia por adelantado con el intervalo de fechas y el tamaño de clúster requerido, y coordine con su administrador de cuentas dedicado el consumo de recursos y los requisitos actuales. Envíe la solicitud al menos 48 horas hábiles antes de que se necesite la capacidad; para la temporada de vacaciones específicamente, envíe lo antes posible, ya que la capacidad durante Black Friday y Cyber Monday es limitada. Ver [Cómo solicitar un cambio temporal](https://experienceleague.adobe.com/es/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize).

Por ejemplo, un cliente de Pro-Architecture con una línea de base diaria de 24 núcleos (24 vCPUs, 96 GB RAM) que se convierte a 96 núcleos durante 7 días utilizaría aproximadamente 4 veces los recursos (96 vCPUs, 384 GB RAM), un consumo incremental de aproximadamente 504 vCPU-días (96×7 − 24×7).

## Protección de origen rápido {#fastly-origin-shielding}

El propósito del blindaje de origen de Adobe Commerce [!DNL Fastly] es reducir el tráfico directamente al origen de Adobe Commerce. Cuando se recibe una solicitud, una ubicación perimetral [!DNL Fastly] (punto de presencia) comprueba el contenido almacenado en caché y lo envía. Si no se almacena en caché, continúa a la POP de escudo para comprobar si se almacena en caché; si el contenido se ha solicitado anteriormente, incluso desde otro POP global, se almacenará en caché. Por último, si no se almacena en caché en el POP de Shield, solo entonces se dirigirá al servidor de origen.

El blindaje de origen [!DNL Fastly] se puede habilitar en el administrador de Adobe Commerce, en la configuración del servidor de [!DNL Fastly]. Elija una ubicación de escudo más cercana a su centro de datos de origen de Adobe Commerce para obtener el mejor rendimiento. Para obtener más información, consulte [Configurar back-ends y blindaje de origen](https://experienceleague.adobe.com/es/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding). De manera predeterminada, el blindaje de origen [!DNL Fastly] no está habilitado.

## Realizar pruebas de carga y conmutación por error {#conduct-load-and-failover-tests}

Realice pruebas de carga y recuperación antes de las campañas principales para validar las configuraciones de escalado y los planes de reversión.