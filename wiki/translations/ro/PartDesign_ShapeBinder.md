---
- GuiCommand:/ro
   Name:PartDesign ShapeBinder
   Name/ro:PartDesign Forme Legate
   Workbenches:[PartDesign](PartDesign_Workbench/ro.md)
   MenuLocation:Part Design → Create a shape binder
   Version:0.17
   SeeAlso:[[PartDesign Clone/ro]]
---

# PartDesign ShapeBinder/ro


</div>

## Descriere


<div class="mw-translate-fuzzy">

Creează o formă de referință legată **shape binder** dintr-un corp selectat din corpul activ. Forma legată este un obiect de referință care leagă marginile sau fețele unui alt Corp. Un exemplu de utilizare ar fi construirea unei casete cu capac de montaj din două corpuri diferite. Obiectul de formă legat este afișat în galben translucid în vizualizarea 3D.


</div>

A ShapeBinder will track the relative placement of the referenced geometry, which is useful in the context of creating [assemblies](Assembly.md), if its **Trace Support** property is set to {{True}}. See the [Example](#Example.md) below to understand how this works.

The referenced geometry can either be a single object (for example a [Part Box](Part_Box.md), a [PartDesign Body](PartDesign_Body.md), or a [sketch](PartDesign_NewSketch.md) or [Feature](PartDesign_Feature.md) inside a Body), or one or more subelements (faces, edges or vertices) belonging to the same parent object. Which geometry should be selected depends on the intended purpose of the ShapeBinder. For a Boolean operation you would need to select a solid. For a Pad operation a face or a sketch can be used. And for the external geometry in a sketch, or to attach a sketch, any combination of subelements may be appropriate. The referenced geometry can also belong to the Body the ShapeBinder is nested in.

<img alt="" src=images/Shapebinder_flow.png  style="width:600px;">


<div class="mw-translate-fuzzy">

*Two shapes from Body.Pad004 are selected and their datum objects are now available in Body001.Sketch005 as external geometry through Body001.ShapeBinder.*


</div>


<div class="mw-translate-fuzzy">

## Cum se folosește 


</div>


<div class="mw-translate-fuzzy">

1.  Activate target body (body to receive shape binder object).
2.  Press the **<img src="images/PartDesign_ShapeBinder.png" width=24px> '''Create a shape binder'''** button.
3.  Press either the **Object** button or the **Add geometry** button.
4.  In the 3D view, select the object or geometry to copy. *Object* will select the whole body; *Add geometry* will select any element (vertex, edge, face).
5.  To remove selected geometry, press the **Remove geometry** button and select the geometry in the 3D view. To cancel, press the button again.
6.  Alternatively, the Body to copy can be selected before launching the Shape binder command.
7.  Press **OK**.


</div>

## Opţiuni


<div class="mw-translate-fuzzy">

Double-click the ShapeBinder label in the Model tree or right-click and select **Edit shape binder** in the contextual menu to edit its parameters.


</div>

## Notes

-   A ShapeBinder can be dragged out of the Body it is nested in, and dropped onto the <img alt="" src=images/Document.svg  style="width:16px;"> document node in the [Tree view](Tree_view.md). Such an unnested ShapeBinder can be used as the [Base Feature](PartDesign_Body#Base_Feature.md) for a new Body.
-   A ShapeBinder created from a sketch can have an opposite \"tool direction\". For example a [Pad](PartDesign_Pad.md) created from the sketch may extend in the +Y direction, while a [Pad](PartDesign_Pad.md), with the same properties, created from the ShapeBinder extends in the -Y direction. Toggling the **Reversed** property (or checkbox) will solve this.

## PartDesign SubShapeBinder vs. PartDesign ShapeBinder 

See [PartDesign SubShapeBinder](PartDesign_SubShapeBinder#PartDesign_SubShapeBinder_vs._PartDesign_ShapeBinder.md).

## Proprietăți


<div class="mw-translate-fuzzy">

-    **Label**: numele dat obiectului, acest nume poate fi modificat dacă vă este comod.

-    **Trace Support**: La setarea acestei opțiuni la adevărat, Shapebinder respectă destinațiile de plasare relative ale părților și corpurilor. <small>(v0.18)</small> 


</div>

## Example

The example uses the ShapeBinder Feature to make a hole (with or without threads) through more than one body. Normally the Hole function of the Part Design workbench is limited to a single body. The example uses two cubes facing each other but misaligned in an arbitrary way. The holes are created with sketches containing a circle for every hole (the diameter is ignored by the hole function). When you copy the sketch to the other cube it will be at the same position in the local cube coordinate system. In the image this is shown by the white circle on the back cube. This is not what we want, because the hole at that position would not be aligned to the hole in the front cube.

![](images/ShapeBinderThroughHole.png ) 
*Example setup for showing how to make holes through different bodies. The white circle shows that copying sketches is not enough*

Here is how you use the ShapeBinder Feature to achieve it:

1.  Prepare a scene as per the above image. If you use the cubes from the [Part workbench](Part_Workbench.md), remember that you must put them into a Body container. Each one in a single body container. Otherwise the [PartDesign](PartDesign_Workbench.md) functions would not work. If you build them from sketches the system should create body containers by default.
2.  In the [Property editor](Property_editor.md) change the placement of the second cube so that it touches the first cube with a side displacement.
3.  Select the PartDesign workbench
4.  Create a sketch on the front face of the first cube and place a circle anywhere and close the sketch
5.  Select the sketch in the tree and press the **<img src="images/PartDesign_Hole.svg" width=16px> [PartDesign Hole](PartDesign_Hole.md)** button. Before make sure the first body is the [active body](PartDesign_Body#Active_status.md) (double-click).
6.  Select a hole of appropriate size. The image above had also counterbore selected. Close the [Hole](PartDesign_Hole.md) function.

    :   Now the image should look as above. When you hide the first cube (select and press space) you can see that the hole does not reach the second cube. It will not, even when you select **Through All**, or when you enter a really large distance in the [Hole](PartDesign_Hole.md) task panel. The hole is always limited to a single body.
    :   Here is where our ShapeBinder comes in.
7.  First select the back cube. This is the target where the ShapeBinder will be added. It must be [actived](PartDesign_Body#Active_status.md) before, so be sure it has been double-clicked.
8.  In the tree select the sketch we used for the hole. It\'s important to not activate the first body.
9.  Select the shapeBinder function.

    :   A task panel should open. In the line **Object** the name of our sketch should be visible. If you had selected the function without selecting the sketch, you could press **Object** and then select the sketch from the list. It\'s recommended to select it first in order to get the right one, especially if you have many sketches with automatically generated names Sketch001,.. **Add Geometry** is not useful for us, because we want to select the whole sketch. **Add Geometry** is used if only parts should be selected.
10. Press **OK** to close the task panel and check that a new item has been added to the tree of the second cube.

    :   When you toggle the visibility of the ShapeBinder it is shown yellow in the [3D view](3D_view.md). However it\'s on the wrong position, just as the white circle in the image above. That is because of the default setting for the Trace parameter.
11. In the PropertyView of the ShapeBinder in the Data tab set the **Trace Support** parameter to true. The default was false.

    :   With **Trace Support** true, the ShapeBinder in not affected by local transformations of the target body, e.g. our translations. The shape remains exactly where the original front object shape has been. Try moving the front object around and you can see that the ShapeBinder always follows to the new position.
12. Select the ShapeBinder in the tree and press press the **<img src="images/PartDesign_Hole.svg" width=16px> [PartDesign Hole](PartDesign_Hole.md)** button. If you enter the same values as for the initial hole you will notice that no hole is created in the second cube. This is because a ShapeBinder in some cases has an opposite \"tool direction\" compared to the referenced sketch. To solve this check the Reverse checkbox. Press **OK** to finish.
13. You now have linked holes in two different bodies. If you change the position of the circle in the sketch, both holes will adapt. You can even add new circles in the sketch to create additional linked holes.





{{PartDesign_Tools_ navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [PartDesign](PartDesign_Workbench.md) > PartDesign ShapeBinder/ro
