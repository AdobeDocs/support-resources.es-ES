---
title: Barra oblicua en los bloques de código UGP-11189
description: Barra oblicua en los bloques de código Prueba UGP-11189
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Barra oblicua en bloques de código

1. Ejecute el comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Siguiente paso

No está en el bloque de código

proveedor/bin/magento-parches -n estado |grep &quot;27015\|Estado&quot;

Barra invertida omitida:

proveedor/bin/magento-parches -n estado |grep &quot;27015&bsol;|Status&quot;
