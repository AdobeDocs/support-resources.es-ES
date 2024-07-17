---
title: Saltos de tabla
description: Prueba de diferentes saltos de tabla
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# Saltos de tabla

No hay mucho que ver aquí.

## Tabla de marcado estándar con `<br>`

**CORREGIDO`Green<br>Red<br>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<br>Rojo<br>Azul |
| María | 23 | Amarillo<br>Marrón |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<br>Red<br>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<br>Rojo<br>Azul |
| María | 23 | Amarillo<br>Marrón |

{style="table-layout:auto"}

## Tabla de Markdown con `<br>`s dobles

**CORREGIDO`Green<br><br>Red<br><br>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Rojo<br><br>Azul |
| María | 23 | Amarillo<br><br>Marrón |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<br><br>Red<br><br>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Rojo<br><br>Azul |
| María | 23 | Amarillo<br><br>Marrón |

{style="table-layout:auto"}

## Tabla de Markdown con `<p>`

**CORREGIDO`Green<p>Red<p>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<p>Rojo<p>Azul |
| María | 23 | Amarillo<p>Marrón |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<p>Red<p>Blue`**

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Verde<p>Rojo<p>Azul |
| María | 23 | Amarillo<p>Marrón |

{style="table-layout:auto"}

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Este es el color **verde** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. <p>Este es el color **rojo** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. <p>Este es el color **azul** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. |
| María | 23 | Amarillo<p>Marrón |

{style="table-layout:fixed"}

|  | Número | Colores |
|---|---|---|
| Juanya | 17 | Este es el color **verde** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. <p>Este es el color **rojo** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. <p>Este es el color **azul** y está diseñado para ajustarse a una línea diferente como cuestión o como medio para probar los saltos de párrafo mencionados. |
| María | 23 | Amarillo<p>Marrón |

{style="table-layout:auto"}
