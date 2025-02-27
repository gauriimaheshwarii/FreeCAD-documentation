---
- GuiCommand:/de
   Name:Sketcher ToggleConstruction
   Name/de:Sketcher UmschalterKonstruktion
   MenuLocation:Skizze → Skizzengeometrien → Umschalten der Hilfsgeometrie
   Workbenches:[Sketcher](Sketcher_Workbench/de.md)
   Shortcut:**G** **N**
   SeeAlso:[Sketcher UmschalterRandbedingung](Sketcher_ToggleDrivingConstraint/de.md)
---

# Sketcher ToggleConstruction/de

## Beschreibung

Dieses Werkzeug schaltet die Skizzengeometrie vom/zum Konstruktionsmodus um. Es kann auf jeder Art von Geometrie angewendet werden: Linie, Bogen oder Kreis.

Die Konstruktionsgeometrie ist ein wichtiges Werkzeug des Sketchers. Wenn eine Skizze für eine 3D-Funktion verwendet wird, wird die Konstruktionsgeometrie ignoriert.

Im **[<img src=images/Sketcher_EditSketch.svg style="width:16px"> [Bearbeitungsmodus](Sketcher_EditSketch/de.md)** wird die Konstruktionsgeometrie blau dargestellt und wird nicht grün, wenn eine Skizze vollständig bestimmt ist. Sobald **[<img src=images/Sketcher_LeaveSketch.svg style="width:16px">[Skizze verlassen](Sketcher_LeaveSketch/de.md)** ausgewählt wird, wird die Konstruktionsgeometrie in der [3D-Ansicht](3D_view/de.md) ausgeblendet.

Konstruktionslinien können von der Funktion **[<img src=images/PartDesign_Revolution.svg style="width:16px"> [PartDesign Drehteil](PartDesign_Revolution/de.md)** als Drehachse verwendet werden.

<img alt="" src=images/Sketcher_ConstructionMode_fr_01.png  style="width:480px;">

## Anwendung

Dieses Werkzeug kann auf zwei Arten verwendet werden:

1.  Ohne etwas in der [3D-Ansicht](3D_view/de.md) ausgewählt zu haben:
    -   Den Bearbeitungsmodus aufrufen durch Anklicken der Schaltfläche **[<img src=images/Sketcher_ToggleConstruction.svg style="width:16px"> [Umschalten der Hilfsgeometrie](Sketcher_ToggleConstruction/de.md)** oder durch Auswahl des Menüeintrags **Skizze → Skizzengeometrien → [<img src=images/Sketcher_ToggleConstruction.svg style="width:16px"> Umschalten der Hilfsgeometrie**.
    -   Dies ändert die Farbe für die Ertstellung neuer Geometrieelemente auf Blau.
    -   Neue Geometrieelemente werden jetzt im Konstruktionsmodus erstellt.
2.  Mit einem oder mehreren in der [3D-Ansicht](3D_view/de.md) ausgewählten Geometrieelementen:
    -   Das Werkzeug aufrufen durch Anklicken der Schaltfläche **[<img src=images/Sketcher_ToggleConstruction.svg style="width:16px"> [Umschalten der Hilfsgeometrie](Sketcher_ToggleConstruction/de.md)** oder durch Auswahl seines Menüeintrags.
    -   Die ausgewählten Elemente werden jetzt in der Konstruktionsmodus versetzt.
    -   Danach werden neue Elemente wieder als normale Geometrie erstellt.

## Beispiel

Verwendet man den Konstruktionsmodus für einige Skizzenelemente,

<img alt="" src=images/Sketcher_ConstructionMode_fr_01.png  style="width:450px;">

werden sie, sobald **[<img src=images/Sketcher_LeaveSketch.svg style="width:16px"> [Skizze verlassen](Sketcher_LeaveSketch/de.md)** ausgewählt wird, in der [3D-Ansicht](3D_view/de.md) unsichtbar (sind aber immer noch im Sketcher-Bearbeitungsmodus vorhanden).

<img alt="" src=images/Sketcher_ConstructionMode_fr_02.png  style="width:450px;">

## Hinweise

-    **[<img src=images/Sketcher_CreatePoint.svg style="width:16px"> [Punkt erstellen](Sketcher_CreatePoint/de.md)**wird immer Punkte im Konstruktionsmodus erstellen unabhängig von der Einstellung des Umschalters in der Symbolleiste. Sollen Punkte in normale Geometrie gewandelt werden, wählt man sie nach der Erstellung in der [3D-Ansicht](3D_view/de.md) aus und klickt dann auf die Schaltfläche **[<img src=images/Sketcher_ToggleConstruction.svg style="width:16px"> [Umschalten der Hilfsgeometrie](Sketcher_ToggleConstruction.md)**. {{Version/de|0.19}}





{{Sketcher_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ToggleConstruction/de
