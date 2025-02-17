---
- GuiCommand:/fr
   Name:Path Drilling
   Name/fr:Path Perçage
   MenuLocation:Path → Perçage
   Workbenches:[Path](Path_Workbench/fr.md)
---

# Path Drilling/fr

## Description

La commande Perçage génère une opération de perçage durant l\'opération.

<img alt="" src=images/Path_Drilling_Sample.png  style="width:400px;"> 
*Ci-dessus: exemple d'opérations de perçage*

## Utilisation

1.  Il existe plusieurs façons de lancer la commande :
    -   Appuyez sur le Button **<img src="images/Path_Drilling.svg" width=16px> [Perçage](Path_Drilling/fr.md)**.
    -   Sélectionnez l\'option **Path → <img src="images/Path_Drilling.svg" width=16px> Perçage** dans le menu.
2.  Dans la section **Opération** :
    -   Sélectionnez un **Contrôleur d'outil**.
    -   Sélectionnez un **Mode de refroidissement**.
    -   En option, activez et ajustez les éléments suivants :
        -   
            **Perçage**
            
            définissez la **Profondeur**.

        -   
            **Temporisation**
            
            définit le **Temps** en secondes.

        -   
            **Profondeur étendue**
            
            .
3.  Dans la section **Géométrie de base**, vérifiez que la liste correspond aux trous destinés à être traités, et ajustez l\'ajout, l\'activation ou la désactivation, si nécessaire. Les trous peuvent être ajoutés en sélectionnant les faces des murs des Trous.
4.  Dans la section **Profondeurs**, vérifiez et ajustez si nécessaire les **Profondeur initiale** et **Profondeur finale**.
5.  Dans la section **Hauteurs**, vérifiez et, si nécessaire, ajustez les **Hauteur de sécurité** et **Hauteur de dégagement**.
6.  Appuyez sur le bouton **OK** pour générer le(s) chemin(s) de perçage.

## Remarques

-   Lorsque vous utilisez des arêtes pour la géométrie de base, sélectionnez toujours le bord inférieur du trou.
-   Vérifiez toujours que l\'outil choisi est le bon diamètre pour le(s) trou(s) sélectionné(s).
-   **Perçage désactivé** génère (cycles de forage pré-programmés G81). **Perçage activé** génère (cycles de forage prédéfinis G83).
-   **Temporisation activé** est actuellement non pris en charge, mais il est destiné à générer (cycles de forage fixes G82).

## Propriétés

***Remarque***: toutes ces propriétés ne sont pas disponibles dans l\'éditeur de fenêtre de tâches. Certaines ne sont accessibles que dans l\'onglet Données du panneau Vue de propriétés pour cette opération.


{{TitleProperty|Base}}

Remarque: il est conseillé de ne pas modifier la propriété Placement des opérations de chemin. Déplacez ou faites pivoter le modèle de tâche de chemin selon vos besoins.

-    **Placement**: emplacement global \[position et rotation\] de l\'objet - par rapport à l\'origine (ou à l\'origine du conteneur de l\'objet parent).

    -   
        **Angle**
        
        : angle en degrés appliqué à la rotation de l\'objet autour de la valeur de la propriété Axis.

    -   
        **Axis**
        
        : axe (un ou plusieurs) autour duquel faire pivoter l\'objet, défini dans les sous-propriétés: x, y, z.

        -   
            **X**
            
            : valeur de l\'axe x.

        -   
            **Y**
            
            : valeur de l\'axe y.

        -   
            **Z**
            
            : valeur de l\'axe z.

    -   
        **Position**
        
        : position de l\'objet, définie dans les sous-propriétés: x, y, z - par rapport à l\'origine (ou à l\'origine du conteneur de l\'objet parent).

        -   
            **X**
            
            : valeur de distance x.

        -   
            **Y**
            
            : valeur de distance y.

        -   
            **Z**
            
            : valeur de distance z.

-    **Label**: nom de l\'objet fourni par l\'utilisateur (UTF-8).

-    **Disabled**: liste des fonctionnalités désactivées.


{{TitleProperty|Depth}}

-    **Clearance Height**: hauteur nécessaire pour éviter les brides et les obstructions.

-    **Final Depth**: profondeur finale de l\'outil - valeur la plus basse de Z.

-    **Safe Height**: hauteur au-dessus de laquelle les mouvements rapides sont autorisés. (Hauteur de sécurité rapide entre les sites).

-    **Start Depth**: profondeur initiale de l\'outil - *profondeur de la première coupe en Z*.


{{TitleProperty|Drill}}

-    **Add Tip Length**: calcule la longueur de la pointe et la soustrait de la profondeur finale.

-    **Dwell Enabled**: active la temporisation.

-    **Dwell Time**: le temps de pause entre les cycles de perçage.

-    **Peck Depth**: profondeur de perçage incrémental avant de se rétracter pour nettoyer les copeaux.

-    **Peck Enabled**: active le perçage.

-    **Retract Height**: hauteur à laquelle commence l\'avance de l\'outil et la hauteur pendant laquelle l\'outil est rétracté lorsque la trajectoire est terminée.

-    **Return Level**: contrôle le retrait de l\'outil. Par défaut = G98.


{{TitleProperty|Path}}

-    **Active**: mis à False, pour empêcher l\'opération de générer du code.

-    **Comment**: commentaire facultatif pour cette opération.

-    **User Label**: identifiant attribuée par l\'utilisateur.

-    **Tool Controller**: définit le contrôleur d\'outil utilisé dans l\'opération.


{{TitleProperty|Rotation}}

(*si disponible*)

-    **Attempt Inverse Angle**: tente automatiquement l\'angle inverse si la rotation initiale est incorrecte.

-
-    **Enable Rotation**: active la rotation pour accéder aux trous non normaux sur l\'axe Z.

-    **Angle Inverse**: inverse l\'angle de la rotation. ***Exemple :** change une rotation de -22,5 à 22,5 degrés.*

-    **Reverse Direction**: inverse l\'orientation de l\'opération de 180 degrés.

## Disposition de l\'éditeur de fenêtre de tâches 

*Les descriptions des paramètres sont fournies dans la liste des propriétés ci-dessus.*

Cette section est simplement une représentation des paramètres de l'éditeur de fenêtres pour l'opération.

### Géométrie de base 

-   **Ajouter** : ajoute le(s) élément(s) sélectionné(s) qui doit(vent) être la(les) base(s) pour le(s) trajectoire(s).
-   **Enlever** : supprime le ou les éléments sélectionnés dans la liste de la géométrie de base.
-   **Réinitialiser** : efface tous les éléments de la liste de la géométrie de base.

### Emplacement de base 

-   **Ajouter** : ajoute un emplacement de coordonnées (X, Y) à l\'opération de forage en cours.
-   **Enlever** : supprime le(s) élément(s) de localisation sélectionné(s) de la liste de Emplacement de base.
-   **Éditer** : modifie l\'élément l\'emplacement sélectionné.

### Profondeurs

-   **Profondeur initiale** :
-   **Profondeur finale** :

### Hauteurs

-   **Hauteur de sécurité** :
-   **Hauteur de dégagement** :

### Opération

-   **Contrôleur d\'outil** :
-   **Hauteur de rétraction** :
-   **Perçage** :
-   **Profondeur de perçage** :
-   **Temporisation** :
-   **Temps de temporisation** :
-   **Longueur de la pointe utilisée** :

## Script


**Voir aussi:**

[FreeCAD Script de base](FreeCAD_Scripting_Basics/fr.md).

Exemple :


```python
#Place code example here.
```





{{Path_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Path](Path_Workbench.md) > Path Drilling/fr
