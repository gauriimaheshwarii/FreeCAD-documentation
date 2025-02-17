---
- GuiCommand:/ru
   Name/ru:Добавить вспомогательную линию между 2-мя точками
   Name:TechDraw_2PointCosmeticLine
   MenuLocation:TechDraw → Добавить Линии → Добавить вспомогательную линию между 2-мя точками
   Workbenches:[TechDraw](TechDraw_Workbench/ru.md)
   Version:0.19
   SeeAlso:[Добавить осевую линию к граням](TechDraw_FaceCenterLine/ru.md), [Добавить осевую линию между 2 линиями](TechDraw_2LineCenterLine/ru.md)
---

# TechDraw 2PointCosmeticLine/ru

## Описание

The **2PointCosmeticLine** tool adds a cosmetic line between two Vertices (Points). The vertices can be 2d or 3d. The resulting line can be used for dimensioning. The line\'s appearance can be modified using the [Change Appearance of Line(s)](TechDraw_DecorateLine.md) tool.

<img alt="" src=images/CosLine2PointsSample.png  style="width:200px;">



*Cosmetic line between 2 Points*

## Применение

1.  Select 2 Vertexes in a View or 2 Vertexes in the 3D view.
2.  Press the **<img src="images/TechDraw-line2points.svg" width=16px> Add Cosmetic line between 2 Points** button.
3.  A dialog will open where you can adjust the coordinates of the 2 points.
4.  A line will be added to connect the 2 selected Vertices. In the case of 3d points, the line will connect the projection of the selected points.

## Editing Cosmetic Lines 

To change the endpoints of a cosmetic line:

1.  Select the cosmetic line.
2.  Press **<img src="images/TechDraw-line2points.svg" width=16px> Add Cosmetic line between 2 Points**.
3.  A dialog will open where you can change the coordinates of the endpoints.
4.  Press **OK** to see your changes.

To delete a cosmetic line use <img alt="" src=images/TechDraw_CosmeticEraser.svg  style="width:16px;"> [Remove Cosmetic Object](TechDraw_CosmeticEraser.md).

To change the appearance of a cosmetic line use <img alt="" src=images/TechDraw_DecorateLine.svg  style="width:16px;"> [Change Appearance of Line(s)](TechDraw_DecorateLine.md).

## Свойства

Cosmetic lines have no properties of their own, as they are not document objects.

## Программирование


**См. так же:**

[TechDraw API](TechDraw_API/ru.md) и [Основы составления скриптов FreeCAD](FreeCAD_Scripting_Basics/ru.md).

Cosmetic lines can be created using the makeCosmeticLine(v1, v2) or makeCosmeticLine3d(v1, v2) methods of DrawViewPart.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw 2PointCosmeticLine/ru
