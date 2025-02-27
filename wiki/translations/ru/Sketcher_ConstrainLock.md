---
- GuiCommand:/ru
   Name:Sketcher ConstrainLock
   Name/ru:Sketcher ConstrainLock
   MenuLocation:Sketch → Ограничения эскиза → Ограничение положения
   Workbenches:[Sketcher](Sketcher_Workbench/ru.md)
   SeeAlso:[Sketcher Constrain Block](Sketcher_ConstrainBlock/ru.md)
---

# Sketcher ConstrainLock/ru


</div>

## Описание

**Constraint Lock** applies **[<img src=images/Sketcher_ConstrainDistanceX.svg style="width:16px"> [Horizontal distance](Sketcher_ConstrainDistanceX.md)** and **[<img src=images/Sketcher_ConstrainDistanceY.svg style="width:16px"> [Vertical distance](Sketcher_ConstrainDistanceY.md)** constraints to selected vertices (points) in the sketch. If a single vertex is selected, the horizontal and vertical distance constraints will refer to the sketch origin point. If two or more points are selected, horizontal and vertical distance constraints will be added for each pair of points. There is no automatic prompt to edit the constraints\' values, they must be edited manually.

## Применение

1.  Select one or more vertices (points) in the sketch.
2.  Press the **[<img src=images/Sketcher_ConstrainLock.svg style="width:16px"> [Constrain lock](Sketcher_ConstrainLock.md)** button.
3.  To edit the constraints values, double-click on a constraint value in the 3D view, or double-click on the constraint or right-click and select **Edit value** in the Constraint list in the Tasks tab.

**Note:** the constraint tool can also be started with no prior selection, but it will then only work on a single vertex, and reference the constraints to the sketch origin point. By default the command will be in continue mode to create new constraints; press the right mouse button or **ESC** once to quit the command.

## Программирование

The <img alt="" src=images/Sketcher_ConstrainLock.svg  style="width:24px;"> [Lock](Sketcher_ConstrainLock.md) constraint is a GUI command which creates a <img alt="" src=images/Sketcher_ConstrainDistanceX.svg  style="width:24px;"> [Horizontal distance](Sketcher_ConstrainDistanceX.md) and a <img alt="" src=images/Sketcher_ConstrainDistanceY.svg  style="width:24px;"> [Vertical distance](Sketcher_ConstrainDistanceY.md) constraint, it is not a constraint of its own. See the [Sketcher scripting](Sketcher_scripting.md) page for details and examples on how to create these constraints from Python scripts.


<div class="mw-translate-fuzzy">





</div>


{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainLock/ru
