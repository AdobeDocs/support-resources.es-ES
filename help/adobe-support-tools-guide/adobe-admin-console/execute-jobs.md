---
title: Ejecutar trabajos pendientes
description: Obtenga información sobre cómo ejecutar trabajos pendientes en Adobe Admin Console para asegurarse de que todos los cambios se aplican a su organización.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Ejecutar trabajos pendientes

Esta característica se aplica a las organizaciones empresariales que usan [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

- Los cambios en [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) se completan en dos fases:

   1. **Editar fase**: realice cambios en las organizaciones o asigne productos.
   2. **Fase de ejecución**: revise y ejecute los cambios pendientes para que surtan efecto.

- Para asegurarse de que todos los cambios realizados en [[!DNL Global Admin Console]](https://helpx.adobe.com/es/enterprise/global-admin-console/adopt-global-administration.html) estén implementados y surtan efecto, seleccione la pestaña **[!UICONTROL Ejecución de trabajo]** y continúe con la ejecución de los cambios pendientes.

  Inicie sesión en [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

## Persistencia y visibilidad de los cambios

### Cambiar persistencia

- Puede cerrar la sesión y volver más tarde sin perder los cambios pendientes.
- Cambios sin ejecutar:
   - Se descartan pasados 30 días.
   - Se borran al finalizar la sesión, por ejemplo cuando se cierra la pestaña o la ventana del explorador.

&#x200B;> [!NOTE]
>
> Ejecute los cambios importantes con prontitud para garantizar que se aplican correctamente.

### Varios administradores y conflictos

- Dos administradores que trabajan en la misma organización:
   - No vea los cambios no ejecutados de los demás.
   - Ver cambios solo después de:
      - Ejecución, y
      - Actualizando la pantalla o iniciando sesión de nuevo.
- Los cambios no ejecutados pueden entrar en conflicto con los ya ejecutados.

### Gestión de conflictos

Se informa de los conflictos:
- En tiempo de ejecución, o
- Cuando se actualizan los datos (por ejemplo, después de cerrar la sesión y volver a iniciarla).

## Ejecutando cambios pendientes

Como administrador global, puede revisar y ejecutar los cambios pendientes desde la ficha **[!UICONTROL Ejecución de trabajos]**.

### Pasos para ejecutar los cambios

1. Inicie sesión en [!DNL Global Admin Console].
2. Seleccione la ficha **[!UICONTROL Ejecución de trabajo]** en el panel de navegación izquierdo.
3. Revise los cambios pendientes.
4. Seleccione **[!UICONTROL Enviar cambios]** para ejecutarlos.

Después de ejecutar el trabajo:

- El trabajo entra en la cola de ejecución.
- El estado es **[!UICONTROL Pendiente]** mientras se ejecuta el trabajo.
- Adobe recomienda ejecutar solo un trabajo a la vez para facilitar la predictibilidad y la resolución de problemas.

&#x200B;> [!IMPORTANT]
>
> Si se produce un error durante la ejecución, los cambios que no se hayan aplicado correctamente deben volver a introducirse y enviarse.

### Asignaciones de larga duración

Si la asignación de un producto tarda más de 12 horas:
- El trabajo está marcado como **[!UICONTROL Error]**.
- No se ejecuta ninguna tarea pendiente subsiguiente de ese trabajo.

![trabajos pendientes](assets/pending-jobs.png)

## Cancelar un trabajo en ejecución

Puede cancelar un trabajo que se esté ejecutando actualmente desde la ficha **[!UICONTROL Ejecución del trabajo]**.

### Pasos para cancelar un trabajo en ejecución

1. Inicie sesión en [!DNL Global Admin Console].
2. Seleccione **[!UICONTROL Ejecución de trabajo]**.
3. Seleccione **[!UICONTROL Cancelar trabajo en ejecución]**.

### Comportamiento de cancelación

1. El trabajo se detiene al final del paso actual.
2. El trabajo no se detiene en medio de un paso.
3. Algunos pasos pueden tardar minutos u horas en completarse.
4. Durante este tiempo, el trabajo puede permanecer en estado **[!UICONTROL Cancelando]**.

&#x200B;> [!NOTE]
>
> Planifique las cancelaciones con el entendimiento de que la finalización del paso actual puede retrasar significativamente el momento en que se detiene el trabajo.

## Ver historial de trabajos

- Para ver los trabajos ejecutados en los últimos 30 días:

   1. Inicie sesión en [!DNL Global Admin Console].
   2. Seleccione **[!UICONTROL Ejecución de trabajo]**.
   3. Desplácese al final de la página.
   4. Seleccione **[!UICONTROL Trabajos recientes]**.

- Se muestran trabajos recientes:
   - Envió **comandos de trabajo**.
   - **Errores** y **advertencias** asociados con la ejecución.

&#x200B;> [!NOTE]
>
> Los posteriores cambios de nombre o eliminaciones de los objetos relacionados **no afectan** al modo en que se muestran los comandos en el historial de trabajos. El historial refleja el estado en el momento del envío.
