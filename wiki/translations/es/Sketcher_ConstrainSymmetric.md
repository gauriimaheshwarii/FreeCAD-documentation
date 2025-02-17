---
- GuiCommand:/es
   Name:Constraint Symmetric
   Name/es:Restricción Simetría
   Workbenches:[Croquizador](Sketcher_Workbench/es.md)
   MenuLocation:Croquis → Restricciones del Croquizador → Restricción de Simetría
   Shortcut:S
   SeeAlso:[Restricción Paralela](Sketcher_ConstrainParallel/es.md)
---

# Sketcher ConstrainSymmetric/es


</div>

## Descripción


<div class="mw-translate-fuzzy">

#### Descripción 

La Restricción de Simetría restringe dos puntos seleccionados a ser simétricos con respecto a un eje dado. Los dos puntos seleccionados se restringen para situarse sobre la perpendicular al eje de simetría y situados a la misma distancia de este.


</div>


<div class="mw-translate-fuzzy">

#### Funcionamiento

<img alt="" src=images/SymmetricConstraint1.png  style="width:256px;">

Selecciona dos puntos y una línea en el croquis. Los puntos y la línea seleccionados se volverán de color verde oscuro.

<img alt="" src=images/SymmetricConstraint2.png  style="width:256px;">

Pulsa sobre el icono <img alt="" src=images/Constraint_Symmetric.png  style="width:16px;"> en la barra de herramientas del Croquizador o selecciona la Restricción de Simetría en el submenú de Restricciones del entorno del Croquizador (o del entorno de Diseño de Piezas). Esto aplicará la restricción a los elementos seleccionados.

<img alt="" src=images/SymmetricConstraint3.png  style="width:256px;">

Esta es una restricción geométrica y no tiene parámetros editables.


</div>

<img alt="" src=images/SymmetricConstraint1.png  style="width:500px;">

Select two points (vertexes) in the sketch and a line in the sketch. The selected points and the line will be dark green.

<img alt="" src=images/SymmetricConstraint2.png  style="width:500px;">

Click on **[<img src=images/Sketcher_ConstrainSymmetric.svg style="width:16px"> [Constrain symmetric](Sketcher_ConstrainSymmetric.md)** or select the Constrain Symmetrical menu item from the Sketcher Constraints sub menu of the Sketcher (or Part Design) menu item.

This will apply the constraint to the selected items.

<img alt="" src=images/SymmetricConstraint3.png  style="width:500px;">


**Note:**

Before Version 0.19 (see fix [1](https://github.com/FreeCAD/FreeCAD/pull/3746)), if you want to define a symmetry constraint with respect to a point, the order of the selection is important, depending on if you select the tool at the beginning or at the end.

-   If you click the tool first: select the first point, then the symmetry reference point, and finally the second point.
-   If you click the tool last: select the first point, then the second point, and finally the symmetry reference point.

See the tracker [issue #4144](https://freecadweb.org/tracker/view.php?id=4144), and [forum thread](https://forum.freecadweb.org/viewtopic.php?f=3&t=39611).

## Scripting

Two points and a symmetry line:


```pythonSketch.addConstraint(Sketcher.Constraint('Symmetric', Line1, PointOfLine1, Line2, PointOfLine2, SymmetryLine))```

Two points and a symmetry point:


```pythonSketch.addConstraint(Sketcher.Constraint('Symmetric', Line1, PointOfLine1, Line2, PointOfLine2, LineS, PointOfLineS))```

A line and a symmetry point (In the GUI one can select a line and a point, but it uses internally the same form as above, with the two extremities of the same line):


```pythonSketch.addConstraint(Sketcher.Constraint('Symmetric', Line, 1, Line, 2, LineS, PointOfLineS))```

The [Sketcher scripting](Sketcher_scripting.md) page explains the values which can be used for `Line1`, `Line2`, `LineS`, `Line`, `PointOfLine1`, `PointOfLine2` and `PointOfLineS`, and contains further examples on how to create constraints from Python scripts.





{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainSymmetric/es
