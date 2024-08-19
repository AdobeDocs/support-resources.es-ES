---
title: Barra oblicua en los bloques de código UGP-11189
description: Barra oblicua en los bloques de código Prueba UGP-11189
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Barra oblicua en bloques de código

1. Ejecute el comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Ejecute el comando (sin escape):

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

No está en el bloque de código

proveedor/bin/magento-parches -n estado |grep &quot;27015\|Estado&quot;

Escapado:

proveedor/bin/magento-parches -n estado |grep &quot;27015&amp;bsol;|Status&quot;

