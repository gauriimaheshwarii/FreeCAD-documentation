---
- GuiCommand:/pt
   Name:Constraint Horizontal
   Name/pt:Constraint Horizontal
   Workbenches:[Sketcher](Sketcher_Workbench/pt.md)
   Shortcut:H
   MenuLocation:Sketch → Sketcher constraints → Constrain horizontally
   SeeAlso:[Constraint Vertical](Sketcher_ConstrainVertical/pt.md)
---

# Sketcher ConstrainHorizontal/pt


</div>

## Descrição

The Horizontal Constraint forces a selected line or lines in the sketch to be parallel to the horizontal axis of the sketch.


<div class="mw-translate-fuzzy">

## Como usar 


</div>

<img alt="" src=images/HorizontalConstraint1.png  style="width:500px;"> 
*Select a line in the sketch by clicking on it.*

<img alt="" src=images/HorizontalConstraint2.png  style="width:500px;"> 
*The line turns dark green.*

<img alt="" src=images/HorizontalConstraint3.png  style="width:500px;"> 
*Apply the Horizontal Constraint by clicking on the **[<img src=images/Sketcher_ConstrainHorizontal.svg style="width:16px"> [Constraint horizontal](Sketcher_ConstrainHorizontal.md)* in the Sketcher Constraints toolbar or by selecting the Constrain horizontally menu item in the Sketcher constraints sub menu of the Sketch menu item in the Sketcher work bench (or the Part Design menu item of the Part Design work bench). The selected line is constrained to be parallel to the horizontal axis of the sketch.**

<img alt="" src=images/HorizontalConstraint4.png  style="width:500px;"> 
*Multiple lines may be selected*

<img alt="" src=images/HorizontalConstraint5.png  style="width:500px;"> 
*and then applying the constraint as described above, they are constrained to be parallel to the sketch horizontal axis.*

## Scripting


```pythonSketch.addConstraint(Sketcher.Constraint('Horizontal', Line))```

The [Sketcher scripting](Sketcher_scripting.md) page explains the values which can be used for `Line` and contains further examples on how to create constraints from Python scripts.


<div class="mw-translate-fuzzy">


</div>


{{Sketcher Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainHorizontal/pt
