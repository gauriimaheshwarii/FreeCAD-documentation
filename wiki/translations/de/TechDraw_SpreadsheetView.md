---
- GuiCommand:/de
   Name:TechDraw SpreadsheetView
   Name/de:TechDraw Tabellenansicht
   MenuLocation:TechDraw → Tabellenansicht einfügen
   Workbenches:[TechDraw](TechDraw_Workbench/de.md), [Spreadsheet](Spreadsheet_Workbench/de.md)
---

# TechDraw SpreadsheetView/de

## Beschreibung

Dieses Werkzeug ermöglicht es, eine ausgewählte [Kalkulationstabelle](Spreadsheet_Workbench/de.md) in einer Tabellenansicht auf einem [Zeichnungsblatt](TechDraw_Workbench/de.md) darzustellen.

![](images/TechDraw_Spreadsheetview.png ) 
*Darstellung einer eingefügten Kalkulationstabelle (Spreadsheet-Objekt) als Tabellenansicht (Sheet-Objekt) auf einem TechDraw-Zeichnungsblatt*

## Anwendung

1.  Ein Tabellenblatt in der [Bauamsicht](Tree_view/de.md) auswählen.
2.  Die Schaltfläche **<img src="images/TechDraw_SpreadsheetView.svg" width=16px> [Tabellenansicht einfügen](TechDraw_SpreadsheetView/de.md)** drücken

## Eigenschaften

Siehe auch [TechDraw Ansicht](TechDraw_View/de#Eigenschaften.md)

### Daten


{{TitleProperty|Spreadsheet}}

-    **Source|Link**(Quelle): Das zum Zeichungsblatt hinzuzufügende Tabellenblatt.

-    **Cell Start|String**(Zellanfang): Die linke obere Zelle des Zellbereichs, der dieser Ansicht hinzugefügt werden soll.

-    **Cell End|String**(Zellenende): Die rechte untere Zelle des Zellbereichs, der in diese Ansicht aufgenommen werden soll.

-    **Font|Font**(Schriftart): Der Name der für Texte verwendeten Schriftart.

-    **Text Color|Color**(Farbe): Die Farbe von Linien und Texten, denen in der Kalkulationstabelle kein Farbe zugewiesen wurde.

-    **Text Size|Float**(Schriftgröße): Die Schriftgröße von Texten.

-    **Line Width|Float**(Strichstärke): Die Breite der Zellränder.

## Hinweise

-   In der {{VersionMinus/de|0.19}} erzeugen einige Zeichen in Tabellenzellen Fehler, wenn sie in einer Tabellenansicht dargestellt werden. Diese Zeichen müssen XML-kodiert werden. Bisher bekannte Zeichen sind: {{Incode|&}} (ersetz durch {{Incode|&amp;amp;}}) und {{Incode|&lt;}} (ersetz durch {{Incode|&amp;lt;}}). Siehe auch diese [Diskussion](https://forum.freecadweb.org/viewtopic.php?p=629853#p629885) (engl.) im Forum.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw SpreadsheetView/de
