---
- GuiCommand:
   Name:Part XOR
   MenuLocation:Part → Split → Boolean XOR
   Workbenches:[Part](Part_Workbench.md)
   Version:0.17
   SeeAlso:[Part Boolean Fragments](Part_BooleanFragments.md), [Part Slice](Part_Slice.md), [Part Join features](Part_CompJoinFeatures.md), [Part Boolean](Part_Boolean.md)
---

# Part XOR/en

## Description

The <img alt="" src=images/Part_XOR.svg  style="width:24px;"> **Part XOR** command removes geometry shared by an even number of objects and leaves a void space between the involved objects. For two objects it represents a symmetric version of [Part Cut](Part_Cut.md).

<img alt="" src=images/Part_XOR-01.png  style="width:300px;"> <img alt="" src=images/Button_right.svg  style="width:16px;"> <img alt="" src=images/Part_XOR-02.png  style="width:300px;"> 
*Three overlapping objects → Result object*

## Usage

1.  Select two or more objects. It is also possible to select a [Part Compound](Part_Compound.md) containing two or more objects.
2.  There are several ways to invoke the command:
    -   Select the **Part → Boolean → <img src="images/Part_XOR.svg" width=16px> Boolean XOR** option from the menu.
    -   Press the **<img src="images/Part_XOR.svg" width=16px> [Boolean XOR](Part_XOR.md)** button.

## Notes

-   Void spaces are hard to detect if the selected objects do not have co-planar faces. To verify the XOR result the [Std ToggleClipPlane](Std_ToggleClipPlane.md) can then be used.

## Properties

## Scripting



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part XOR/en
