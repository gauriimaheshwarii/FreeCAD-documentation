# Property editor/es
{{TOCright}}



## Introducción

El [Editor de propiedades](property_editor/es.md) es una de las herramientas más importantes de FreeCAD y un elemento principal al trabajar con FreeCAD. El Editor de propiedades permite administrar las propiedades de los objetos en su documento.

Im Allgemeinen ist der Eigenschaftseditor dafür vorgesehen, jeweils nur ein Objekt zu behandeln. Die im Eigenschaftseditor angezeigten Werte gehören zu dem ausgewählten Objekt des aktiven Dokuments. Trotzdem können einige Eigenschaften, wie z. B. Farben, für mehrere ausgewählte Objekte eingestellt werden. Wenn keine Elemente ausgewählt sind, ist der Eigenschaftseditor leer.

Not all properties can be modified always; depending on the specific status of the property, some of them will be invisible (not listed), or be read-only (not editable).


{{TOCright}}

![](images/FreeCAD_Property_editor_empty.png )



*Empty property editor, when no object is selected.*




<div class="mw-translate-fuzzy">

## Definición de propiedad 

A **property** is a piece of information like a number or a text string that is attached to a FreeCAD document or an object in a document. Properties can be viewed and modified with the [Property editor](Property_editor.md).

Properties play a very important part in FreeCAD, since it has been designed to work with parametric objects, which are objects defined only by their properties.

Custom [scripted objects](scripted_objects.md) in FreeCAD can have properties of the following types:


```python
 Boolean
 Float
 FloatList
 FloatConstraint
 Angle
 Distance
 Integer
 IntegerConstraint
 Percent
 Enumeration
 IntegerList
 String
 StringList
 Link
 LinkList
 Matrix
 Vector
 VectorList
 Placement
 PlacementLink
 Color
 ColorList
 Material
 Path
 File
 FileIncluded
 PartShape
 FilletContour
 Circle
```

## Ejemplo de propiedades 

There are two types of feature properties accessible through tabs at the bottom of the property editor:

:   
    **View**: properties related to the \"visual\" display of an object.

:   
    **Data**: properties related to the \"physical\" parameters of an object.

### View

<img alt="" src=images/FreeCAD_Properties_View.png  style="width:490px;"> {{TitleProperty|Base}}

-    **Bounding Box**: Indicates if a box showing the overall extent of the object is to be displayed. Value False, or True (Default, False).

-    **Control Point**: Indicates if the feature control points are to be displayed. Value False, or True (Default, False).

-    **Deviation**: Sets the accuracy of the polygonal representation of the model in the 3d view (tessellation). Lower values = better quality. The value is in percent of object\'s size (deviation in mm = (w+h+d)/3\*valueInPercent/100, where w,h,d are the bounding box dimensions).

-    **Display Mode**:Display mode of the feature, **Flat lines, Shaded, Wireframe, Points** [96px](IMAGE:Vue_DisplayModePartDesign_fr_00.png.md). (Default, **Flat lines**).

-    **Lighting**: Lighting **One side, Two side** [96px](IMAGE:Vue_Lighting_fr_00.png.md). (Default, **Two side**).

-    **Line Color**: Gives the color of the line (edges) (Default, **25, 25, 25**).

-    **Line Width**: Gives the thickness of the line (edges) (Default, **2**).

-    **Point Color**: Gives the color of the points (ends of the feature) (Default, **25, 25, 25**).

-    **Point Size**: Gives the size of the points (Default, **2**).

-    **Selectable**: Allows selection of the feature. Value False, ou True (Default, True).

-    **Shape Color**: Give the color shape (default, **204, 204, 204**).

-    **Transparency**: Sets the degree of transparency in the feature of **0** to **100** (Default, **0**).

-    **Visibility**: Determines the visibility of the feature (like the bar **SPACE**). Value False, or True (Default, True).




### Data

<img alt="" src=images/FreeCAD_Properties_Data.png  style="width:490px;"> {{TitleProperty|Base}}


**Placement**

