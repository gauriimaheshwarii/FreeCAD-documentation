---
- GuiCommand:/de
   Name:TechDraw WeldSymbol
   Name/de:TechDraw Schweißsymbol
   MenuLocation:TechDraw → Hinzufügen von Schweißinformationen zur Hinweislinie
   Workbenches:[TechDraw](TechDraw_Workbench/de.md)
   Version:0.19
   SeeAlso:[TechDraw Hinweislinie](TechDraw_LeaderLine/de.md)
---

# TechDraw WeldSymbol/de

## Beschreibung

Das Werkzeug Schweißsymbol fügt einer bestehenden Hinweislinie Schweißspezifikationen hinzu.

<img alt="" src=images/TechDraw_WeldingSymbol_example.png  style="width:330px;"> 
*Schweißspezifikation zu einer Hinweislinie hinzugefügt*

## Anwendung

1.  Eine vorhandene [Hinweislinie](TechDraw_LeaderLine/de.md) auswählen.
2.  Die Schaltfläche **<img src="images/TechDraw_WeldSymbol.svg" width=16px> [Hinzufügen von Schweißinformationen zur Hinweislinie](TechDraw_WeldSymbol/de.md)** drücken.
3.  Der Aufgabenbereich wird geöffnet. Er ermöglicht es, individuelle Schweißsymbole und begleitenden Text festzulegen, die der Hinweislinie hinzugefügt werden.
4.  Die Schaltfläche OK drücken, um den Dialog zu verlassen und die Änderungen zu speichern.
5.  Nachdem das Schweißsymbol erstellt wurde, kann es durch Doppelklicken auf das Schweißsymbol im Baum bearbeitet werden.

## Eigenschaften

### Schweißsymbol

-    {{PropertyData/de|All Around}}: Zeigt das Symbol für \"umlaufende Naht\" (Kreis) am Knick der Hinweislinie.

-    {{PropertyData/de|Field Weld}}: Zeigt das Symbol für *Baustellennaht* (Flagge) am Knick der Hinweislinie.

-    {{PropertyData/de|Alternating Weld}}: Versetzt das untere Symbol, um wechselseitig Schweißungen anzuzeigen.

-    {{PropertyData/de|Tail Text}}: Text, der am Ende der Hinweislinie angezeigt werden soll.

### Kacheln

Jedes einzelne Symbol (\"Pfeilseite\" und \"andere Seite\") wird durch ein \"Kachel\"-Objekt dargestellt. Einem Schweißsymbol sind 1 oder 2 Kacheln zugeordnet. Die Eigenschaften können geändert werden. Dazu muß in der Baumansicht auf die jeweilige Schweißkachel geklickt werden. Unten im Eigenschaftsfeld können dann Änderungen vorgenommen werden:

-    {{PropertyData/de|Tile Parent}}: das ursprüngliche Schweißsymbol

-    {{PropertyData/de|Tile Row}}: Reihe der Kachel. 0 bedeutet oberhalb der Linie, -1 unterhalb der Linie. **Hinweis:** Wenn du die Reihe einer Kachel änderst, musst du auch die Kachel für die zweite Seite ändern! Auf diesem Weg kannst du die Seiten tauschen.

-    {{PropertyData/de|Tile Column}}: Im Moment = 0, zur Zeit noch nicht änderbar.

-    {{PropertyData/de|Symbol File}}: Verzeichnis und Dateiname der SVG-Datei für das Symbol.

-    {{PropertyData/de|Left Text}}: Text, der links neben dem SVG-Symbol angezeigt werden soll.

-    {{PropertyData/de|Center Text}}: Text, der oberhalb/unterhalb des SVG-Symbols angezeigt werden soll.

-    {{PropertyData/de|Right Text}}: Text, der rechts neben dem SVG-Symbol angezeigt werden soll.

## Skripten

Siehe auch: [Autogenerierte API Dokumentation](https://freecad.github.io/SourceDoc/) und [FreeCAD Grundlagen Skripten](FreeCAD_Scripting_Basics/de.md).

Das Werkzeug Schweißsymbol kann in [Makros](Macros/de.md) und von der [Python](Python/de.md)-Konsole aus mit den folgenden Funktionen verwendet werden:


```python
symbolName = "DrawWeldSymbol001")
symbolType = "TechDraw::DrawWeldSymbol"
App.activeDocument().addObject(symbolType, symbolName)
App.activeDocument().Page.addView(App.activeDocument().DrawWeldSymbol001)
App.activeDocument().DrawWeldSymbol001.Leader = myLeader
App.activeDocument().DrawWeldSymbol001.AllAround = True
App.activeDocument().DrawWeldSymbol001.FieldWeld = True
App.activeDocument().DrawWeldSymbol001.AlternatingWeld = True
App.activeDocument().DrawWeldSymbol001.TailText = "process text"

tileName = "DrawTileWeld001"
tileType = "TechDraw::DrawTileWeld"
App.activeDocument().addObject(tileType, tileName)
App.activeDocument().DrawTileWeld001.TileParent = App.activeDocument().DrawWeldSymbol001
App.activeDocument().DrawTileWeld001.TileRow = 0
App.activeDocument().DrawTileWeld001.TileColumn = 0
App.activeDocument().DrawTileWeld001.SymbolFile = fullPathToMySvgFile
App.activeDocument().DrawTileWeld001.LeftText = "left text"
App.activeDocument().DrawTileWeld001.RightText = "right text"
App.activeDocument().DrawTileWeld001.CenterText = "center text"
```

## Svg Symbol Kacheln 

-   Einzelne Symbole werden durch 64x64 Pixel große SVG-Dateien gebildet. Zusätzliche Symbole können in einem SVG-Programm wie z.B. [Inkscape](https://en.wikipedia.org/wiki/Inkscape) aus einem der mitgelieferten Symbole als Vorlage erstellt werden.

<img alt="" src=images/Techdraw-WeldingSymbolLayoutArrow.svg  style="width:128px;"> <img alt="" src=images/Techdraw-WeldingSymbolLayoutOther.svg  style="width:128px;">

-   Einzelne Symbole werden durch SVG-Dateien mit 64x64 (nominal) Pixeln gebildet. Die Kacheln haben einen \"Rand\" von 4px. Der Rand sorgt dafür, dass sich Hinweislinie und Symbol gut treffen.
-   Das Symbol wird in Schwarz auf einem transparenten Hintergrund gezeichnet. Die Strichstärke beträgt 0,5 mm.
-   Die Hinweislinie verläuft unterhalb der Symbole für die Pfeilseite (siehe Abbildung links) und oberhalb der Symbole für die \"andere\" Seite (siehe Abbildung rechts).
-   Es gibt keinen besonderen Namensstandard, außer dass bei Bedarf \"Auf/Ab\" an die Symbole der Pfeil- und der anderen Seite angehängt wird.

## Hinweise

-   Du kannst dein Schweißsymbol bearbeiten, indem du in der Baumansicht darauf doppelklickst. Ein Doppelklick in den Grafikbereich wird noch nicht unterstützt.
-   Es gibt einen [Einstellungsparameter](TechDraw_Preferences/de.md) für das Standard Schweißsymbolverzeichnis. Du kannst deine eigenen Symbole in einem persönlichen Verzeichnis hinzufügen.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw WeldSymbol/de
