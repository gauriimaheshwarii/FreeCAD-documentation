---
- GuiCommand:/de
   Name:Draft Line
   Name/de:Entwurf Linie
   MenuLocation:Entwurf → Linie
   Workbenches:[Entwurf](Draft_Workbench/de.md), [Arch Arbeitsbereich](Arch_Workbench/de.md)
   Shortcut:**L** **I**
   Version:0.7
   SeeAlso:[Entwurf Draht](Draft_Wire/de.md), [Entwurf Punkt](Draft_Point/de.md)
---

# Draft Line/de


</div>

## Beschreibung


<div class="mw-translate-fuzzy">

Das Linienwerkzeug erzeugt eine gerade Linie, die durch zwei Punkte definiert ist. Es wird das [Entwurf Linienstil](Draft_Linestyle/de.md) verwendet, das auf dem [Entwurf Tablett](Draft_Tray/de.md) gesetzt ist. Das Linienwerkzeug verhält sich genau wie das [Entwurf Draht](Draft_Wire/de.md) Werkzeug, nur dass es nach zwei Punkten stoppt.


</div>

A Draft Line is in fact a [Draft Wire](Draft_Wire.md) with only two points.

<img alt="" src=images/Draft_Line_example.jpg  style="width:400px;">


<div class="mw-translate-fuzzy">



*Linie erzeugt durch zwei Punkte*


</div>

## Anwendung

See also: [Draft Tray](Draft_Tray.md), [Draft Snap](Draft_Snap.md) and [Draft Constrain](Draft_Constrain.md).


<div class="mw-translate-fuzzy">

1.  Drücke die **<img src="images/Draft_Line.svg" width=16px> [Entwurf Linie](Draft_Line/de.md)** Schaltfläche, oder verwende **Entwurf** → **<img src="images/Draft_Line.svg" width=16px> [Linie](Draft_Line/de.md)** aus dem oberen Menü oder verwende die Tastaturkürzel: **L**, dann **I**.
2.  Klicke auf einen ersten Punkt in der 3D Ansicht, oder gib eine Koordinate ein und drücke die Taste **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste.
3.  Klicke auf einen zweiten Punkt in der 3D Ansicht, oder gib eine Koordinate ein und drücke die Taste **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste.


</div>

## Options

The single character keyboard shortcuts available in the task panel can be changed. See [Draft Preferences](Draft_Preferences.md). The shortcuts mentioned here are the default shortcuts.


<div class="mw-translate-fuzzy">

## Optionen

-   Drücke **X**, **Y** oder **Z** nach dem ersten Punkt, um den zweiten Punkt auf der angegebenen Achse zu beschränken.
-   Um Koordinaten manuell einzugeben, gib einfach die Zahlen ein und drücken dann **Enter** zwischen den einzelnen X-, Y- und Z-Komponenten.
    -   Du kannst auch die Polarkoordinaten des Punktes definieren, indem du einen Wert für \"Länge\" und \"Winkel\" angibst. Klicke auf das Kontrollkästchen neben \"Winkel\", um den Zeiger auf den angegebenen Winkel zu beschränken.
    -   Du kannst die **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste drücken wenn Du die gewünschten Werte hast, um den Punkt einzufügen.
-   Drücke {**R** oder klicke auf das Kontrollkästchen, um den *relativen* Modus umzuschalten. Wenn der Relativmodus eingeschaltet ist, sind die Koordinaten des zweiten Punktes relativ zum ersten; wenn nicht, sind sie absolut, bezogen auf den Ursprung (0,0,0).
-   Drücke **T** oder klicke auf das Kontrollkästchen, um den *Weiter*-Modus umzuschalten. Wenn der Fortsetzungsmodus eingeschaltet ist, wird das Linienwerkzeug nach der Eingabe des zweiten Punktes neu gestartet, so dass du ein weiteres Liniensegment zeichnen kannst, ohne die Werkzeugtaste erneut zu drücken.
-   Halte **Ctrl** während des Zeichnens gedrückt, um [Fang](Draft_Snap/de.md) deinen Punkt auf die nächstgelegene Fangposition zu zwingen, unabhängig von der Entfernung.
-   Halte **Shift** während des Zeichnens gedrückt, um deinen zweiten Punkt horizontal oder vertikal in Bezug auf den ersten zu [Beschränkung](Draft_Constrain/de.md).
-   Drücke **Strg**+**Z** oder drücke die {{button|<img src="images/Draft_UndoLine.svg" width=12px> Rückgängig}} Schaltfläche, um den letzten Punkt rückgängig zu machen.
-   Drücke **Esc** oder die Taste **Close**, um den aktuellen Befehl abzubrechen.


</div>

## Notes


<div class="mw-translate-fuzzy">

Die Linie kann durch doppelklicken des Elements in der Baumansicht geändert werden oder durch drücken der Schaltfläche **<img src="images/Draft_Edit.svg" width=16px> [Bearbeiten](Draft_Edit/de.md)**. Dann kannst Du die Punkte an eine andere Position ziehen.


</div>

## Preferences

See also: [Preferences Editor](Preferences_Editor.md) and [Draft Preferences](Draft_Preferences.md).

-   To change the number of decimals used for the input of coordinates, lengths and angles: **Edit → Preferences... → General → Units → Units settings → Number of decimals**.
-   To change the initial focus of the task panel to the **Length** input box: **Edit → Preferences... → Draft → General settings → Draft tools options → Set focus on Length instead of X coordinate**. Note that you must move the pointer in the [3D view](3D_view.md) for the change to take effect.
-   If the **Edit → Preferences... → Draft → General settings → Draft tools options → Use Part Primitives when available** option is checked, the command will create a [Part Line](Part_Line.md) instead of a Draft Line.

## Properties


<div class="mw-translate-fuzzy">

## Eigenschaften

Ein Linienobjekt teilt alle Eigenschaften eines **<img src="images/Draft_Wire.svg" width=16px>[Entwurf Draht](Draft_Wire/de.md)**, jedoch sind nur einige dieser Eigenschaften auf die Linie anwendbar.


</div>

## Scripting


<div class="mw-translate-fuzzy">

## Skripten


**Siehe auch:**

[Draft API](Draft_API/de.md) und [FreeCAD Skripten Grundlagen](FreeCAD_Scripting_Basics/de.md).


</div>


<div class="mw-translate-fuzzy">

Das Linienwerkzeug kann in [Makros](macros/de.md) und aus der [Python](Python/de.md) Konsole heraus durch folgende Funktion angesprochen werden:


</div>


```python
line = make_line(p1, p2)
line = make_line(LineSegment)
line = make_line(Shape)
```

-   Erzeugt ein `Line` Objekt zwischen den Punkten `p1` und `p2`, jeweils definiert durch ihren `FreeCAD.Vector`, mit Einheiten in Millimetern.
-   Erstellt ein `Line` Objekt aus einem `Part.LineSegment`.
-   Erzeugt ein `Line` Objekt vom ersten Knoten bis zum letzten Knoten der angegebenen `Shape`.

Beispiel:


```python
import FreeCAD as App
import Draft

doc = App.newDocument()

p1 = App.Vector(0, 0, 0)
p2 = App.Vector(1000, 500, 0)
p3 = App.Vector(-250, -500, 0)
p4 = App.Vector(500, 1000, 0)

line1 = Draft.make_line(p1, p2)
line2 = Draft.make_line(p3, p4)

doc.recompute()
```


<div class="mw-translate-fuzzy">





</div>



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft Line/de
