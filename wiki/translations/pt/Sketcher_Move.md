---
- GuiCommand:/pt
   Name/pt:Sketcher Move
   Icon:Sketcher_Move.svg
   Workbenches:[Sketcher](Sketcher_Workbench/pt.md)
   MenuLocation:Sketch → Ferramentas de esboço (Sketcher) → Move
   Shortcut:Ctrl + M
   Version:0.18
   SeeAlso:[Clonar](Sketcher_Clone/pt.md), [Copiar](Sketcher_Copy/pt.md)
---

# Sketcher Move/pt


</div>



## Descrição

Moves the selected sketch elements from one point to another, using the last selected point as reference.

![](images/sketcher_move.png‎ ) 
*The sequence of clicks is indicated by yellow arrows with numbers. Select element '''A'''; see a vector line indicated by two red lines from pivot point '''A''' pointing to mouse position number '''2'''. Move the mouse pointer to the target location '''3''' and see the element now as '''B''' autoconstrained on point '''3'''.*

## Usage

1.  Select the sketch elements for the move operation.
2.  There are several ways to invoke the command:
    -   Press the **[<img src=images/Sketcher_Move.svg style="width:16px"> [Move](Sketcher_Move.md)** button in the toolbar.
    -   Use the **Z** then **M** keyboard shortcut.
    -   Use the **Sketch → Sketcher tools → [<img src=images/Sketcher_Move.svg style="width:16px"> Move** entry in the menu.
3.  Move the mouse in the [3D view](3D_view.md) to the desired location.By keeping **Ctrl** pressed (**Cmd** on macOS), the angle to the location can be fixed in steps of 5°. <small>(v0.20)</small> 
4.  Left-click in the 3D view to finish the move. The existing constraints move as well.
5.  If you want to detach an element and move it freely, delete its locking constraints and drag it with the mouse.





{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher Move/pt
