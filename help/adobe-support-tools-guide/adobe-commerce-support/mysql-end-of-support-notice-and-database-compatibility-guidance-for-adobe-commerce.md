---
title: Aviso de fin de soporte MySQL y guía de compatibilidad de bases de datos para Adobe Commerce
description: Este artículo proporciona información sobre las escalas de tiempo de fin de soporte de MySQL y la guía de compatibilidad de bases de datos para las versiones de Adobe Commerce compatibles.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Aviso de fin de soporte MySQL y guía de compatibilidad de bases de datos para Adobe Commerce

Este artículo proporciona información importante sobre el fin de la compatibilidad con MySQL (EOS) y la compatibilidad con bases de datos para versiones de Adobe Commerce compatibles.
Adobe recomienda encarecidamente que los comerciantes revisen este anuncio y tomen medidas para mantener la estabilidad de la plataforma y cumplir con los requisitos de asistencia.
Obtenga más información en los [requisitos previos de actualización para MariaDB](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) y los [requisitos del sistema](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).

## Fin de soporte de MySQL 8.0 (EOS)

MySQL 8.0 llega al fin del soporte (EOS) el 30 de abril de 2026.
Después de esta fecha, las siguientes versiones de Adobe Commerce no admitirán ni mantendrán la compatibilidad con las versiones de MySQL publicadas después de MySQL 8.0:

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe no validará ni proporcionará compatibilidad con las versiones principales más recientes de MySQL en estas versiones de Adobe Commerce.

## Acción necesaria para los clientes locales

Se recomienda migrar los servidores de base de datos de las instalaciones locales de Adobe Commerce que ejecuten las siguientes versiones a una versión compatible de MariaDB:

* 2.4.5
* 2.4.6
* 2.4.7

MariaDB es totalmente compatible con estas versiones y es la plataforma de base de datos recomendada a partir de ahora.

* 2.4.5
* 2.4.6
* 2.4.7

Se recomienda migrar sus servidores de bases de datos a una versión de MariaDB compatible.
MariaDB es totalmente compatible con estas versiones de Adobe Commerce y es la plataforma de base de datos recomendada.

## Compatibilidad con MySQL en Adobe Commerce 2.4.8 y 2.4.9

Adobe Commerce 2.4.8 y 2.4.9 son las últimas versiones de Adobe Commerce que admiten MySQL.

Para estas versiones:
* MySQL 8.4 es la versión final de MySQL compatible con Adobe Commerce.
* Ninguna versión de MySQL publicada después de la versión 8.4 será certificada o compatible con Adobe Commerce.

## Dirección futura: MariaDB como plataforma de base de datos predeterminada

En adelante, Adobe Commerce seguirá admitiendo MariaDB como plataforma de base de datos predeterminada y recomendada.

Adobe recomienda encarecidamente que los siguientes clientes empiecen a planificar su migración a MariaDB para mantener la compatibilidad y la alineación de la asistencia a largo plazo:
* Todos los clientes locales de Adobe Commerce 2.4.8 y 2.4.9
* Clientes que ejecutan versiones de Adobe Commerce compatibles anteriores
