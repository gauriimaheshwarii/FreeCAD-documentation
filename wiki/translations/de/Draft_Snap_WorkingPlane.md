---
- GuiCommand:/de
   Name:Draft Snap WorkingPlane
   Name/de:Draft Arbeitsebene
   MenuLocation:Entwurf → [Objektfang](Draft_Snap/de.md) → Arbeitsebene
   Workbenches:[Draft](Draft_Workbench/de.md), [Arch](Arch_Workbench/de.md)
   SeeAlso:[Draft Objektfang](Draft_Snap/de.md), [Draft Ebene markieren](Draft_SelectPlane/de.md)
---

# Draft Snap WorkingPlane/de


</div>

## Beschreibung


<div class="mw-translate-fuzzy">

Diese Methode platziert immer einen neuen Punkt auf der aktuellen [Arbeitsebene](Draft_SelectPlane/de.md), selbst wenn eine andere Einrastmethode verwendet und ein Punkt außerhalb dieser Arbeitsebene ausgewählt wird.


</div>

![](images/Draft_Snap_WorkingPlane_example.png )


<div class="mw-translate-fuzzy">



*Einrasten des zweiten Punkts einer Linie an einem Endpunkt einer Kante eines Körpers, der dann auf die XY-Ebene projiziert wird*


</div>

## Anwendung

For general information about snapping see [Draft Snap](Draft_Snap.md).

1.  Optionally change the [working plane](Draft_SelectPlane.md).
2.  Make sure snapping is enabled. See <img alt="" src=images/Draft_Snap_Lock.svg  style="width:16px;"> [Draft Snap Lock](Draft_Snap_Lock.md).
3.  If **Draft Snap WorkingPlane** is not active do one of the following:
    -   Press the **<img src="images/Draft_Snap_WorkingPlane.svg" width=16px>** button in the Draft snap toolbar.
    -   Press the **<img src="images/Draft_Snap_WorkingPlane.svg" width=16px>** button in the [Draft snap widget](Draft_snap_widget.md).
4.  Make sure at least one other snap option is active.
5.  Choose a [Draft](Draft_Workbench.md) or [Arch](Arch_Workbench.md) command to create your geometry.
6.  Note that you can also change snap options while a command is active.
7.  Move the cursor over the object you want to snap to.
8.  The object is highlighted.
9.  If a snap point is found it is projected onto the [working plane](Draft_SelectPlane.md) where it is marked.
10. Click to confirm the point.


{{Userdocnavi/de}}

See [Draft Snap](Draft_Snap#Preferences.md).



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft Snap WorkingPlane/de
