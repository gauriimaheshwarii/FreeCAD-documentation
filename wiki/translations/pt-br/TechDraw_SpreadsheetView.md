---
- GuiCommand:
   Name:TechDraw SpreadsheetView
   MenuLocation:TechDraw → Insert Spreadsheet View
   Workbenches:[TechDraw](TechDraw_Workbench.md), [Spreadsheet](Spreadsheet_Workbench.md)
---

# TechDraw SpreadsheetView/pt-br

## Description

This tool allows you to place a view of a selected [spreadsheet](Spreadsheet_Workbench.md) on a [Page](TechDraw_Workbench.md).

![](images/TechDraw_Spreadsheetview.png ) 
*Spreadsheet element inserted in the TechDraw drawing page*

## Usage

1.  Select a spreadsheet in the [Tree view](Tree_view.md).
2.  Press the **<img src="images/TechDraw_SpreadsheetView.svg" width=16px> [Insert Spreadsheet View](TechDraw_SpreadsheetView.md)** button.

## Properties

See also [TechDraw View](TechDraw_View#Properties.md).

### Data


{{TitleProperty|Spreadsheet}}

-    **Source|Link**: The spreadsheet to be added to the page.

-    **Cell Start|String**: The top left cell of the cell range to be included in this view.

-    **Cell End|String**: The bottom right cell of the cell range to be included in this view.

-    **Font|Font**: The name of the font used for texts.

-    **Text Color|Color**: The color of texts and lines that have no color specified in the spreadsheet.

-    **Text Size|Float**: The font size of texts.

-    **Line Width|Float**: The width of the cell borders.

## Notes

-   In {{VersionMinus|0.19}} some characters in spreadsheet cells will cause errors when displayed in a Spreadsheet View. These characters have to be XML encoded. Currently known characters are: {{Incode|&}} (replace with {{Incode|&amp;amp;}}) and {{Incode|&lt;}} (replace with {{Incode|&amp;lt;}}). See also this [discussion](https://forum.freecadweb.org/viewtopic.php?p=629853#p629885) in the forum.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw SpreadsheetView/pt-br
