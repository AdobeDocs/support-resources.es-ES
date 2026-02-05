---
title: Notas de la versión del portal Adobe Success
description: La información de la última versión de [!DNL Adobe Success portal].
feature: Release Notes
exl-id: be268e05-8298-4f21-8f2f-f66c52d76fe3
source-git-commit: 2894190b3171228e9c14a7cdef5bb2d92b97a6ec
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 83%

---

# Notas de la versión de [!DNL Adobe Success portal]

Estas notas de la versión contienen actualizaciones para [!DNL Adobe Success portal] e incluyen lo siguiente:

![Novedades:](../adobe-success-portal/assets/new.svg) nuevas características
![Correcciones](../adobe-success-portal/assets/fix.svg): correcciones y mejoras
![Errores](../adobe-success-portal/assets/bug.svg): problemas conocidos

## 4,0

_11 de noviembre de 2025_

![Corregir](../adobe-success-portal/assets/fix.svg) optimizó el orden de la conversación en la página de detalles del caso para desplazarse automáticamente al mensaje más reciente.

![Corregir](../adobe-success-portal/assets/fix.svg) se han actualizado los detalles de los casos para que cuando se abra en una nueva pestaña con **Ctrl+clic** / **Comando+clic**, el botón Atrás esté correctamente deshabilitado para evitar errores de navegación.

![Error](../adobe-success-portal/assets/bug.svg) Se ha corregido un problema por el que se mostraban detalles incorrectos de estado, región o zona horaria para las alertas de **[!UICONTROL Adobe Status]** en **[!UICONTROL Soporte e información]**.

![Error](../adobe-success-portal/assets/bug.svg) Resolvió los problemas de visualización con **[!UICONTROL Aceleradores]** y **[!UICONTROL Actividades]** vinculadas a **[!UICONTROL Socios estratégicos]**.

## 3.0

_9 de octubre de 2025_

![Nuevo](../adobe-success-portal/assets/new.svg) Se ha añadido una vista de calendario al módulo **[!UICONTROL Plan de acción]** para visualizar las cronologías de **[!UICONTROL Aceleradores]** y **[!UICONTROL Actividades]** vinculadas a **[!UICONTROL Objetivos clave de negocios]** (KBO).
* Acceda al calendario desde la página de KBO del plan de acción o desde las páginas de detalles **[!UICONTROL KBO]**/**[!UICONTROL Acelerador]**/**[!UICONTROL Actividad]** (solo si están vinculadas a un KBO).
* Cambie entre la vista Lista (predeterminada) y la vista Calendario.
* El calendario muestra las secciones contraíbles de cada KBO:
   * Azul para **[!UICONTROL Aceleradores]**
   * Verde para **[!UICONTROL Actividades]**
* Cada sección **[!UICONTROL Aceleradores]**/ **[!UICONTROL Actividades]** muestra el nombre, el estado y las fechas de inicio y finalización (con el formato *Mes XX*, *AAAA*).
* Al hacer clic en una tarjeta del evento, se abre una página con detalles del evento. Al hacer clic en el botón Atrás, volverá a la tarjeta del evento. 
* Los eventos están codificados por colores: azul para **[!UICONTROL Aceleradores]**, verde para **[!UICONTROL Actividades]**. Desplácese verticalmente por los KBO y horizontalmente por semana o mes.
* Las ayudas contextuales muestran nombres completos cuando se trunca el texto y la cronología permanece visible mientras se desplaza.
* La vista predeterminada es la semana actual; las flechas de navegación permiten moverse entre semanas.
* La vista Mes proporciona una cronología clara del trabajo en curso y planificado.

![Corrección](../adobe-success-portal/assets/fix.svg) Se han mejorado las páginas **[!UICONTROL Objetivos clave de negocios]** y **[!UICONTROL Actividades]** en el **[!UICONTROL Plan de acción]** para mostrar ayudas contextuales sobre las fechas de finalización, lo que se traduce en una mejora en la visibilidad de la cronología.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha añadido la búsqueda dentro de los filtros en **[!UICONTROL Plan de acción]** y **[!UICONTROL Rastreador de resultados]** para que la navegación sea más rápida.


![Corrección](../adobe-success-portal/assets/fix.svg) Se han añadido ayudas contextuales a cada hallazgo para obtener un contexto rápido.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha añadido la promoción de la marca Adobe a los archivos PDF descargados de los hallazgos y casos.

![Corrección](../adobe-success-portal/assets/fix.svg) Muestra todos los **[!UICONTROL socios estratégicos]** asociados a una cuenta, con indicadores de los contactos principales.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido un problema por el que las zonas horarias de **[!UICONTROL Alertas y estado de Adobe]** no reflejaban correctamente el perfil del usuario que ha iniciado sesión.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido un problema por el cual los filtros de **[!UICONTROL Alertas y estado de Adobe]** no funcionaban juntos como se esperaba.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido un problema en el cual la ordenación de **[!UICONTROL Casos de uso]** en las páginas Detalles de KBO y **[!UICONTROL Rastreador de resultados]** era inconsistente.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido un problema en el cual la información contextual sobre la página de la lista de casos no mostraba el nombre completo del caso al pasar el puntero por encima del título de un caso.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido un problema por el que el icono de la flecha hacia atrás no aparecía correctamente en el explorador Safari.

## 2.0

_11 de septiembre de 2025_

![Novedades](../adobe-success-portal/assets/new.svg) Se han añadido los campos siguientes a la página **[!UICONTROL Detalles de actividades]**:

* **[!UICONTROL Prioridad]**: indica el nivel de prioridad de una actividad. Los valores disponibles son *Urgente*, *Alta*, *Normal*, *Baja* y *Ninguna*. Si el valor es *Ninguna*, el campo **[!UICONTROL Prioridad]** no será visible en la interfaz de usuario del portal.
* **[!UICONTROL Propietario de Adobe]**: muestra el propietario de Adobe designado para la actividad.
* **[!UICONTROL Propietario del cliente]**: muestra el propietario desde el lado del cliente.
* **[!UICONTROL Pasos siguientes]**: muestra las siguientes acciones capturadas para la actividad.
* **[!UICONTROL Soluciones Adobe]**: indica las soluciones Adobe relacionadas con la actividad.

![Corrección](../adobe-success-portal/assets/fix.svg) Se han mejorado las páginas de **[!UICONTROL Objetivos clave de la empresa]** y **[!UICONTROL Actividades]** en el **[!UICONTROL Plan de acción]** para mostrar las fechas de finalización de cada acelerador y actividad, lo que ha mejorado la visibilidad de los plazos.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha mejorado la forma de mostrar los **[!UICONTROL casos de uso]** en la página de **[!UICONTROL Detalles de KBO]** para garantizar un diseño más limpio, una mejor facilidad de uso y una navegación coherente.

![Corrección](../adobe-success-portal/assets/fix.svg) Se ha corregido el problema al abrir en una nueva pestaña con **Ctrl+clic** (o **Comando+clic** en Mac) los vínculos de casos.
