---
- GuiCommand:/it
   Name:Draft ToggleConstructionMode
   Name/it:Costruzione
   MenuLocation:Draft → Utilità → Costruzione
   Workbenches:[Draft](Draft_Workbench/it.md), [Architettura](Arch_Workbench/it.md)
   Shortcut:**C** **M**
   SeeAlso:[Aggiungi al gruppo Costruzione](Draft_AddConstruction/it.md)
---

# Draft ToggleConstructionMode/it


</div>

## Descrizione


<div class="mw-translate-fuzzy">

L\'[Ambiente Draft](Draft_Workbench/it.md) <img alt="" src=images/Workbench_Draft.svg  style="width:24px;"> presenta una modalità di costruzione, che consente all\'utente di disegnare forme in uno speciale [Gruppo](Std_Group/it.md), con un colore definito. La geometria di costruzione è composta da linee, punti e altre forme che fungono da riferimenti o [elementi di aggancio](Draft_Snap/it.md) che sono utili per costruire la geometria principale. La geometria della costruzione può essere nascosta (**Visibility** `False`) o cancellata dopo che non è più necessaria.


</div>

<img alt="" src=images/Draft_construction_mode_example.jpg  style="width:400px;">


<div class="mw-translate-fuzzy">



*Geometria di costruzione in blu che aiuta a impostare il centro del cerchio*


</div>

## Utilizzo


<div class="mw-translate-fuzzy">

1.  Premere il pulsante **<img src="images/Draft_ToggleConstructionMode.png" width=16px> [Attiva/disattiva modalità di costruzione](Draft_ToggleConstructionMode/it.md)**.
2.  Disegnare alcuni oggetti.
3.  Premere di nuovo il pulsante **<img src="images/Draft_ToggleConstructionMode.png" width=16px> [Attiva/disattiva modalità di costruzione](Draft_ToggleConstructionMode/it.md)** per tornare alla modalità normale.


</div>

## Notes

-   If Draft construction mode is switched on the active [layer](Draft_Layer.md) is ignored.

## Preferences

-   To change the label of the construction group: **Edit → Preferences... → Draft → General settings → Construction Geometry → Construction group name**.
-   To change the color that is used: **Edit → Preferences... → Draft → General settings → Construction Geometry → Construction geometry color**.



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft ToggleConstructionMode/it
