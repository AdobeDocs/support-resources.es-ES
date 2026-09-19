---
title: Cómo aplicar un parche del compositor proporcionado por Adobe
description: Este artículo explica cómo aplicar un parche del compositor para Adobe Commerce local, Adobe Commerce en la infraestructura en la nube y Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
exl-id: 66d8df60-4c4a-49ef-8107-986e10d6e289
source-git-commit: 32e69e55405db4f7bb78ef055e07175336401179
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%
---
# Cómo aplicar un parche del compositor proporcionado por Adobe

Este artículo explica cómo aplicar un parche del compositor para Adobe Commerce local, Adobe Commerce en la infraestructura en la nube y Magento Open Source.

>[!WARNING]
>
>Recomendamos encarecidamente aplicar y probar el parche en el entorno de ensayo/integración antes de aplicarlo a producción. También le recomendamos que tenga una copia de seguridad reciente antes de realizar cualquier manipulación.

## Cómo aplicar un parche del compositor para Adobe Commerce en la infraestructura en la nube {#cloud}

1. Si no tiene un directorio llamado `m2-hotfixes` en la raíz del proyecto, cree uno.
1. Copie los `%patch_name%.composer.patch` archivos en el directorio `m2-hotfixes`.
1. Añada, confirme e inserte los cambios de código:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

Para obtener información adicional sobre cómo aplicar parches a proyectos en la nube, consulte [Aplicar parches](https://experienceleague.adobe.com/es/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches) en nuestra documentación para desarrolladores.

## Cómo aplicar un parche del compositor para Adobe Commerce local y Magento Open Source {#commerce}

1. Cargue el parche en el directorio raíz de Adobe Commerce local o de Magento Open Source.
1. Ejecute el siguiente comando SSH:

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   (Si el comando anterior no funciona, intente usar `-p2` en lugar de `-p1` )

1. Para que se reflejen los cambios, actualice la caché en el Administrador en **[!UICONTROL Sistema]** > **[!UICONTROL Administración de caché]**.
