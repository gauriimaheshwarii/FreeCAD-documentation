---
- GuiCommand:/ro
   Name:Sketcher CreateEllipseBy3Points
   Name/ro:Sketcher CreateEllipse3Point
   Icon:Sketcher_CreateEllipse_3points.png
   Workbenches:[Sketcher](Sketcher_Workbench/ro.md)
   MenuLocation:Sketch → Sketcher geometries → Create ellipse by 3 points
   Version:0.15
   SeeAlso:[Sketcher Ellipse by center](Sketcher_CreateEllipseByCenter/ro.md), [Sketcher Circle](Sketcher_CreateCircle/ro.md), [Sketcher Arc of Ellipse](Sketcher_CreateArcOfEllipse/ro.md)
---

# Sketcher CreateEllipseBy3Points/ro


</div>



## Descriere

This tool draws an ellipse by picking three points : (1) the periapsis (first crossing of longer diameter with ellipse), (2) the apoapsis (second crossing of longer diameter with ellipse), (3) one point on a side of the longer diameter (a) defining the minor radius (b). (c) is the resulting center and (f) are the focal points.

When starting the tool, the mouse pointer changes to a white cross with a red ellipse icon.

![](images/Ellipse_3Point.png‎ )


<div class="mw-translate-fuzzy">

#### Utiolizare


</div>




<div class="mw-translate-fuzzy">

#### Versiune


</div>

-   Press the **[<img src=images/Sketcher_CreateEllipseBy3Points.svg style="width:16px"> [Create ellipse by 3 points](Sketcher_CreateEllipseBy3Points.md)** button.
-   First click in 3D view sets a point that defines the crossing of the major diameter with the ellipse (periapsis). Second click in 3D view sets a point that defines the crossing of the major diameter with the ellipse opposite to the center point (apoapsis). Third click sets a point on the ellipsis defining the minor radius.

-   After the third click, the ellipse is created, together with a set of construction geometry aligned to it (major diameter, minor diameter, two foci). The construction geometry can be manually deleted if not needed, and recreated later. See [Internal Alignment Constraint](Sketcher_ConstrainInternalAlignment.md) and [Sketcher Show Hide Internal Geometry](Sketcher_RestoreInternalAlignmentGeometry.md).
-   Pressing **ESC** or clicking the right mouse button cancels the function.

## Peculiarities

-   Major and minor axes of ellipses are strict and cannot be swapped by resizing the ellipse. This is a consequence of the solver parametrization used (center (x,y), focus1 (x,y) and minor radius length (b)) and the same strict behavior of OpenCascade. The ellipse must be rotated to swap the axes.
-   Ellipse can function as a circle when its major and minor diameter lines are deleted, and one of the foci is constrained to coincide with the center. But radius constraint won\'t work on such a circle.
-   Moving the ellipse by edge is the same as moving ellipse\'s center.





{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher CreateEllipseBy3Points/ro
