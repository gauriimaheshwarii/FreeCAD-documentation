---
- GuiCommand:/ru
   Name:Std ViewZoomOut
   Name/ru:Уменьшить
   MenuLocation:Вид → Масштаб‏‎ → Уменьшить
   Workbenches:All
   Shortcut:**Ctrl**+**-**
   SeeAlso:[Увеличить](Std_ViewZoomIn/ru.md), [Увеличить область](Std_ViewBoxZoom/ru.md)
---

# Std ViewZoomOut/ru

## Описание

The **Std ViewZoomOut** command zooms out in the active [3D view](3D_view.md).

## Применение

1.  There are several ways to invoke the command:
    -   Select the **View → Zoom → <img src="images/Std_ViewZoomOut.svg" width=16px> Zoom Out** option from the menu.
    -   Use the keyboard shortcut: **Ctrl**+**-**.

## Примечания

-   It is also possible to zoom with the mouse scroll wheel.

## Настройки

-   The zoom factor can be changed in the preferences: **Edit → Preferences... → Display → Navigation → Zoom step**. This setting also affects scroll wheel zoom. See [Preferences Editor](Preferences_Editor#Navigation.md).

## Scripting


**Смотрите так же:**

[Основы составления скриптов в FreeCAD](FreeCAD_Scripting_Basics/ru.md).

To zoom out use the `zoomOut` method of the ActiveView object. This method is not available if FreeCAD is in console mode.


```python
import FreeCADGui

FreeCADGui.ActiveDocument.ActiveView.zoomOut()
```





{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std ViewZoomOut/ru
