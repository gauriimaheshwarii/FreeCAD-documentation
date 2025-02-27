# Part Ellipse/cs
---
- GuiCommand:/cs   Name:Part Ellipse   Name/cs:Díl Elipsa   MenuLocation:Díl → [Workbenches:[[Part_Workbench/cs   Díl](Part_CreatePrimitives/cs___Vytváření_zákl.geom.tvarů]] → Elipsa.md),  [OpenSCAD](OpenSCAD_Workbench/cs.md)|SeeAlso:..---


</div>


<div class="mw-translate-fuzzy">

### Základní geometrické tvary 

+++
| ![](images/PartEllipsePrimitivesOptions_it.png ) | Elipsa                          |
|                                                                                |                                 |
|                                                                                | #### Parametr                   |
|                                                                                |                                 |
|                                                                                | -                |
|                                                                                |     {{Parameter|Velký poloměr}} |
|                                                                                |                              |
|                                                                                |                                 |
|                                                                                | -                |
|                                                                                |     {{Parameter|Malý poloměr}}  |
|                                                                                |                              |
|                                                                                |                                 |
|                                                                                | -                |
|                                                                                |     {{Parameter|Úhel 1}}        |
|                                                                                |                              |
|                                                                                |                                 |
|                                                                                | -                |
|                                                                                |     {{Parameter|Úhel 2}}        |
|                                                                                |                              |
|                                                                                |                                 |
|                                                                                | #### Umístění                   |
|                                                                                |                                 |
|                                                                                | -                               |
|                                                                                | -                               |
+++


</div>

A <img alt="" src=images/Part_Ellipse.svg  style="width:24px;"> **Part Ellipse** is a parametric shape that can be created with the <img alt="" src=images/Part_Primitives.svg  style="width:24px;"> [Part Primitives](Part_Primitives.md) command. In the coordinate system defined by its **Placement** property, the ellipse lies on the XY plane with its center at the origin. Its mayor axis is parallel to the X axis.

A Part Ellipse is in fact a closed counterclockwise elliptical arc, it can be turned into an arc by changing its **Angle1** and/or **Angle2** properties.

<img alt="" src=images/Part_Ellipse_Example.png  style="width:400px;">

## Usage

See [Part Primitives](Part_Primitives#Usage.md).

## Example

![Part Ellipse from the scripting example](images/Part_Ellipse_Scripting_Example.png )

A Part Ellipse object created with the [scripting example](#Scripting.md) below is shown here.

## Properties

See also: [Property editor](Property_editor.md).

A Part Ellipse object is derived from a [Part Feature](Part_Feature.md) object and inherits all its properties. It also has the following additional properties:

### Data


{{TitleProperty|Attachment}}

The object has the same attachment properties as a [Part Part2DObject](Part_Part2DObject#Data.md).


{{TitleProperty|Base}}

-    **MajorRadius|Length**: The major radius of the ellipse or elliptical arc. The default is {{Value|4mm}}.

-    **MinorRadius|Length**: The minor radius of the ellipse or elliptical arc. The default is {{Value|2mm}}.

-    **Angle1|Angle**: The start angle of the elliptical arc. Valid range: {{Value|0° &lt; value &lt;&#61; 360°}}. The default is {{Value|0°}}.

-    **Angle2|Angle**: The end angle of the elliptical arc. Valid range: {{Value|0° &lt; value &lt;&#61; 360°}}. The default is {{Value|360°}}. If **Angle1** and **Angle2** are equal, or if one angle is {{Value|0°}} and the other {{Value|360°}}, a full ellipse is created.

## Scripting

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/), [Part scripting](Part_scripting.md) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

A Part Ellipse can be created with the {{Incode|addObject()}} method of the document:


```python
ellipse = FreeCAD.ActiveDocument.addObject("Part::Ellipse", "myEllipse")
```

-   Where {{Incode|"myEllipse"}} is the name for the object.
-   The function returns the newly created object.

Example:


```python
import FreeCAD as App

doc = App.activeDocument()

ellipse = doc.addObject("Part::Ellipse", "myEllipse")
ellipse.MajorRadius = 20
ellipse.MinorRadius = 10
ellipse.Angle1 = 45
ellipse.Angle2 = 135
ellipse.Placement = App.Placement(App.Vector(1, 2, 3), App.Rotation(30, 45, 10))

doc.recompute()
```





{{Part_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Ellipse/cs
