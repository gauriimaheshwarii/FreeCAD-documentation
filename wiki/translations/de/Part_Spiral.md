---
- GuiCommand:/de
   Name:Part Spiral
   Name/de:Part Spirale
   MenuLocation:Formteil → [Grundkörper erstellen...](Part_Primitives/de.md) → Spirale
   Workbenches:[Part](Part_Workbench/de.md), [OpenSCAD](OpenSCAD_Workbench/de.md)
   Version:0.14
   SeeAlso:[Part Grundelemente](Part_Primitives/de.md)
---

# Part Spiral/de

## Beschreibung

Eine <img alt="" src=images/Part_Spiral.svg  style="width:24px;"> **Part Spirale** ist ein parametrischer Volumenkörper, der mit dem Befehl <img alt="" src=images/Part_Primitives.svg  style="width:24px;"> [Part Grundelemente](Part_Primitives/de.md) erstellt werden kann. Im Koordinatensystem durch ihre {{PropertyData/de|Placement}} festgelegt, liegt die Spirale auf der XY-Ebene mit ihrem Mittelpunkt im Ursprung und ihrem Startpunkt auf der X-Achse. Sie öffnet sich gegen den Uhrzeigersinn.

<img alt="" src=images/Part_Spiral_Example.png  style="width:400px;">

## Anwendung

Siehe [Part Grundelemente](Part_Primitives/de#Anwendung.md).

## Beispiel

![Part-Spirale aus dem Skriptbeispiel](images/Part_Spiral_Scripting_Example.png )

Ein Part-Spirale-Objekt, das mit dem [Skriptbeispiel](#Skripten.md) weiter unten erzeugt wurde wird hier dargestellt.

## Eigenschaften

Siehe auch: [Eigenschafteneditor](Property_editor/de.md).

Ein Part-Spirale-Objekt wird von einem [Part-Formelement](Part_Feature/de.md) abgeleitet und erbt alle seine Eigenschaften. Außerdem hat es die folgenden zusätzlichen Eigenschaften:

### Daten


{{TitleProperty|Attachment}}

The object has the same attachment properties as a [Part Part2DObject](Part_Part2DObject#Data.md).


{{TitleProperty|Spiral}}

-    **Growth|Length**: The distance between two consecutive turns of the spiral. The default is {{Value|1mm}}.

-    **Radius|Length**: The start radius of the spiral, the distance between its center and its start point. Can be {{Value|0mm}}. The default is {{Value|1mm}}.

-    **Rotations|QuantityConstraint**: The number of rotations, or turns, of the spiral. The default is {{Value|2}}.

-    **Segment Length|QuantityConstraint**: The number of turns per spiral subdivision. The default is {{Value|1}}, meaning each full turn of the spiral is a separate segment. Use {{Value|0}} to suppress subdivision.

## Skripten

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/), [Part scripting](Part_scripting.md) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

A Part Spiral can be created with the {{Incode|addObject()}} method of the document:


```python
spiral = FreeCAD.ActiveDocument.addObject("Part::Spiral", "mySpiral")
```

-   Where {{Incode|"mySpiral"}} is the name for the object.
-   The function returns the newly created object.

Beispiel:


```python
import FreeCAD as App

doc = App.activeDocument()

spiral = doc.addObject("Part::Spiral", "mySpiral")
spiral.Growth = 2
spiral.Radius = 3
spiral.Rotations = 4
spiral.Placement = App.Placement(App.Vector(1, 2, 3), App.Rotation(75, 60, 30))

doc.recompute()
```





{{Part_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Spiral/de
