---
- GuiCommand:/it
   Name:Std_SaveAll
   Name/it:Salva tutto
   Empty:1
   MenuLocation:File → Salva tutto
   Workbenches:Tutti
   SeeAlso:[Salva](Std_Save/it.md)
---

# Std SaveAll/it


</div>

## Descrizione

Il comando **Salva tutto** salva tutti i documenti aperti.

## Utilizzo


<div class="mw-translate-fuzzy">

1.  Selezionare l\'opzione **File → Salva tutto** dal menu.
2.  Per i nuovi documenti: immettere un nome file nella finestra di dialogo e premere il pulsante **Salva**.


</div>

## Opzioni

-   Per i nuovi documenti: premere il tasto **Esc** o il pulsante **Annulla** per annullare il comando.

## Preferenze

-   L\'ultima posizione del file utilizzato viene memorizzata in: **Strumenti → Modifica parametri... → BaseApp → Preferences → General → FileOpenSavePath**.

## Script


**Vedere anche:**

[Script di base per FreeCAD](FreeCAD_Scripting_Basics/it.md)

Per salvare un documento, utilizzare il metodo `save` dell\'oggetto documento. Un nuovo documento deve prima essere salvato con il metodo `saveAs` dell\'oggetto documento. Per un esempio di scripting vedere [Nuovo](Std_New/it.md).


<div class="mw-translate-fuzzy">





</div>


{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std SaveAll/it
