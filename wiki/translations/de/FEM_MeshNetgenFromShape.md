---
- GuiCommand:/de
   Name:FEM MeshNetgenFromShape
   Name/de:FEM NetzNetgenAusForm
   MenuLocation:FEM → FEM Netz aus Form durch Netgen
   Workbenches:[FEM](FEM_Workbench/de.md)
   Shortcut:
   SeeAlso:[FEM Tutorium](FEM_tutorial/de.md)
---

# FEM MeshNetgenFromShape/de


</div>

## Beschreibung

For a finite element analysis the geometry needs to be discretized into a [FEM Mesh](FEM_Mesh.md). This command uses Netgen (which needs to be installed on the system) for calculating the mesh.

Depending on your operating system and your installation package Netgen might be bundled with FreeCAD or not. For further information see [FEM Install](FEM_Install.md).

## Anwendung

1.  Select the shape you want to analyze. For volume FEM this needs to be a solid or compsolid. A compsolid is necessary if your part is made from multiple materials. (A compsolid can be created with the [BooleanFragments](Part_BooleanFragments.md) command.)
    -   Press the **<img src="images/FEM_MeshNetgenFromShape.svg" width=16px> [FEM MeshNetgenFromShape](FEM_MeshNetgenFromShape.md)** button, or
    -   select the **Mesh → <img src="images/FEM_MeshGmshFromShape.svg" width=16px> FEM mesh from shape by Netgen** option from the menu.
2.  Optionally, edit the parameters.
3.  Click the **Apply** button to make a mesh, or **OK** button to make a mesh and close the dialogue.

## Properties

-    **Max. Size**: Maximum size of the element in mm.

-    **Second order**: Second order elements contain more nodes per element. Usually, it is enough to use rougher mesh to obtain same solution precision as with the first order elements,

    -   true (default); second order elements,
    -   false; first order elements.

-    **Fineness**: Defines how fine the mesh should be.

-    **Growth Rate**: Defines how much adjacent elements can differ in size.

-    **Nb. Segs per Edge**: Defines the minimum number of mesh segments per edge.

-    **Nb. Segs per Radius**: Defines the minimum number of mesh segments per radius.

-    **Optimize**:

    -   true (default); applies optimization algorithm to improve mesh quality,
    -   false;


<div class="mw-translate-fuzzy">





</div>


{{FEM Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM MeshNetgenFromShape/de
