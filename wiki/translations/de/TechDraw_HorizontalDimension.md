---
- GuiCommand:/de
   Name:TechDraw Dimension Horizontal
   Name/de:TechDraw MaßHorizontal
   MenuLocation:TechDraw → Bemaßungen → Horizontales Maß einfügen
   Workbenches:[TechDraw](TechDraw_Workbench/de.md)
   Shortcut:**Shift** + **H**
   SeeAlso:[TechDraw Längenmaß](TechDraw_LengthDimension/de.md), [TechDraw MaßVertikal](TechDraw_VerticalDimension/de.md)
---

# TechDraw HorizontalDimension/de

## Beschreibung

Das Werkzeug MaßHorizontal fügt einer Ansicht ein horizontales Maß hinzu. Das Maß kann zwischen zwei Eckpunkten liegen, die Länge einer Kante oder der horizontale Abstand zwischen zwei Kanten sein. Der Abstand ist zuerst der projizierte Abstand (wie in der Zeichnung dargestellt), kann aber unter Verwendung des Werkzeugs **<img src="images/TechDraw_LinkDimension.svg" width=16px> [MaßVerknüpfen](TechDraw_LinkDimension/de.md)** auf den eigentlichen 3D-Abstand geändert werden.

<img alt="" src=images/TechDraw_Dimension_Horizontal_example.png  style="width:200px;"> 
*Längenbemaßung zweier beliebiger Knoten der Ansicht, der Abstand wird in horizontaler Richtung gemessen*

## Anwendung

1.  Punkte oder Kanten auswählen, die deine Messung festlegen.
2.  Die Schaltfläche **<img src="images/TechDraw_HorizontalDimension.svg" width=16px> [Horizontales Maß einfügen](TechDraw_HorizontalDimension/de.md)** drücken.
3.  Ein Maß wird der Ansicht hinzugefügt. Das Maß kann an die gewünschte Position gezogen werden.
4.  Falls erforderlich, können Toleranzen, wie auf der [GD&T-Seite](TechDraw_Geometric_dimensioning_and_tolerancing/de#Toleranzen.md) beschrieben, hinzugefügt werden.

Um die Eigenschaften eines Dimension-Objekts zu ändern, doppelklickt man sie entweder in der Zeichnung oder in der [Baumansicht](Tree_view/de.md). Dadurch wird der [Bemaßungsdialog](TechDraw_LengthDimension/de#Bemaßungsdialog.md) geöffnet.

## Einschränkungen

Dimension-Objekte (Maße) sind anfällig für das \"[Topological-Naming-Problem](topological_naming_problem/de.md)\" (Problem der topologischen Benennung). Siehe [TechDraw Längenmaß](TechDraw_LengthDimension/de.md) für weitere Informationen.

## Eigenschaften

Siehe [TechDraw Längenmaß](TechDraw_LengthDimension/de#Eigenschaften.md).

## Skripten

Siehe auch: [Autogenerierte API Dokumentation](https://freecad.github.io/SourceDoc/) und [FreeCAD Grundlagen Skripten](FreeCAD_Scripting_Basics/de.md).

Das Werkzeug MaßHorizontal kann in [Makros](Macros/de.md) und von der [Python](Python/de.md)-Konsole aus mit den folgenden Funktionen verwendet werden:


```python
dim1 = FreeCAD.ActiveDocument.addObject('TechDraw::DrawViewDimension','Dimension')
dim1.Type = "DistanceX"
dim1.References2D=[(view1, 'Edge1')]
rc = page.addView(dim1)
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw HorizontalDimension/de
