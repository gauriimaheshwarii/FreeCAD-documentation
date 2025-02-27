---
- GuiCommand:
   Name:TechDraw ProjectionGroup
   MenuLocation:TechDraw → Insert Projection Group
   Workbenches:[TechDraw](TechDraw_Workbench.md)
   SeeAlso:[TechDraw View](TechDraw_View.md), [TechDraw Section View](TechDraw_SectionView.md)
---

# TechDraw ProjectionGroup/pl

## Description

The <img alt="" src=images/TechDraw_ProjectionGroup.svg  style="width:24px;"> [ProjectionGroup](TechDraw_ProjectionGroup.md) tool creates a [multiview projection](https://en.wikipedia.org/wiki/Multiview_projection) of one or more 3D objects. The isometric views of the 4 front corners can also be included.

If you only want to produce a single view, there is no advantage in using ProjectionGroup; you should then use [Insert View](TechDraw_View.md) instead. If you do not wish to use the traditional [first-](https://en.wikipedia.org/wiki/Multiview_orthographic_projection#First-angle_projection) / [third-angle projection](https://en.wikipedia.org/wiki/Multiview_orthographic_projection#Third-angle_projection), you should use multiple *Views* ([Insert View](TechDraw_View.md)) instead of *ProjectionGroup*.

<img alt="" src=images/TechDraw_ProjGroup_example.png  style="width:400px;"> 
*Three orthogonal views and one isometric view of a solid object*

## Usage

1.  Optionally rotate the [3D view](3D_view.md). The camera direction in the [3D view](3D_view.md) determines the initial value of the **Primary Direction** of the Projection Group (the **Direction** property of the central view).
2.  Select one or more objects in the [3D view](3D_view.md) or [Tree view](Tree_view.md).
3.  If there are multiple drawing pages in the document: optionally add the desired page to the selection by selecting it in the [Tree view](Tree_view.md). This is not optional for {{VersionMinus|0.19}}.
4.  There are several ways to invoke the tool:
    -   Press the **<img src="images/TechDraw_ProjectionGroup.svg" width=16px> [Insert Projection Group](TechDraw_ProjectionGroup.md)** button.
    -   Select the **TechDraw → <img src="images/TechDraw_ProjectionGroup.svg" width=16px> Insert Projection Group** option from the menu.
5.  If there are multiple drawing pages in the document and you have not yet selected a page, the **Page Chooser** dialog box opens: <small>(v0.20)</small> 
    1.  Select the desired page.
    2.  Press the **OK** button.
6.  The **Projection Group** task panel opens.
7.  Select which views should appear in the Projection Group, and the Projection Group\'s scale and other parameters.
8.  Press the **OK** button.
9.  Optionally move the Projection Group by dragging its central view.
10. Optionally move the Projection Group\'s other views relative to the central view by dragging them individually.

![](images/TaskProjGroup.png ) 
*Projection Group [task panel](Task_panel.md). The Primary Direction field indicates the current view direction.*

## Properties

### Data


{{TitleProperty|Base}}

-    **Source|LinkList**: Links to the drawable objects to be depicted.

-    **XSource|XLinkList**: Links to the drawable objects in an external file. <small>(v0.19)</small> 

-    **Anchor|Link**: The central view in the group. Normally the Front view.

-    **ProjectionType|Enumeration**: {{Value|First Angle}} or {{Value|Third Angle}}.

For the other properties in this group see [TechDraw View](TechDraw_View#Properties.md).


{{TitleProperty|Collection}}

-    **Views|LinkList**: Links to the views in this ProjectionGroup.


{{TitleProperty|Distribute}}

-    **Auto Distribute|Bool**: If `True`, space out individual views automatically. Use `False` to position manually.

-    **spacing X|Length**: Horizontal space between views when automatically positioned. Note that Scale and the size of other views in the group also influence the spacing.

-    **spacing Y|Length**: Vertical space between views when automatically positioned.

### View


{{TitleProperty|Base}}

See [TechDraw View](TechDraw_View#Properties.md).

## Notes

The ProjectionGroup as a whole inherits X, Y, ScaleType, Scale and Rotation from the basic View.

Individual Views within the group inherit all part view properties, but the ProjectionGroup object controls the scale of all its member Views.

The RotationVector property of individual Views within the group is deprecated as of v0.19. Use XDirection instead.

Note that the central box displays the current projection direction of the primary view. It cannot be used to change the direction.

## Scripting

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

The NewProjGroup tool can be used in [macros](Macros.md) and from the [Python](Python.md) console. A full script is available in the Source distribution in \"source-dir/src/Mod/TechDraw/TDTest/DProjGroupTest.py\".


```python
    #make a page
    print("making a page")
    page = FreeCAD.ActiveDocument.addObject('TechDraw::DrawPage','Page')
    FreeCAD.ActiveDocument.addObject('TechDraw::DrawSVGTemplate','Template')
    FreeCAD.ActiveDocument.Template.Template = templateFileSpec
    FreeCAD.ActiveDocument.Page.Template = FreeCAD.ActiveDocument.Template

    #make projection group
    group = FreeCAD.ActiveDocument.addObject('TechDraw::DrawProjGroup','ProjGroup')
    rc = page.addView(group)
    group.Source = [fusion]

    #add Front(Anchor) view
    frontView = group.addProjection("Front")               ##need an Anchor

    #update group
    group.Anchor.Direction = FreeCAD.Vector(0,0,1)
    group.Anchor.RotationVector = FreeCAD.Vector(1,0,0)

    #add more projections
    leftView = group.addProjection("Left")
    topView = group.addProjection("Top")
    rightView = group.addProjection("Right")
    rearView = group.addProjection("Rear")
    BottomView = group.addProjection("Bottom")

    #remove a view from projection group
    iv = group.removeProjection("Left")

```

Programming note: The Projection Group should always be added to the Page (ex. page.addView(group) before adding projections to the Group. This allows the Projection Group to use default parameter values derived from the parent page.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw ProjectionGroup/pl
