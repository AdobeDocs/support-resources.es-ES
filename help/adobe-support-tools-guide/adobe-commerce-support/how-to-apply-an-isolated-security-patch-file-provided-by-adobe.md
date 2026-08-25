---
title: Cómo aplicar un parche aislado proporcionado por Adobe
description: Este artículo explica cómo aplicar un parche aislado para Adobe Commerce local, Adobe Commerce en la infraestructura de la nube y Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Cómo aplicar un parche aislado proporcionado por Adobe

Este artículo explica cómo aplicar un parche aislado para Adobe Commerce local, Adobe Commerce en la infraestructura de la nube y Magento Open Source.

>[!WARNING]
>
>Recomendamos encarecidamente aplicar y probar el parche en el entorno de ensayo/integración antes de aplicarlo a producción. También le recomendamos que tenga una copia de seguridad reciente antes de realizar cualquier manipulación.

## Cómo aplicar un parche aislado para Adobe Commerce en la infraestructura en la nube {#cloud}

1. Si no tiene un directorio llamado `m2-hotfixes` en la raíz del proyecto, cree uno.
1. Copie los `%patch_name%.patch` archivos en el directorio `m2-hotfixes`.
1. Añada, confirme e inserte los cambios de código:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Para obtener información adicional sobre cómo aplicar parches a proyectos en la nube, consulte [Aplicar parches](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches).

## Cómo aplicar un parche aislado para Adobe Commerce local y Magento Open Source {#commerce}

1. Cargue el parche en el directorio raíz de Adobe Commerce local o de Magento Open Source.
1. Ejecute el siguiente comando SSH:

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   (Si el comando anterior no funciona, intente usar `-p2` en lugar de `-p1`)

1. Para que se reflejen los cambios, actualice la caché en [!UICONTROL Admin] en **[!UICONTROL Sistema]** > **[!UICONTROL Administración de caché]**.
