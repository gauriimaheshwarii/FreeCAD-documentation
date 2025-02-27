---
- GuiCommand:
   Name:TechDraw MoveView
   MenuLocation:TechDraw → Move View
   Workbenches:[TechDraw](TechDraw_Workbench.md)
   Version:0.20
   SeeAlso:[TechDraw ShareView](TechDraw_ShareView.md)
---

# TechDraw MoveView/pl

## Description

The <img alt="" src=images/TechDraw_MoveView.svg  style="width:24px;"> **TechDraw MoveView** tool moves a View and all its dependents (Balloons, Dimensions, etc) to a different Page.

## Usage

1.  Optionally select a View, a from Page and a to Page. The pages must be selected in that order.
2.  There are several ways to invoke the tool:
    -   Press the **<img src="images/TechDraw_MoveView.svg" width=16px> [Move View](TechDraw_MoveView.md)** button.
    -   Select the **TechDraw → <img src="images/TechDraw_MoveView.svg" width=16px> Move View** option from the menu.
3.  A dialog will open to allow you to select a View, from Page and to Page.
4.  Press the **OK** button.

## Scripting

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

The MoveView tool can be used in [macros](Macros.md) and from the [Python](Python.md) console by using the following functions:


```python
import TechDrawTools
TechDrawTools.MoveView(viewName, fromPageName, toPageName)
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw MoveView/pl
