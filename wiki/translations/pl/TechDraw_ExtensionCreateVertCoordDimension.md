---
- GuiCommand:
   Name:TechDraw ExtensionCreateVertCoordDimension
   MenuLocation:TechDraw → Extensions: Dimensions → Create Vertical Coordinate Dimensions
   Workbenches:[TechDraw](TechDraw_Workbench.md)
   Shortcut:
   Version:0.20
   SeeAlso:[TechDraw ExtensionCreateHorizCoordDimension](TechDraw_ExtensionCreateHorizCoordDimension.md), [TechDraw ExtensionCreateObliqueCoordDimension](TechDraw_ExtensionCreateObliqueCoordDimension.md)
---

# TechDraw ExtensionCreateVertCoordDimension/pl

## Description

The <img alt="" src=images/TechDraw_ExtensionCreateVertCoordDimension.svg  style="width:24px;"> **TechDraw ExtensionCreateVertCoordDimension** tool creates vertical coordinate dimensions: multiple evenly spaced dimensions starting from the same baseline.

<img alt="" src=images/TechDraw_ExtensionCreateVertCoordDimensionExample.png  style="width:400px;"> 
*On the right the created dimensions*

## Usage

1.  Optionally specify the cascade spacing with the <img alt="" src=images/TechDraw_ExtensionSelectLineAttributes.svg  style="width:16px;"> [TechDraw ExtensionSelectLineAttributes](TechDraw_ExtensionSelectLineAttributes.md) tool.
2.  Select three or more vertexes.
3.  The selection order of the first two vertexes determines the position of the baseline. If the vertex that is selected first is below the second, the baseline is created at the lowest vertex, else it is created at the highest vertex.
4.  There are several ways to invoke the tool:
    -   Press the **<img src="images/TechDraw_ExtensionCreateVertCoordDimension.svg" width=16px> [TechDraw ExtensionCreateVertCoordDimension](TechDraw_ExtensionCreateVertCoordDimension.md)** button.
    -   Select the **TechDraw → Extensions: Dimensions → <img src="images/TechDraw_ExtensionCreateVertCoordDimension.svg" width=16px> Create Vertical Coordinate Dimensions** option from the menu.
5.  Coordinate dimensions with centered dimension texts are created.





{{TechDraw_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw ExtensionCreateVertCoordDimension/pl
