---
- GuiCommand:/fr
   Name:TechDraw ProjectShape
   Name/fr:TechDraw Projection de forme
   MenuLocation:TechDraw → Projeter la forme...
   Workbenches:[TechDraw](TechDraw_Workbench/fr.md)
   Shortcut:
   Version:0.20
   SeeAlso:[Draft Shape2DView](Draft_Shape2DView/fr.md)
---

# TechDraw ProjectShape/fr

## Description

L\'outil <img alt="" src=images/TechDraw_ProjectShape.svg  style="width:24px;"> **TechDraw Projection de forme** crée des projections de formes. Les projections sont créées dans la [Vue 3D](3D_view/fr.md) et non sur une [TechDraw Page](TechDraw_PageDefault/fr.md).

![](images/ProjectShape1_it.png )

## Utilisation

1.  Sélectionnez un ou plusieurs objets. Une projection distincte sera créée pour chaque objet.
2.  Il existe plusieurs façons de lancer l\'outil :
    -   Appuyez sur le **<img src="images/TechDraw_ProjectShape.svg" width=16px> [Projeter la forme...](TechDraw_ProjectShape/fr.md)** bouton.
    -   Sélectionnez l\'option **TechDraw → <img src="images/TechDraw_ProjectShape.svg" width=16px> Projeter la forme...** dans le menu.
3.  Le panneau de tâches **Projeter les formes** s\'ouvre. Voir [Propriétés](#Propri.C3.A9t.C3.A9s.md).
4.  Définissez les options souhaitées.
5.  Les options sélectionnées ne doivent pas donner lieu à une projection vide, car cela entraînerait une erreur. Par exemple, pour un objet ne comportant que des arêtes vives, comme un [Part Cube](Part_Box/fr.md), l\'option **Arêtes vives visibles** et/ou **Arêtes vives masquées** doit être cochée.
6.  Appuyez sur le bouton **OK**.

## Propriétés

Un objet Projection est dérivé d\'un [Part Feature](Part_Feature/fr.md) et hérite de toutes ses propriétés. Il possède également les propriétés supplémentaires suivantes :

### Données


{{TitleProperty|Projection}}

-    **Source|Link**: la forme à projeter.

-    **Direction|Vector**: direction de la projection. Il s\'agit du vecteur normal du plan de projection.

-    **VCompound|Bool**: si `True`, les arêtes vives visibles sont affichées. Exemple : tous les arêtes d\'un [Part Cube](Part_Box/fr.md).

-    **Rg1 Line VCompound|Bool**: si `True`, les arêtes lisses visibles sont affichés. Exemple : les arêtes entre un congé et ses faces adjacentes.

-    **Rg NLine VCompound|Bool**: si `True`, les arêtes cousues visibles sont affichés. Exemple : la couture d\'une face cylindrique de 360°.

-    **Out Line VCompound|Bool**: si `True`, les arêtes de contour visibles (qui ne sont pas nettes) sont affichées. Exemple : la vue latérale d\'un [Part Cylindre](Part_Cylinder/fr.md) présente deux de ces bords.

-    **Iso Line VCompound|Bool**: si `True`, les isoparamètres visibles sont affichés. Ne fonctionne pas actuellement.

-    **HCompound|Bool**: si `True`, les arêtes vives cachées sont affichées.

-    **Rg1 Line HCompound|Bool**: si `True`, les arêtes lisses cachées sont affichés.

-    **Rg NLine HCompound|Bool**: si `True`, les arêtes cousues cachées sont affichés.

-    **Out Line HCompound|Bool**: si `True`, les arêtes cachées du contour sont affichés.

-    **Iso Line HCompound|Bool**: si `True`, les isoparamètres cachés sont affichés. Ne fonctionne pas actuellement.

## Remarques

Cet outil était auparavant disponible dans l\'atelier Drawing.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw ProjectShape/fr
