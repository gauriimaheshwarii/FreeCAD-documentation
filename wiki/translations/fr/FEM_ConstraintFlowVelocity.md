---
- GuiCommand:/fr
   Name:FEM ConstraintFlowVelocity
   Name/fr:FEM Contrainte de vitesse d'écoulement
   MenuLocation:Modèle → Contraintes du fluide → Contrainte de vitesse d'écoulement
   Workbenches:[FEM](FEM_Workbench/fr.md)
   SeeAlso:[FEM Contrainte vitesse d'écoulement initiale](FEM_ConstraintInitialFlowVelocity/fr.md)
---

# FEM ConstraintFlowVelocity/fr

## Description

Applique une vitesse d\'écoulement comme condition limite à un bord en 2D ou à une face en 3D.

<img alt="" src=images/FEM-constraint-flow-velocity_task-panel.png  style="width:400px;"> 
*Menus des contraintes de vitesse d'écoulement dans le [Panneau des tâches](Task_panel/fr.md)*

## Utilisation

1.  Il existe plusieurs façons d\'appeler la commande:
    -   Appuyez sur le bouton **<img src="images/FEM_ConstraintFlowVelocity.svg" width=16px> [Contrainte de vitesse d'écoulement](FEM_ConstraintFlowVelocity/fr.md)**.
    -   Sélectionnez l\'option **Modèle → Contraintes du fluide → <img src="images/FEM_ConstraintFlowVelocity.svg" width=16px> Contrainte de vitesse d'écoulement** dans le menu.
2.  Le [Panneau des tâches](Task_panel/fr.md) affichera des menus pour la contrainte de vitesse d\'écoulement
3.  Sélectionnez les arêtes cibles ou faces cibles.
4.  Appuyez sur le bouton **Ajouter**.
5.  Désélectionnez \"unspecified\" pour activer les champs nécessaires à l\'édition.
6.  Renseignez les valeurs en mm/s pour les principales composantes cartésiennes.

## Remarques

-   Les composants vectoriels cochés comme \"unspecified\" (non spécifiés) seront interpolés par le solveur sélectionné.

    :   Tout vecteur qui devrait être le résultat du solveur doit être coché comme \"unspecified\".
-   Si la face ou l\'arête cible n\'est pas alignée avec le système de coordonnées cartésiennes principal, il est possible de cocher \"normal to boundary\".

    :   Si \"normal to boundary\" est coché, le vecteur normal au bord ou à la face sélectionné est X et il sera orienté loin du domaine du maillage.
    :   Par exemple, si un flux de 20 mm/s d\'air doit entrer dans le domaine, après avoir coché \"normal à la limite\", l\'utilisateur devra entrer -20 mm/s dans le champ \"velocity X\".

-   Pour une paroi avec une condition adhérente, le débit sera de (0,0,0)
-   Pour une condition de symétrie, l\'écoulement sera (0, Unspecified, Unspecified) si \"normal to boundary\" est coché.





{{FEM Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM ConstraintFlowVelocity/fr
