---
- GuiCommand:/it
   Name:FEM_ConstraintDisplacement
   Name/it:Vincolo di dislocamento
   MenuLocation:Modello → Vincoli meccanici → Vincolo dislocamento
   Workbenches:[FEM](FEM_Workbench/it.md)
   Shortcut:
   SeeAlso:[Tutorial di FEM](FEM_tutorial/it.md)
---

# FEM ConstraintDisplacement/it


</div>

## Descrizione

Crea un vincolo FEM per un determinato dislocamento di un oggetto selezionato per un dato grado di libertà.

## Utilizzo


<div class="mw-translate-fuzzy">

1.  Cliccare su <img alt="" src=images/FEM_ConstraintDisplacement.png  style="width:32px;"> o scegliere **Modello** → **Vincoli meccanici** → **<img src="images/FEM_ConstraintDisplacement.png" width=32px> Vincolo dislocamento** dal menu principale.
2.  Selezionare nella vista 3D l\'oggetto a cui deve essere applicato il vincolo, che può essere
    1.  vertice (angolo)
    2.  bordo
    3.  faccia
3.  Scegliere un grado di libertà e prescrivere uno spostamento.


</div>

## Note


<div class="mw-translate-fuzzy">

1.  Il vincolo utilizza \*BOUNDARY card in CalculiX. Come stabilire un grado di libertà è spiegato in <http://web.mit.edu/calculix_v2.7/CalculiX/ccx_2.7/doc/ccx/node164.html> e prescrivere uno dislocamento per un grado di libertà è spiegato in <http://web.mit.edu/calculix_v2.7/CalculiX/ccx_2.7/doc/ccx/node165.html>


</div>


<div class="mw-translate-fuzzy">





</div>


{{FEM Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM ConstraintDisplacement/it
