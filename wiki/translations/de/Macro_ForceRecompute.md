# Macro ForceRecompute/de
{{Macro/de
|Name=Macro Force Recompute
|Icon=Force_Recompute.png
|Description=Dieses kleine Makro erzwingt eine manuelle Neuberechnung des Modells.
Manchmal nimmt der Benutzer Änderungen am Modell in FreeCAD vor.
Aber FreeCAD scheint sie nicht zu erkennen.
(Ab <small>(v0.17)</small> ) kann die Wirkung dieses Makros über die GUI erreicht werden. Klicke mit der rechten Maustaste auf das Projekt in der Modellstrukturansicht und wähle "Zum Neuberechnen markieren" aus dem Kontextmenü. Danach klicke auf die Schaltfläche Neu berechnen.
|Author=shoogen
|Version=1.0
|Date=2014-09-01
|FCVersion=All
|Download=[https://www.freecadweb.org/wiki/images/8/88/Force_Recompute.png ToolBar Icon]
}}


<div class="mw-translate-fuzzy">

## Beschreibung

Manchmal, wenn ein Benutzer Änderungen am Modell vornimmt, scheint FreeCAD diese nicht zu erkennen und zu integrieren. Zusätzlich dazu bleibt die blaue **<img src="images/Std_Refresh.svg" width=24px> [Aktualisieren/Neuberechnen](Std_Refresh/de.md)** Taste ausgegraut. Daher wurde dieses kleine Makro entwickelt, um eine manuelle Neuberechnung des Modells zu erzwingen.


</div>

Sometimes when a user applies changes to the model, FreeCAD does not seem to recognize/integrate them. In addition to that, the blue **<img src="images/Std_Refresh.svg" width=24px> [Refresh/Recompute](Std_Refresh.md)** button remains greyed out. Hence this small macro was designed to force a manual recompute of the model.


<div class="mw-translate-fuzzy">

**Hinweis:** Ab {{VersionPlus/de|0.17}} kann die Wirkung dieses Makros über die GUI erreicht werden. Rechtsklicke auf das Projekt in der [Modellbaumansicht](Tree_view/de.md) und wähle **Zum Neuberechnen markieren** aus dem Kontextmenü. Dadurch wird das Symbol Aktualisieren/Neuberechnen wieder aktiv. Drücke nun auf die <img alt="" src=images/Std_Refresh.svg  style="width:24px;"> [Aktualisieren/Neuberechnen](Std_Refresh/de.md) Taste, um eine Neuberechnung auszulösen.


</div>


<div class="mw-translate-fuzzy">

## Anwendung

Führe das Makro bei Bedarf aus.


</div>

Run the macro when necessary.

## Skript

ToolBar Icon <img alt="" src=images/Force_Recompute.png  style="width:24px;">

**Macro Force_Recompute.py**


{{MacroCode|code=
# -*- coding: utf-8 -*-
# Force Recompute
# macro provided by shoogen

import FreeCAD
for obj in FreeCAD.ActiveDocument.Objects:
 obj.touch()
FreeCAD.ActiveDocument.recompute()

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Macro ForceRecompute/de
