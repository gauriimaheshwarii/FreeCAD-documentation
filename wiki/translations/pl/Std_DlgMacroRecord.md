---
- GuiCommand:/pl
   Name:Std DlgMacroRecord
   Name/pl:Std: Rejestrator makrodefinicji 
   MenuLocation:Makrodefinicje → Rejestrator makrodefinicji ...
   Workbenches:wszystkie
   SeeAlso:[Zatrzymaj nagrywanie makra](Std_MacroStopRecord/pl.md)
---

# Std DlgMacroRecord/pl



## Opis

Polecenie **Rejestrator makrodefinicji** uruchamia sesję nagrywania [makrodefinicji](Macros/pl.md), podczas której działania użytkownika są zapisywane w makrze FreeCAD, pliku z rozszerzeniem **.FCMacro**. Makrodefinicja może być później odtworzona, wykonana, w celu powtórzenia zarejestrowanych działań.

![](images/Std_DlgMacroRecord_dialog.png ) 
*Okienko dialogowe Rejestrator makrodefinicji*



## Użycie

1.  Istnieje kilka sposobów na wywołanie polecenia:
    -   Naciśnij przycisk **<img src="images/Std_DlgMacroRecord.svg" width=16px> [Rejestrator makrodefinicji ...](Std_DlgMacroRecord/pl.md)**.
    -   Wybierz z menu opcję **Makrodefinicje → <img src="images/Std_DlgMacroRecord.svg" width=16px> Rejestrator makrodefinicji ...**.
2.  Otwiera się okno dialogowe Rejestrator makrodefinicji.
3.  Wprowadź nazwę dla makra w polu wejściowym **Nazwa makrodefinicji**.
4.  Opcjonalnie zmień **ścieżkę do pliku makrodefinicji**, naciskając przycisk **...**.
5.  Przycisk **Stop** nie działa w tej chwili.
6.  Naciśnij przycisk **Nagrywanie**, aby zamknąć okno dialogowe i rozpocząć sesję nagrywania.
7.  Wykonaj czynności, które chcesz nagrać.
8.  Aby zakończyć sesję nagrywania wykonaj jedną z następujących czynności:
    -   Naciśnij przycisk **<img src="images/Std_MacroStopRecord.svg" width=16px> [Zatrzymaj nagrywanie makra](Std_MacroStopRecord/pl.md)**.
    -   Wybierz z menu opcję **Makrodefinicje → <img src="images/Std_MacroStopRecord.svg" width=16px> Zatrzymaj nagrywanie makra**.



## Opcje

-   Po wyświetleniu okna dialogowego Rejestrator makrodefinicji: naciśnij przycisk **Esc** lub **Anuluj**, aby przerwać wykonywanie polecenia.



## Uwagi

-   Aby wykonać nagraną makrodefinicję należy użyć polecenia [Wykonaj makro](Std_DlgMacroExecute/pl.md).
-   Aby dowiedzieć się więcej o makrach zobacz stronę [Makrodefinicje](Macros/pl.md).



## Ustawienia

-   Ścieżkę do makrodefinicji można również zmienić w preferencjach: **Edycja → Preferencje ... → Ogólne → Makropolecenia → Ścieżka do plików makrodefinicji**. Patrz [Edytor ustawień](Preferences_Editor/pl#Makropolecenia.md)
-   W większości przypadków niepożądane jest rejestrowanie akcji, które nie zmieniają modelu: pod **Edycja → Preferencje ... → Ogólne → Makropolecenia → Polecenia GUI** wykonaj jedną z następujących czynności:
    -   Aby wykluczyć te działania odznacz pole wyboru {{CheckBox|FALSE|Nagrywanie poleceń GUI}}.
    -   Aby uwzględnić je tylko jako komentarze zaznacz oba pola wyboru {{CheckBox|TRUE|Nagrywanie poleceń GUI}} i {{CheckBox|TRUE|Zarejestruj jako komentarz}}.





{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std DlgMacroRecord/pl
