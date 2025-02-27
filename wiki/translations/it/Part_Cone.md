# Part Cone/it
---
- GuiCommand:/it   Name:Part Cone   Name/it:Cono   MenuLocation:Parte → Primitive → Cono   Workbenches:[SeeAlso:[[Part_CreatePrimitives/it|Crea primitive](Part_Workbench/it___Parte]].md)---


</div>

## Descrizione


<div class="mw-translate-fuzzy">

Crea un tronco di cono parametrico.


</div>

The default Part Cone is truncated. It can be turned into a full, untruncated, cone by changing its **Radius1** or **Radius2** property to zero. It can be turned into a segment of a cone by changing its **Angle** property.

<img alt="" src=images/Part_Cone_Example.png  style="width:400px;">

## Utilizzo


<div class="mw-translate-fuzzy">

1.  Attivare l\'ambiente **<img src="images/Workbench_Part.svg" width=16px> [Parte](Part_Workbench/it.md)**.
2.  Richiamare il comando Cono in uno di questi modi:
    -   Premere il pulsante <img alt="" src=images/Part_Cone.svg  style="width:24px;"> [Cono](Part_Cone/it.md)
    -   Usare **Part → Primitive → Cono** dal menu principale.


</div>

## Example

![Part Cone from the scripting example](images/Part_Cone_Scripting_Example.png )

A Part Cone object created with the [scripting example](#Scripting.md) below is shown here.

## Notes

-   A Part Cone can also be created with the <img alt="" src=images/Part_Primitives.svg  style="width:16px;"> [Part Primitives](Part_Primitives.md) command. With that command you can specify the dimensions and placement at creation time.


<div class="mw-translate-fuzzy">

## Opzioni

+++
| ![](images/PartConeProperty_en.png ) |                                                                                                                                                                                         |
|                                                        | **Cone**                                                                                                                                                                                           |
|                                                        |                                                                                                                                                                                                     |
|                                                        | -   **Radius 1:** raggio dell\'arco o del cerchio che definisce la faccia inferiore                                                                                                                    |
|                                                        | -   **Radius 2:** raggio dell\'arco o del cerchio che definisce la faccia superiore                                                                                                                    |
|                                                        | -   **Height:** l\'altezza del cono                                                                                                                                                                    |
|                                                        | -   **Angle:** il numero di gradi dell\'arco che definisce le facce superiore e inferiore del cono. Il valore 360° predefinito crea facce circolari, un valore inferiore crea una porzione di un cono. |
+++


</div>

See also: [Property editor](Property_editor.md).

A Part Cone object is derived from a [Part Feature](Part_Feature.md) object and inherits all its properties. It also has the following additional properties:

### Data


{{TitleProperty|Attachment}}

The object has the same attachment properties as a [Part Part2DObject](Part_Part2DObject#Data.md).


{{TitleProperty|Cone}}

-    **Radius1|Length**: The radius of the bottom face of the cone. Can be {{Value|0mm}} if **Radius2** is larger than {{Value|0mm}}. The default is {{Value|2mm}}.

-    **Radius2|Length**: The radius of the top face of the cone. Can be {{Value|0mm}} if **Radius1** is larger than {{Value|0mm}}. The default is {{Value|4mm}}.

-    **Height|Length**: The height of the cone. The default is {{Value|10mm}}.

-    **Angle|Angle**: The angle of the circular arc that defines the top and bottom face of the cone. Valid range: {{Value|0° &lt; value &lt;&#61; 360°}}. The default is {{Value|360°}}. If it is smaller than {{Value|360°}} the resulting solid will be a segment of a cone.

## Scripting

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/), [Part scripting](Part_scripting.md) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

A Part Cone can be created with the {{Incode|addObject()}} method of the document:


```python
cone = FreeCAD.ActiveDocument.addObject("Part::Cone", "myCone")
```

-   Where {{Incode|"myCone"}} is the name for the object.
-   The function returns the newly created object.

Example:


```python
import FreeCAD as App

doc = App.activeDocument()

cone = doc.addObject("Part::Cone", "myCone")
cone.Radius1 = 5
cone.Radius2 = 10
cone.Height = 50
cone.Angle = 270
cone.Placement = App.Placement(App.Vector(1, 2, 3), App.Rotation(30, 60, 15))

doc.recompute()
```


<div class="mw-translate-fuzzy">





</div>


{{Part_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Cone/it
