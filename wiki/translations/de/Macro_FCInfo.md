# Macro FCInfo/de
<div class="mw-translate-fuzzy">


{{Macro/de
|Name=Macro FCInfo
|Translate=Macro FCInfo
|Icon=FCInfo.png
|Description=Gibt eine Reihe von Informationen zum Formular aus.
|Author=Mario52
|Version=1.22
|Date=2020/11/12
|FCVersion=All
|Download=Download the [https://forum.freecadweb.org/download/file.php?id=50755 Macro_FCInfo_Icon] package and paste it in the same directory of the macro
|SeeAlso=[Arch Survey|<img src=images/Arch_Survey.svg style="width:24px"> [Arch Survey](Arch_Survey/de.md)<br />[Macro SimpleProperties](Macro_SimpleProperties/de.md)
}}


</div>


{{Macro
|Name=Macro FCInfo
|Icon=FCInfo.png
|Description=Gives information about the selected shape and can display a conversion of length, inclination (degrees, radians, grades, percent), area, volume and weight in different units (metric and imperial). The macro now also works for the elements of a sketch in edit mode.
<br />French Version [https://gist.githubusercontent.com/mario52a/6afc64081c4eb8be3b93/raw/795cac01c84fbbfa7ea68703c7138667119995d8/FCInfo_fr_Ver_1-26c-rmu_Docked.FCMacro Version française]
|Author=Mario52
|Version=1.26c
|Date=2022/04/19
|FCVersion=All
|SeeAlso=[Arch Survey|<img src=images/Arch_Survey.svg style="width:24px"> [Arch Survey](Arch_Survey.md)<br /> [Macro_SimpleProperties|<img src=images/Macro_SimpleProperties.png style="width:24px"> [Macro SimpleProperties](Macro_SimpleProperties.md)<br /> [<img src=images/Macro_FCInfoGlass.png style="width:24px"> [Macro FCInfoGlass](Macro_FCInfoGlass.md)
}}

## Description


<div class="mw-translate-fuzzy">

## Beschreibung

Gibt eine Reihe von Informationen über die ausgewählte Form und kann eine Umwandlung von Länge, Neigung (Grad, Bogenmaß, Neigung, Fließvermögen), Form, Oberfläche, Volumen und Gewicht der Form in der ausgewählten Dichte in verschiedenen Mengeneinheiten international und englisch anzeigen-Saxon.


</div>


{{Codeextralink|https://gist.githubusercontent.com/mario52a/8d40ab6c018c2bde678f/raw/5577cf1a8818a4cbc5790cce335df158713b5841/FCInfo_en_Ver_1-26c-rmu_Docked.FCMacro}}

<img alt="" src=images/Macro_FCInfo_00_en.png  style="width:480px;"> 
*FCInfo*

## Utilisation


<div class="mw-translate-fuzzy">

## Nutzung

Wählen Sie ein Objekt aus oder starten Sie die Anwendung und wählen Sie ein Objekt aus. Eine Reihe von Informationen wird angezeigt. Seine Berechnungen basieren auf der Einheit \"FreeCAD\", also \"mm\" für jede neue Auswahl. Die Längeneinheit wird immer auf \"mm\" und der Winkel auf Dezimalgrad zurückgesetzt. <img alt="upper window" src=images/Macro_FCInfo_06.png  style="width:200px;"><img alt="lower window" src=images/Macro_FCInfo_07.png  style="width:200px;">


</div>




**Sector 1: Document**

-   Dokumentname
-   Beschriftung des Objekts
-   Interner Name des Objekts
-   Unterelementname des Objekts
-   Typ des Objekts


<div class="mw-translate-fuzzy">

**Sector 2: Coordinates click mouse**

-   Koordinaten X, Y und Z klicken Sie mit der Maus
-   Die Schaltfläche Erstellen auf Punkt, Achse, Ebene, Vektorachse erstellen *\'FreeCAD.Vector (-24.0, 240.0, 7.0)\'*


</div>


<div class="mw-translate-fuzzy">

**Sector 3: Value**

-   Länge des Objekts, wenn das Objekt ein Gesichtsumfang ist, Einheitsgröße kann ausgewählt werden:
    km, hm, dam, m, dm, cm, *\'mm\'*, µm, nm, pm, fm, zoll, link, fuß, hof, barsch, kette, furlong, meile, liga, nautique. Wenn das Objekt ein Kreis ist, ist eine Sekunde lineEdit offen und zeigt den Radius des Kreises an.
-   Umfang der Form


</div>


<div class="mw-translate-fuzzy">

**Sector 4: Vertexes and details**

-   CheckBox für die Suche oder nicht alle Details des Objekts, wenn nicht nur der Hauptwert angezeigt wird.
-   Scheitelpunkte und Details der Form (compt_Edge), (compt_Faces), (compt_Vector of the Face)
    max. 200 Zeilen in der Tabelle, wenn mehr als 200 Zeilen vorhanden sind (! + 200) und die Anzahl von Zeilen
    (vollständige Details können über die Schaltfläche {{KEY | Save}} in einer Datei im CSV-Format gespeichert werden. Die Datei kann in einer Tabelle mit dem {{KEY | Read}} oder von einer externen Tabelle als angezeigt werden [LibreOffice](https://www.libreoffice.org/) [OpenOffice](http://openoffice.apache.org/downloads.html) or other)


</div>


<div class="mw-translate-fuzzy">

**Sector 5: Inclination**

-   Neigungen des Objekts können angezeigt werden in:
-   **Dezimalgrad**, Beispiel: 174.831872611 °
-   **Grad Minute Sekunde**, Beispiel: 174 ° 49 \'54.741401\' \'
-   **radian**, ex: 3.05139181449 rad
-   **grade**, ex: 194.257636235 gon
-   **pourcent** ex: 30 ° = 57,74%
-   Neigungen in den Ebenen XY, YZ, ZX und deren Koordinaten
-   **Richtungsobjekt**, gibt die Richtung des Objekts an. Die Berechnung lautet: coord_1 - coord_2 = Richtung (oder umgekehrt)
    -   
        **Line**
        
        Diese Schaltfläche erstellt eine Linie in Richtung des Objekts
-   **ValueAt** gibt den 3D-Vektor zurück, der einem Parameterwert entspricht.


</div>


<div class="mw-translate-fuzzy">

**Sector 6: Surface and Volume**

-   Die Oberfläche der angezeigten Einheitsgröße kann ausgewählt werden
-   Die Oberfläche der angezeigten Einheitsgröße kann ausgewählt werden
-   Das Volumen der angezeigten Einheitsgröße kann ausgewählt werden
-   Dichte des Materials in **kg von dm3**
    (die \"spinBox\" ist auf **7,5** kg gesetzt, durchschnittliche Stahldichte. Wenn Sie einen anderen Standardwert wünschen , ändern Sie den Wert der Dichte, Zeile 204)
-   Die **Gramm** -Untereinheit kann gewählt werden:
    Tonne, Quintintal, kg, hg, Tag, **Gramm**, dg, mg, mg, µg, ng, pg, fg, gr (getreide), dr (drachm), oz (einmalig), oz t (einmal troy),
    lb t (livre troy), lb (livre av), st (stein), qtr (viertel) cwt (Zentner), Tonneau fr, ct
-   Gewicht der angezeigten Einheitsmasse kann ausgewählt werden


</div>


<div class="mw-translate-fuzzy">

**Sector 7: BoundBox**

-   BoundBox extreme Abmessungen der Form


</div>


<div class="mw-translate-fuzzy">

**Sector 8: Center of:**

-   Mittelpunkt der Form und dieser Koordinaten XYZ
-   Massenmittelpunkt und diese Koordinaten XYZ
-   Die Schaltfläche kann auf Punkt, Achse, Ebene und Vektorachsenform erstellt werden**FreeCAD.Vector(-24.0, 240.0, 7.0)**


</div>


<div class="mw-translate-fuzzy">

**Sector 9: Inertia**

-   Trägheitsmoment und diese Koordinaten Länge und Gewicht
-   Die Schaltfläche Erstellen auf Punkt, Achse, Ebene, Vektorachse erstellen **FreeCAD.Vector (-24.0, 240.0, 7.0)**
    -   Aktionslinie 1: x1, y1, z1
    -   Aktionslinie 2: x2, y2, z2
    -   Aktionslinie 3: x3, y3, z3
    -   Aktion 4 Diagonale: x1, y2, z3

Länge und Gewicht gleich

-   Determinante 1: Berechnet die Determinante des wissenschaftlichen Matrixwerts
-   Determinante 2: Berechnet die Determinante des Matrix-Dezimalwerts


</div>

**Section 10: SpreadSheet**

-    **Read**: Lesen Sie die Daten in einer Kalkulationstabelle, die **.FCInfo** oder txt, asc, csv gespeichert wurde

-    **Save**: Speichern Sie die Daten in der unter **.FCInfo** oder txt, asc, csv ausgewählten Form auf der Festplatte

-    **Tabulation**: Das Trennzeichen ist Tabulation

-    **Comma**: Das Trennzeichen ist Comma

-    **Semikolon**: Das Trennzeichen ist Semikolon

-    **Space**: Das Trennzeichen ist Space


<div class="mw-translate-fuzzy">

Option zum Speichern oder Lesen des spreadSheets mit unterschiedlichen Trennzeichen, Tabulation, Komma, Semikolon, Leerzeichen
Die Tabellierung ist das Trennzeichen für das FreeCAD spreadSheet-Modul
Die Nummer dieser vier Trennzeichen wird für Hilfe berechnet, falls unbekannt
Die COMMA sind das alte (01.16 und davor) Trennzeichen des FCInfo-Makros
Aus Kompatibilitätsgründen mit dem FreeCAD-SpreadSheet und seit Version 01.17 ist TABULATION standardmäßig das Trennzeichen
Wenn Sie Ihre alte FCInfo-Kalkulationstabelle konvertieren möchten: Öffnen Sie sie in FCInfo und speichern Sie sie mit aktivierter Option Tabulation


</div>


<div class="mw-translate-fuzzy">

**Section 11: Main**

-    **CheckBox Clip Board**: Wenn diese Option aktiviert ist, werden die Koordinaten in ClipBoard-Form gespeichert: **FreeCAD.Vector (-24.0, 240.0, 7.0)**

-    **CheckBox Point**: Wenn diese Option aktiviert ist, wird in der angezeigten Koordinate ein Punkt erstellt: **FreeCAD.Vector (-24.0, 240.0, 7.0)**

-    **CheckBox Axis**: Wenn diese Option markiert ist, wird eine Achse in der angezeigten Koordinate erstellt: **FreeCAD.Vector (-24.0, 240.0, 7.0)**

-    **CheckBox Plane**: Wenn diese Option aktiviert ist, wird eine Achsenebene in der angezeigten Koordinate erstellt: **FreeCAD.Vector (-24.0, 240.0, 7.0)**

-    **Ref**: Die Anzeige der Daten in der Berichtansicht wird aktualisiert

-    **Exit**: Beenden Sie das Makro (Sie müssen über die Schaltfläche der Werkzeugleiste oder über das Menü \"Ansicht → Panels → FCInfo\" einen Neustart durchführen.)

-    **CheckBox****1**: Wenn diese CheckBox markiert ist, werden die Informationen im Berichtansichtsfenster angezeigt

-    **CheckBox****2**: Wenn diese CheckBox nicht markiert ist, wird das Fenstermakro rechts angezeigt (Standard). Wenn diese Option aktiviert ist, wird das Fenstermakro links angezeigt


</div>

Nach dem Starten des Makros bleibt das Makro aktiv und das Fenster bleibt sichtbar. Um das Makro durch Drücken von **Exit** zu verlassen. Wenn Sie das Kreuz verlassen, bleibt das Makro im Speicher und die Daten werden in der \"Berichtansicht\" von FreeCAD angezeigt.


<div class="mw-translate-fuzzy">


<center>

Image:Macro_FCInfo_04.png\|Docked to rigth, Image:Macro FCInfo 05.png\|or left with Combo view and reachable by a tab, or not docked to the choice.


</center>





</div>

## Options


<div class="mw-translate-fuzzy">

## Optionen

### Die verwendete Einheit 

#### Längeneinheit:

km, hm, dam, m, dm, cm, **mm**, µm, nm, pm, fm, inch, link, foot, yard, perch, chain, furlong, mile, league, nautique.


</div>

#### Length unit: 

km, hm, dam, m, dm, cm, **mm**, µm, nm, pm, fm, inch, link, foot, yard, perch, chain, furlong, mile, league, nautique.

#### Angle degrees : 


<div class="mw-translate-fuzzy">

#### Angle degrees : 

1.  **decimal degree**, ex: 174.831872611°
2.  degree minute seconde, ex: 174° 49\' 54.741401\'\'
3.  radian, ex: 3.05139181449 rad
4.  grade, ex: 194.257636235 gon
5.  pourcent ex: 30° = 57.74%


</div>

Kenntnis der Winkel in der FCInfo-Anzeige.


<center>

Image:Macro FCInfo 02.png\|Understanding of angles in FCInfo display Image:Macro FCInfo 03.gif\|Understanding of angles in poucent in FCInfo display
click twice to see the animation (the image must be in full screen)


</center>




#### Weight unit : 


<div class="mw-translate-fuzzy">

#### Weight unit : 

ton, quintal, kg, hg, dag, **gram**, dg, cg, mg, µg, ng, pg, fg, gr (grain), dr (drachm), oz (once), oz t (once troy),
lb t (livre troy), lb (livre av), st (stone), qtr (quarter), cwt (hundredweight), tonneau fr, ct
the \"spinBox\" is set to **7,5** kg, average density of steel. Wenn Sie einen anderen Standardwert wünschen, ändern Sie den Wert der Dichte in Zeile 208


</div>


```python
 global densite       ; densite       = 7.5  # (steel = 7.5 kg par dm3)
```


<div class="mw-translate-fuzzy">

Eine Datei kann mit der Schaltfläche **Save** erstellt werden. Die Datei wird als Datei [csv](https://fr.wikipedia.org/wiki/Comma-separated_values) geschrieben. Auf diese Weise können die Daten in einer Tabelle in untersucht werden FreeCAD or Openoffice, LibreOffice\...


</div>


<div class="mw-translate-fuzzy">

## Skrip

Kopieren Sie den Inhalt des Makros in eine Datei mit dem Namen \"FCInfo.FCMacro\".

-   Windows: Das Formular lautet normalerweise **drive:\\Users\\your_user_name\\AppData\\Roaming\\FreeCAD\\**
-   Ubuntu: Das Formular lautet normalerweise **/home/your_user_name/.FreeCAD**.

Oder direkt in der Oberfläche von FreeCAD
Das Symbol muss sich im selben Verzeichnis wie das Makro befinden.
Laden Sie die Bildpositionierung auf das Symbol herunter <img alt=" 64px" src=images/_FCInfo.png ) ![](images/_FCInfoSpreadsheet.png  style="width:64px;"> und ziehen Sie die Maustaste mit der rechten Maustaste auf \"Speichern unter\" (ändern Sie den Namen nicht).


</div>

Copy the contents of the macro in a file named \"FCInfo.FCMacro\"

-   Windows: the form is usually **\" drive:\\Users\\your_user_name\\AppData\\Roaming\\FreeCAD\\ \"**
-   Ubuntu: the form is usually **\" /home/your_user_name/.FreeCAD \"**.

Or, directly in the interface of FreeCAD
The icon must be in the same directory as the macro.
Download image positioning on the icon <img alt="" src=images/FCInfo.png  style="width:64px;"> <img alt="" src=images/FCInfoSpreadsheet.png  style="width:64px;"> and then drag the mouse right click \"save as\" (do not change the name)


<div class="mw-translate-fuzzy">

**PS: zu lang, um in der Wiki-Seite enthalten zu sein (zur Zeit akzeptieren die Wiki-Seiten nur 64 KB), wurde der Makrocode in das Forum**
gestellt


</div>


<div class="toccolours mw-collapsible mw-collapsed">


<div class="mw-translate-fuzzy">

Es gibt auch FCInfo_Alternate_Linux nur für die FreeCAD-Version 0.13 \... und PyQt4


<div class="mw-collapsible-content">


</div>


<div class="mw-translate-fuzzy">

Es gibt auch eine [Macro_FCInfo_Alternate_Linux](http://www.freecadweb.org/wiki/index.php?title=Macro_FCInfo_Alternate_Linux). Hier wird der Code geändert (aufgrund des Zeichenanzeigefehlers: *\'² ³ °\'* Ordinalzahl nicht im Bereich (128) \"), was bei bestimmten Konfigurationen zu Problemen führte, die Funktionen sind gleich
Beispiel : 
```python
global uniteSs       ; uniteSs       = u"mm²"
global uniteVs       ; uniteVs       = u"mm³"
global uniteAs       ; uniteAs       = u"°"
``` ersetzt durch 
```python
global uniteSs       ; uniteSs       = "mm"+iso8859(unichr(178))
global uniteVs       ; uniteVs       = "mm"+iso8859(unichr(179))
global uniteAs       ; uniteAs       = iso8859(unichr(176))
``` **Dateien, die mit dieser Version gespeichert wurden, sind nicht kompatibel mit der anderen Version (angedockt oder nicht).**


</div>


</div>



</div>

Example : 
```python
global uniteSs       ; uniteSs       = u"mm²"
global uniteVs       ; uniteVs       = u"mm³"
global uniteAs       ; uniteAs       = u"°"
``` remplacés par 
```python
global uniteSs       ; uniteSs       = "mm"+iso8859(unichr(178)) # also:  carre    hex="\xb2"  # also:  html=<span>&#178;</span>
global uniteVs       ; uniteVs       = "mm"+iso8859(unichr(179)) # also:  cube     hex="\xb3"  # also:  html=<span>&#179;</span>
global uniteAs       ; uniteAs       = iso8859(unichr(176))      # also:  degrees  hex="\xb0"  # also:  html=<span>&#176;</span>
                                     = iso8859(unichr(181))      # also:  micro    hex="\xB5"  # also:  html=<span>&#181;</span>
``` **Files saved with this version is incompatible with the other version (docked or not)**


</div>


</div>



<div class="mw-translate-fuzzy">

Laden Sie die Makrodatei in gist herunter **docked to right**


</div>


<div class="mw-translate-fuzzy">


{{CodeDownload|https://gist.github.com/mario52a/8d40ab6c018c2bde678f|last version Macro_FCInfo and the icons at the end of the page}}


</div>


<div class="mw-translate-fuzzy">

(Or **[On the forum.](http://forum.freecadweb.org/viewtopic.php?f=10&t=3185&p=47748#p47748)** )
**PS:** Dieses Makro verwendet **getSelection ()** und die Objektliste beginnt mit 1 Ex: für eine Box **Edge1 bis Edge12** und der Code in der Konsole beginnt bei 0 ex: für eine Box **Edge \[0\] to Edge \[11\]**
Normalerweise beginnt die Zählung von Arrays/Listen in OpenCascade immer bei **1 und nicht bei 0**


</div>

### Limitations


<div class="mw-translate-fuzzy">

### Einschränkungen

Lassen Sie immer die Taste **Exit**. Wenn man das Programm verlässt, ohne die Taste **Exit** zu durchlaufen, bleibt das Programm im Speicher und läuft weiter, und die Anzeige bleibt im \"Bericht anzeigen\". Sie müssen FreeCAD verlassen, um es aus dem Speicher zu löschen.
In der Tabelle sind nur die ersten 200 Elemente des Objekts sichtbar, wenn das Objekt mehr als 200 Elemente enthält, wird ein Signal durch **(! +200)** angezeigt. Die vollständige Datenliste ist in der Datei sichtbar, die mit der Schaltfläche **Save** gespeichert wird.


</div>


<div class="mw-translate-fuzzy">

Wenn das Fenstermakro nach dem Lauf nicht sichtbar ist, siehe das untere Fenster:


</div>

![](images/Macro_FCInfo_08.png )

![](images/FCInfo_begin_00.gif ) 


<div class="mw-translate-fuzzy">

Projekt:
~~lies die Datei direkt in einer Tabelle.~~ done
~~stimmt mit den \"Kanten\" und ihren Koordinaten überein~~ done
Zuordnung eines Stoffes zu seiner Dichte ~~Neigung auf das Element und nicht auf das globale Objekt~~ erledigt
~~Inlay direkt in der Oberfläche von FreeCAD~~ fertig


</div>

## Version


<div class="mw-translate-fuzzy">

-   ver 1.22 , 12/11/2020 : now the macro is totally uninstalled i use :


</div>

-   ver 1.26b 20/02/2022 upgrade for detect BSpline in SubObject

-   ver 1.26 06/02/2022 add info on Mesh and Points objects, decode colours, duplicate object or subObject, memorize the latest path and other preferences options

-   ver 1.25e 18/12/2021 add info detailed to BSpline (ToByArcs) and info \"sel\[0\].TypeId\"
-   ver 1.25d 12/12/2021 \-\--
-   ver 1.25c 12/12/2021 correct \"strAround((\" by \"str(Around(\" and other little \...
-   ver 1.25b 11/12/2021 correction error in change/modify new material and reorganization
-   ver 1.25 10/12/2021 PySide2 and add comboBox materials
-   ver 1.24 02/12/2021 add [adjustedGlobalPlacement](https://forum.freecadweb.org/viewtopic.php?f=22&t=59852) modified by edwilliams16 for placement with Body, boundbox tracing
-   ver 1.23cb 25/11/2021 delete **\"import Sketcher \* \"** create conflict with \"**open(OpenName, \"r\")**\" ??

Adding 
```python
FreeCAD.ActiveDocument.openTransaction(u"FCInfo")    # memorise les actions (avec annuler restore)
FreeCAD.ActiveDocument.commitTransaction()           # restore les actions  (avec annuler restore)
#FreeCAD.ActiveDocument.abortTransaction()            # abandonne les actions(avec annuler restore)
```

-   ver 1.25d, 13/12/2021 little correction material field uncomment the \"\'try\...Except\" !!!
-   ver 1.25c, 12/12/2021 little correction new material
-   ver 1.23b, 20/11/2021 little correction, add text info in beginning run macro, and ordinal the text code
-   ver 1.23 , 19/11/2021 include icon in macro, number decimal displayed, text height, configure options in the Preference FC, correct info for elements of sketch in edit mode.
-   ver 1.22 , 12/11/2020 : now the macro is totally uninstalled i use :


```python
try:
        self.window.setAttribute(QtCore.Qt.WA_DeleteOnClose, True)    # destroy
        self.window.deleteLater()                                     # destroy
        self.window.destroy()                                         # destroy
except Exception:
        None
```

[How do i exit from FreeCAD instead of Python?](https://forum.freecadweb.org/viewtopic.php?f=22&t=48013#p411508)

instead: 
```python
self.window.hide()
``` and i adding the possibility display or not the \"Error Message\" window \"False\" by default, if you wand activate the warning window go to : 
```python
FreeCAD >Menu >Tools >Edit parameters... >BaseApp/Preferences/Macros/FCMmacros/FCInfo > switchWarning
``` currently:
\*ver 1.21-3.01 , 07/11/2019 \# 07/11/2019 ver \"01.21-3-rmu\" replace character micro = \"U\", square = \"2\", cube = \"3\", degrees = \" deg\" see \"<https://forum.freecadweb.org/viewtopic.php?f=3&t=6005&start=70#p345819>\"

-   ver 1.21.01 (1.21-rmu) 30/05/2019 rmu change fixed positions to qt layouts grid.addWidget() by rmu75 see the rmu75 fork \"<https://gist.github.com/rmu75/b165147bd1c2f2659c014103793ae1d8>\"
-   ver 1.20 , 29/01/2018 optimization
-   ver 1.19 , 20/01/2018 create checkBox for use detection all elements of the object if wanted or not , the macro is faster. Optimisation
-   ver 1.18 , 19/12/2017 \...
-   ver 1.17c , 14/12/2017 create plane with coordinate give in one project in other project and replace \"FCInfo\" by \"\_\_title\_\_\"
-   ver 1.17b , 13/12/2017 little correction replace FCTreeView to FCInfo
-   ver 1.17 , 12/12/2017 add upgrade Moment of inertia mm and kg by pinq [FCMacro and moment of inertia of assembly](https://forum.freecadweb.org/viewtopic.php?t=23888), and create plane, axis, point, and add options separator for spreadsheet
-   ver 1.16 , 21/06/2017 add control height police (here PointSize 8) and checkbox for position the window to right or left
-   ver 1.15 , 19/12/2015 suppression PyQt4 option [see](http://forum.freecadweb.org/viewtopic.php?f=12&t=13541) , add checkBox for editing infos in report view
-   ver 1.14 , 04/08/2014 replace PyQt4 and PySide and correct tooltip not displayed cause on PySide and add fg
-   ver 1.13 , 27/07/2014 replace FCInfo_en_Ver_1-12_Docked.FCMacro to FCInfo_en_Ver_1-13_Docked.FCMacro accept PyQt4 and PySide
-   ver 1.12 , 10/03/2014 adding tooltip
-   ver 1.11 , 04/03/2014 adding µm, nm, pm, fm, µg, ng, pg, pourcent, fixed of grandeur carat ~~\"cd\"~~ in **\"ct\"**, display of the label and internal name, fixed calculation of angles XY YZ ZX could give an error on a compound shape, window dockable in FreeCAD
-   ver 1.10.b , 19/11/2013 buttons outside the scrollbar and the dimensions of the window blocking

(ver 1.10 , 18/11/2013 create scrollbar)
\*ver 1.08.b , 10/11/2013 translation units in English, error correction to display the area of the faces listed in the table and replacement of the\"**print**\" by \"**App.Console.PrintMessage**\"
~~ver 1.09 , 04/11/2013 works perfectly on Windows and Linux (cause of errors on Linux the characters : ² ³ ° \"ordinal not in range(128)\")~~
In a Linux distribution and in the case of an error of **\"ordinal not in range (128)\"** an alternative version exists on this page [Macro_FCInfo_Alternate_Linux](Macro_FCInfo_Alternate_Linux.md)
\*ver 1.08 , 24/10/2013 correction of high top \"Faces\" and \"Edges\" displaying 100 objects (in the saved file)
\*ver 1.07 , 11/10/2013 matches the \"Faces\" and their coordinates.
\*ver 1.06 , 22/09/2013 matches the \"Edges\" and their coordinates, inclination on the element rather than the global object
\*ver 1.05 , 17/09/2013 added an icon for the spreadsheet, conversion barrel fr, affichage des dimensions overall instead of coordinates.
\*ver 1.04 , 11/09/2013: read the file directly in a table.
\*ver 1.03 , 09/09/2013: clearer display in view report and replacement by \"typeObject = sel\[0\].Shape.ShapeType\"
\*ver 1.02 , 7/09/2013 : small updates
\*ver 1.00 , 6/09/2013


<div class="mw-translate-fuzzy">

## Verknüpfungen

Siehe auch [Arch Überblick](Arch_Survey/de.md) <img alt="Arch Überblick" src=images/Arch_Survey.svg  style="width:36px;">


</div>

See Also: <img alt="Arch Survey" src=images/Arch_Survey.svg  style="width:36px;"> [Arch Survey](Arch_Survey.md)

Sie können Ihre Kommentare im Forum teilen [Info Workbench - Help with icons please.](http://forum.freecadweb.org/viewtopic.php?f=10&t=3185)
Hier noch ein Beitrag von [FCInfo Macro](http://forum.freecadweb.org/viewtopic.php?f=8&t=6005)



---
![](images/Right_arrow.png) [documentation index](../README.md) > Macro FCInfo/de
