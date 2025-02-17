---
- GuiCommand:/es
   Name:Sketcher ConstrainDistance
   Name/es:Restricción de distancia
   Workbenches:[Croquizador](Sketcher_Workbench/es.md)
   MenuLocation:Sketch → Restricciones de croquis → Restricción de distancia
   Shortcut:May + D
   SeeAlso:[Distancia Horizontal](Sketcher_ConstrainDistanceX/es.md), [Distancia Vertical](Sketcher_ConstrainDistanceY/es.md)
---

# Sketcher ConstrainDistance/es


</div>

## Description


<div class="mw-translate-fuzzy">

## Descripción

La Restricción de Distancia restringe la longitud de una línea, la distancia perpendicular entre un punto y una línea o la distancia entre dos puntos a un valor específico.


</div>

![](images/Sketcher_ConstrainDistance_example.png )


<div class="mw-translate-fuzzy">

## Utilización


</div>

1.  Pick two points or one line or one point and one line.
2.  Invoke the command several ways:
    -   Press the **[<img src=images/Sketcher_ConstrainDistance.svg style="width:16px"> [Constrain distance](Sketcher_ConstrainDistance.md)** button in the Sketcher toolbar.
    -   Use the **K** then **D** keyboard shortcut.
    -   Use the **Sketch → Sketcher constraints → [<img src=images/Sketcher_ConstrainDistance.svg style="width:16px"> Constrain distance** entry from the top menu.
3.  A pop up dialog opens to edit or confirm the value. Press **OK** to validate.

**Note:** the constraint tool can also be started with no prior selection. To set the perpendicular distance between a point and a line, the point needs to be selected first. By default the command will be in continue mode to create new constraints; press the right mouse button or **Esc** once to quit the command.

### Hint

If applicable please consider using the **[<img src=images/Sketcher_ConstrainDistanceX.svg style="width:16px"> [Horizontal distance](Sketcher_ConstrainDistanceX.md)** or **[<img src=images/Sketcher_ConstrainDistanceY.svg style="width:16px"> [Vertical distance](Sketcher_ConstrainDistanceY.md)** constraints instead. These constraints are more robust and faster to calculate than the **ConstrainDistance** tool.

## Scripting

Distance from origin:


```pythonSketch.addConstraint(Sketcher.Constraint('DistanceX', Edge, PointOfEdge, App.Units.Quantity('123.0 mm')))```

Distance between two vertices:


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Edge1, PointOfEdge1, Edge2, PointOfEdge2, App.Units.Quantity('123.0 mm')))```

Length of line (the GUI allows selecting the edge itself, but it is just a shorthand for using the two extremities of the same line):


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Line, 1, Line, 2, App.Units.Quantity('123.0 mm')))```

Distance from point (`Edge, PointOfEdge`) to nearest point on line (`Line`):


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Edge, PointOfEdge, Line, App.Units.Quantity('123.0 mm')))```

The [Sketcher scripting](Sketcher_scripting.md) page explains the values which can be used for `Edge1`, `Edge2`, `Edge`, `PointOfEdge1`, `PointOfEdge2`, `PointOfEdge` and `Line`, and contains further examples on how to create constraints from Python scripts.





{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainDistance/es
