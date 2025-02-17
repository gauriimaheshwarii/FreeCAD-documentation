---
- GuiCommand:/ru
   Name:Arch Roof
   Name/ru:Arch Roof
   MenuLocation:Архитектура → Крыша
   Workbenches:[Arch](Arch_Workbench/ru.md)
   Shortcut:**R** **F**
---

# Arch Roof/ru


</div>

## Описание

The **<img src="images/Arch_Roof.svg" width=16px> [Arch Roof](Arch_Roof.md)** tool allows for the creation of a sloped roof from a selected wire. The created roof object is parametric, keeping its relationship with the base object. The principle is that each edge is seen allotting a profile of roof (slope, width, overhang, thickness).

**Note:** This tool is still in development, and might fail with very complex shapes.

<img alt="" src=images/RoofExample.png  style="width:600px;"> 
*View from above a building model showing the roof with certain transparency*

## Применение

1.  Create a wire with following the counter-clockwise direction and select it.

    :   <img alt="" src=images/CounterclockwiseWire.png  style="width:600px;">

2.  Press the **<img src="images/Arch_Roof.svg" width=16px> [Arch Roof](Arch_Roof.md)** button, or press **R** then **F** keys

3.  The default roof object could have a strange shape, it\'s because the tool is missing some necessary information.

4.  After creating the default roof, double click on the object in the [tree view](tree_view.md) to access and edit all the properties. Angle must be between 0 and 90.

    :   ![](images/RoofTable.png )

5.  Each line corresponds to a roof pane. So you can set the properties you want for each roof pane.

6.  To help you, you can set `Angle` or `Run` to `0` and define a `Relative Id`, this makes an automatic calculation to find the data relative to the `Relative Id`.

7.  It works like this:
    1.  If `Angle &#61; 0` and `Run &#61; 0` then profile is identical to the relative profile.
    2.  If `Angle &#61; 0` then `Angle` is calculated so that the height is the same one as the relative profile.
    3.  If `Run &#61; 0` then `Run` is calculated so that the height is the same one as the relative profile.

8.  Finally, set an Angle to 90° to make a gable.

    :   <img alt="" src=images/RoofProfil.png  style="width:600px;">

9.  
    **Note**: for better comprehension, please see this [youtube clip](https://www.youtube.com/watch?v=4Urwru71dVk).

## Опции

-   Крыши обладают таким же свойствами и моделью поведения, как и все остальные [компоненты верстака Arch](Arch_Component/ru.md)

## Свойства

-    **Angles**: List of the slope angle of the roof pane (an angle for each edge in the wire).

-    **Runs**: List of the width of the roof pane (a run for each edge in the wire).

-    **IdRel**: List of relation Id of the slope angle of the roof.

-    **Thickness**: List of thickness of the roof pane. (a thickness for each edge in the wire).

-    **Overhang**: List of the overhang of the roof pane (an overhang for each edge in the wire).

-    **Face**: The face index of the base object to be used (not really used).

## Программирование


**См. так же:**

[Arch API](Arch_API/ru.md) и [Основы составления скриптов FreeCAD](FreeCAD_Scripting_Basics/ru.md).

The Roof tool can be used in [macros](macros.md) and from the [Python](Python.md) console by using the following function: 
```python
Roof = makeRoof(baseobj=None, facenr=0, angles=[45.,], run=[], idrel=[0,], thickness=[50.,], overhang=[100.,], name="Roof")
```

-   Creates a `Roof` object from the given `baseobj`, which can be a closed wire or a solid object.
    -   If `baseobj` is a wire, you can provide lists for `angles`, `run`, `idrel`, `thickness`, and `overhang`, for each edge in the wire to define the shape of the roof.
    -   The lists are automatically completed to match the number of edges in the wire.

Пример:


```python
import FreeCAD as App
import Arch, Draft

doc = App.newDocument()

rect = Draft.makeRectangle(3000, 4000)
doc.recompute()

roof = Arch.makeRoof(rect, angles=[30.,])

p1 = App.Vector(0, 0, 0)
p2 = App.Vector(1000, 1000, 0)
p3 = App.Vector(0, 2000, 0)

wire = Draft.make_wire([p1, p2, p3], closed=True)
doc.recompute()

roof1 = Arch.makeRoof(wire)

doc.recompute()
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Arch](Arch_Workbench.md) > Arch Roof/ru
