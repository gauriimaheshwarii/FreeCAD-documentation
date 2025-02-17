---
- GuiCommand:
   Name:FEM ClippingPlaneAdd
   MenuLocation:Utilities → Clipping plane on face
   Workbenches:[FEM](FEM_Workbench.md)
   SeeAlso:[FEM tutorial](FEM_tutorial.md)
---

# FEM ClippingPlaneAdd/en

## Description

Adds a clipping plane for the whole model view. All visible objects will be cut by it, no matter if these are geometric models, meshes or result pipelines.

The clipping plane is the same you get when using the feature [Toggle Clip Plane](Std_ToggleClipPlane.md) with the difference that the clipping plane is persistent. Therefore it shares the same functionality of providing only hollow cuts.

## Usage

To create a clipping plane, either use the toolbar button **<img src="images/FEM_ClippingPlaneAdd.svg" width=16px> '''Clipping plane on face'''** or the menu **Utilities → <img src="images/FEM_ClippingPlaneAdd.svg" width=16px> Clipping plane on face**. It is possible to have several clipping planes.

Despite the plane is persistent, it will not appear in the [document tree](Tree_view.md). The plane appears in the model view like this:

<img alt="" src=images/FEM_Clipping-Plane-Example.png  style="width:400px;">

To move the plane, click on the big white cuboid that is perpendicular to the plane and keep the mouse button pressed while the mouse is moved.

To rotate and tilt the plane, click on a line that connects the small cubes with the the big white cuboid and keep the mouse button pressed while the mouse is moved.

The 6 small cubes are handles to adjust the size. However, since the object is an infinite plane, the size does not matter.

To remove all clipping planes, use the feature [Remove all clipping planes](FEM_ClippingPlaneRemoveAll.md). Removing only a certain plane is not possible.





{{FEM Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM ClippingPlaneAdd/en