: Summary of the data below. Every feature has a placement that can be controlled through the Data Properties table. It controls the placement of the part with respect to the coordinate system. NOTE: The placement properties do not affect the physical dimensions of the feature, but merely its position in space!
If you select the title **Placement** <img alt="Options Placement" src=images/Tache_Placement_01_fr_00.png  style="width:256px;">, a button with **three small points** appears to the right. Clicking this button ** '''...'''**, opens the **[Tasks_Placement](Tasks_Placement.md)** options window.


**Angle**

: Specifies the angle to be used with the [axis](#Axis.md) property (below). An angle is set here, and the axis that the angle acts upon is set with the axis property. The feature is rotated by the specified angle, about the specified axis. A usage example might be if you created a revolution feature as required, but then needed to rotate the whole feature by some amount, in order to allow it to line-up with another pre-existing feature.


**Axis**

: This property specifies the axis/axes about which the feature is to be rotated. The exact value of rotation comes from the angle property (above). This property takes three arguments, which are passed as numbers in the x, y, and z boxes in the tool. Setting a value for more than one of the axes will cause the part to be rotated in each axis, by the angle value multiplied by the value for the axis. For example, with an angle of 15° set, specifying a value of 1.0 for x, and 2.0 for y will cause the finished part to be rotated 15° in the x-axis AND 30° in the y-axis.


**Position**

: This property specifies the base point to which all dimensions refer. This takes three arguments, which are passed as numbers to the x, y, and z boxes in the tool. Setting a value for more than one of the boxes will cause the part to be translated by the number of units along the corresponding axis.


**Label**

: The Label is the name given to the object (feature), this name can be changed as desired.




**PS: The displayed properties can vary, depending on the tool used.**


</div>

A property is a piece of information like a number or a text string that is attached to a FreeCAD document or an object in the document.

Custom [scripted objects](Scripted_objects.md) can use any of the property types defined in the base system. See the full list in [Property](Property.md).

Some of the most commonly used property types are:


```python
App::PropertyBool
App::PropertyFloat
App::PropertyAngle
App::PropertyDistance
App::PropertyInteger
App::PropertyString
App::PropertyMatrix
App::PropertyVector
App::PropertyPlacement
```

Different objects may have different types of properties. However, many objects have the same types because they are derived from the same internal class. For example, most objects that describe geometrical shapes (lines, circles, rectangles, solid bodies, imported parts, etc.), have the \"Placement\" property that defines their position in the [3D view](3D_view.md).

## View and Data properties 

There are two classes of feature properties accessible through tabs in the property editor:

-    **View**properties, related to the \"visual\" appearance of the object. The **View** properties are tied to the **ViewProvider** (`ViewObject` attribute) of the object, and are only accessible when the graphical user interface (GUI) is loaded. They are not accessible when using FreeCAD in console mode, or as a headless library.

-    **Data**properties, related to the \"physical\" parameters of the object. The **Data** properties define the essential characteristics of the object; they exist at all times, even when FreeCAD is used in console mode, or as a library. This means that if you load a document in console mode, you can edit the radius of a circle or the length of a line, even if you cannot see the result on the screen.

For this reason, **Data** properties are considered to be more \"real\", as they truly define the geometry of a shape. On the other hand, **View** properties are less important because they only affect the superficial appearance of the geometry. For example, a circle of 10 mm radius is different from a circle of 5 mm radius; the color of the circle (view property) doesn\'t affect its shape, but the radius does (data property). In many instances in this documentation, the word \"property\" is understood to refer to a \"Data property\" and not to a \"View property\".

### Basic properties 


**See also: [Object name](Object_name.md)**

The most basic [scripted object](Scripted_objects.md) won\'t show any **Data** property in the property editor, except for its `Label` attribute. The `Label` is a user editable string that identifies the object in the [tree view](Tree_view.md). On the other hand, the `Name` attribute of an object is assigned at the moment of its creation and cannot be changed; this attribute is read-only, and is not displayed in the property editor either.

A basic parametric object is created as follow


```python
obj = App.ActiveDocument.addObject("App::FeaturePython", "App__FeaturePython")
obj.Label = "Plain_object"
print(obj.Name)
print(obj.Label)
```

<img alt="" src=images/FreeCAD_Property_editor_View_basic.png  style="width:" height="264px;"> <img alt="" src=images/FreeCAD_Property_editor_Data_basic.png  style="width:" height="264px;">



*View and Data tabs of the property editor, for a basic "App::FeaturePython" scripted object.*

Most geometrical objects that can be created and displayed in the [3D view](3D_view.md) are derived from a `Part::Feature`. See [Part Feature](Part_Feature.md) for the most basic properties that these objects have.

For 2D geometry, most objects are derived from `Part::Part2DObject` (itself derived from `Part::Feature`) which is the base of [Sketches](Sketch.md), and most [Draft elements](Draft_Workbench.md). See [Part Part2DObject](Part_Part2DObject.md) for the most basic properties that these objects have.

## Actions


<small>(v0.19)</small> 

Right clicking in an empty space of the view, or with a property selected, shows only one command:

-    **Show all**: if active, in addition to the standard properties that appear already, it shows all the hidden Data and View properties in their respective tabs.

    -   Data: \"Proxy\", \"Label2\", \"Expression Engine\", and \"Visibility\".
    -   View: \"Proxy\".

When the **Show all** option is active, and one property is selected, more actions are available with a second right click:

-    **Show all**: deactivates the **Show all** command, hiding the additional Data and View properties.

-    **Add Property**: adds a dynamic property to the object; this works with both C++ defined objects, and Python [scripted objects](Scripted_objects.md).

-    **Expression...**: brings up the formula editor, which allows using [expressions](Expressions.md) in the property value.

-    **Hidden**: if active, sets the property as hidden, meaning that it will only be displayed in the property editor if **Show all** is active.

-    **Output**: if active, sets the property as output.

-    **NoRecompute**: if active, sets the property as not recomputed when the document is recomputed; this is useful when a property should be kept unaffected by other updates.

-    **ReadOnly**: if active, sets the property to be read-only; it won\'t be editable in the property editor any more until this switch is turned off. The **Expression...** menu entry is no longer available. **Note:** It may be still possible to change the property via a dialog that updates the property.

-    **Transient**: if active, sets the property as transient. The value of a transient property is not saved to file. When opening a file, it is instantiated with its default value.

-    **Touched**: if active, it becomes touched, and ready for recompute.

-    **EvalOnRestore**: if active, it is evaluated when the document is restored.

## Example of the properties of a PartDesign object 

In this section we show some common properties that are visible for a [PartDesign Body](PartDesign_Body.md), and one [PartDesign Feature](PartDesign_Feature.md). The specific properties of an object can found in the specific documentation page of that object.

### View 

Most of these properties are inherited from the [Part Feature](Part_Feature.md) basic object.


<div class="mw-translate-fuzzy">

<img alt="" src=images/FreeCAD_Properties_View.png  style="width:490px;"> {{TitleProperty|Base}}


</div>


{{TitleProperty|Base}}

-    **Angular Deflection**: it is another way to specify how finely to generate the mesh for rendering on screen or when exporting. The default value is 28.5 degrees, or 0.5 radians. The smaller the value the smoother the appearance will be in the [3D view](3D_view.md), and the finer the mesh that will be exported.

-    **Bounding Box**: indicates if a box showing the overall extent of the object is displayed.

-    **Deviation**: sets the accuracy of the polygonal representation of the model in the [3D view](3D_view.md) (tessellation). Lower values indicate better quality. The value is in percent of object\'s size.

-    **Display Mode**: display mode of the entire Body, {{Value|Flat lines}} (default), {{Value|Shaded}}, {{Value|Wireframe}}, {{Value|Points}}.

-    **Display Mode Body**: display mode of the Tip of the Body, {{Value|Through}} (default), {{Value|Tip}}.

-    **Draw Style**: {{Value|Solid}}, {{Value|Dashed}}, {{Value|Dotted}}, {{Value|Dashdot}}; defines the style of the edges in the [3D view](3D_view.md).

-    **Lighting**: {{Value|One side}}, {{Value|Two side}} (default).

-    **Line Color**: the RGB color of the edges, it defaults to {{value|(25, 25, 25)}}.

-    **Line Width**: the thickness of the edges, it defaults to {{value|2}} pixels.

-    **On Top When Selected**: {{value|Disabled}}, {{value|Enabled}}, {{value|Object}}, {{value|Element}}.

-    **Point Color**: the RGB color of the vertices, it defaults to {{value|(25, 25, 25)}}.

-    **Point Size**: the size of the vertices, it defaults to {{value|2}} pixels.

-    **Selectable**: whether the object is selectable or not.

-    **Selection Style**: {{value|Shape}}, {{value|BoundBox}}.

-    **Shape Color**: the RGB color of the shape, it defaults to {{value|(204, 204, 204)}}.

-    **Show In Tree**: if it is `True`, the object appears in the tree view. Otherwise, it is set as invisible.

-    **Transparency**: the degree of transparency from {{value|0}} (default) to {{value|100}}.

-    **Visibility**: whether the object is visible in the [3D view](3D_view.md) or not. Toggle with the **Space** bar in the keyboard.




### Data 

In this case we observe the properties of the [PartDesign Revolution](PartDesign_Revolution.md) feature.


<div class="mw-translate-fuzzy">

<img alt="" src=images/FreeCAD_Properties_Data.png  style="width:490px;"> {{TitleProperty|Base}}


</div>


{{TitleProperty|Base}}

-    **Label**: the user defined name given to the object, this can be changed as desired.


{{TitleProperty|Part Design}}

-    **Refine**: whether to refine the fusion done with other objects.


{{TitleProperty|Revolution}}

-    **Base**: the point in space that specifies where the revolution takes place. It cannot be modified directly, only when editing the feature.

-    **Axis**: the axis around which the revolution will be performed. It cannot be modified directly, only when editing the feature.

-    **Angle**: the angle that specifies how much of the base element is rotated. By default it is {{value|360 deg}}, but it can be any fraction of that.


{{TitleProperty|Sketch Based}}

-    **Midplane**: if the base object is a [Sketch](Sketch.md), when this property is `True`, it will perform the revolution with the sketch serving as a plane of symmetry. This is noticeable if the **Angle** is different from {{value|360 deg}}.

-    **Reversed**: by default it is `True`. Whether to perform the revolution in one direction or the other.




## Scripting


**See also:**

[FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

See [scripted objects](scripted_objects.md) for the full information on adding properties to objects defined through [Python](Python.md).

Most properties that are visible in the property editor can be accessed from the [Python console](Python_console.md). These properties are just attributes of the class that defines the selected object. For example, if the property editor shows the **Group** property, this means that the object has the `Group` attribute.


```python
print(obj.Group)
```

These attributes (properties) are added with the `addProperty` method of the base object. At least it is necessary to specify the type of [property](property.md), and its name.


```python
obj.addProperty("App::PropertyFloat", "Custom")
print(obj.Custom)
```

Properties follow the `CapitalCamelCase` or `PascalCase` convention, meaning that each word starts with a capital letter, and there are no underscores. When the property editor displays such names, it leaves a space between each capital letter, making it easier to read.


```python
obj.addProperty("App::PropertyDistance", "CustomCamelProperty")
obj.CustomCamelProperty = 1000
print(obj.CustomCamelProperty)
```

![](images/FreeCAD_Property_editor_Custom.png ) 
*Property editor showing the Data properties of a [PartDesign Body](PartDesign_Body.md), with two additional properties, "Custom" and "Custom Camel Property".*

In similar way the **View** properties are added, not to the base object, but to its `ViewObject`. Then, it follows that properties like **Angular Deflection**, **Bounding Box**, **Display Mode**, **Display Mode Body**, **Line Color**, and others, can be examined and changed from the [Python console](Python_console.md).


```python
print(obj.ViewObject.AngularDeflection)
print(obj.ViewObject.BoundingBox)
print(obj.ViewObject.DisplayMode)
print(obj.ViewObject.DisplayModeBody)
print(obj.ViewObject.LineColor)
```

All public properties of the object, and of its view provider, are contained in the corresponding `PropertiesList` attribute.


```python
print(obj.PropertiesList)
print(obj.ViewObject.PropertiesList)
```


<div class="mw-translate-fuzzy">





</div>


{{Interface navi

}} {{Std Base navi}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Property editor/es
