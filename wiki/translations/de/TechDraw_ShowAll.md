---
- GuiCommand:/de
   Name:TechDraw ShowAll
   Name/de: TechDraw AllesAnzeigen
   MenuLocation:TechDraw → AllesAnzeigen
   Workbenches:[TechDraw](TechDraw_Workbench/de.md)
   Version:0.19
   SeeAlso:[TechDraw Ändert Darstellung von Linie(n)](TechDraw_DecorateLine/de.md)
---

# TechDraw ShowAll/de

## Beschreibung

Das ShowAll Werkzeug zeigt oder verbirgt unsichtbare Linien in einer Ansicht. Beachte, dass \"unsichtbar\" ein kosmetischer Zustand ist, nicht zu verwechseln mit ausgeblendeten Linien, die geometrische Konstrukte sind.

## Verwendung

1.  Wähle eine Ansicht auf einer Seite oder im Baum.
2.  Drücke die **{{Button|<img src="images/TechDraw_ShowAll.svg" width=16px>** [Anzeigen/Verbergen Unsichtbare Kanten ](TechDraw_ShowAll/de.md)}} Schaltfläche
3.  Der Zustand der unsichtbaren Linien in der Ansicht wird umgekehrt.

## Eigenschaften

Das AlleAnzeigen Werkzeug hat keine Eigenschaften, da es kein Dokumentobjekt ist.

## Skripten

Siehe auch: [Autogenerierte API Dokumentation](https://freecad.github.io/SourceDoc/) und [FreeCAD Grundlagen Skripten](FreeCAD_Scripting_Basics/de.md).

Die Wirkung des AllesAnzeigen Werkzeugs kann in [Makros](Macros/de.md) oder der [Python](Python/de.md) Konsole dupliziert werden. 
```python
>>> v = App.ActiveDocument.View
>>> vvo = v.ViewObject
>>> vvo.ShowAllEdges = True
>>> App.activeDocument().recompute()
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw ShowAll/de
