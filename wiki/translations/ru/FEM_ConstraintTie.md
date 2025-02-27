---
- GuiCommand:
   Name:FEM ConstraintTie
   MenuLocation:Model → Mechanical Constraints → Constraint tie
   Workbenches:[FEM](FEM_Workbench.md)
   Version:0.19
   SeeAlso:[FEM Constraint pressure](FEM_ConstraintPressure.md)
---

# FEM ConstraintTie/ru

## Описание

Defines a tie constraint that connects the two selected surfaces in such a way that (as opposed to how contact works) they can\'t separate or slide on each other throughout the analysis. Thus, the surfaces remain permanently bonded all the time.

## Применение

1.  There are several ways to invoke the command:
    -   Press the **<img src="images/FEM_ConstraintTie.svg" width=16px> [FEM ConstraintTie](FEM_ConstraintTie.md)** button.
    -   Select the **Model → Mechanical Constraints → <img src="images/FEM_ConstraintTie.svg" width=16px> Constraint tie** option from the menu.
2.  Press the **Add** button in the task panel and then click on the face you want to add to tie constraint definition. Exactly two faces have to be added, one after the other.
3.  Optionally, define Tolerance - tie constraint will be applied only to nodes separated from the opposite surface by the distance not larger than the one specified here.





{{FEM_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > FEM ConstraintTie/ru
