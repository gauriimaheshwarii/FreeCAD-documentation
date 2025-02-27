# <img alt="Icône de l\'atelier externe Fasteners" src=images/Fasteners_workbench_icon.svg  style="width:64px;"> Fasteners Workbench/fr


{{TOCright}}

## Introduction

L\'<img alt="" src=images/Fasteners_workbench_icon.svg  style="width:24px;"> [atelier Fasteners](Fasteners_Workbench/fr.md) est un [atelier externe](External_workbenches/fr.md) qui permet d\'ajouter diverses fixations aux pièces.

![](images/Fasteners_toolbars.png ) 
*La barre d'outils unique optionnelle de l'atelier.<br>
Les fixations à dimensions métriques ont des icônes orange.<br>
Les fixations dont les dimensions sont en pouces ont des icônes vertes.*

## Installation

1.  Installez l\'atelier Fasteners via le <img alt="" src=images/AddonManager.svg  style="width:24px;"> [Gestionnaire des extensions](Std_AddonMgr/fr.md). Pour une installation manuelle, voir [Installer des ateliers supplémentaires](Installing_more_workbenches/fr.md).
2.  Redémarrez FreeCAD.
3.  Créez un nouveau document.
4.  Sélectionnez l\'<img alt="" src=images/Fasteners_workbench_icon.svg  style="width:24px;"> [atelier Fasteners](Fasteners_Workbench/fr.md) dans la [liste déroulante des ateliers](Std_Workbench/fr.md).
5.  En option, vous pouvez modifier la barre d\'outils et la disposition du menu :
    1.  Allez à : **Edition → Préférences... → Fasteners → General settings → Toolbar screw icons grouping**..
    2.  Sélectionnez l\'une des options disponibles :
        -   
            **None**
            
            : toutes les fixations apparaissent dans une seule barre d\'outils. Pour voir tous les boutons disponibles, utilisez le bouton **&gt;&gt;** pour la développer.

        -   
            **Separate toolbars**
            
            : les fixations sont regroupées dans plusieurs barres d\'outils. Il s\'agit de la disposition par défaut.

        -   
            **Dropdown buttons**
            
            : les fixations sont regroupées dans des barres d\'outils avec des boutons déroulants.
    3.  Redémarrez FreeCAD.

## Utilisation

Les fixations peuvent être attachées ou non attachées. Les fixations attachées ont une **base Object**, un bord circulaire, et leur **Placement** est dynamiquement lié à cet objet. La commande <img alt="" src=images/Fasteners_Move.svg  style="width:16px;"> [Fasteners Move](Fasteners_Move/fr.md) peut être utilisée pour fixer ou détacher une fixation.

### Fixations non attachées 

1.  Sélectionnez la fixation souhaitée en cliquant sur son bouton ou en la choisissant dans le menu.
2.  Une fixation est créée à l\'origine.
3.  Vous pouvez modifier les dimensions et les autres propriétés de la fixation :
    1.  Sélectionnez la fixation.
    2.  Allez dans l\'onglet **Data** de l\'[Éditeur de propriétés](Property_editor/fr.md).
    3.  Modifiez les propriétés requises.

### Fixations attachées 

<img alt="" src=images/Fasteners_Attached_Selected.png  style="width:200px;"> <img alt="" src=images/Fasteners_Attached_Created.png  style="width:200px;"> 
*À gauche, deux bords circulaires sélectionnés. À droite, les fixations attachées.*

1.  Spécifiez si les trous sélectionnés sont des trous de taraudage ou des trous de passage en sélectionnant <img alt="" src=images/Fasteners_MatchTypeInner.svg  style="width:16px;"> [Fasteners MatchTypeInner](Fasteners_MatchTypeInner/fr.md) ou <img alt="" src=images/Fasteners_MatchTypeOuter.svg  style="width:16px;"> [Fasteners MatchTypeOuter](Fasteners_MatchTypeOuter/fr.md) respectivement (non utilisé pour les vis à tête fraisée).
2.  Sélectionnez une ou plusieurs arêtes circulaires et/ou faces avec des arêtes circulaires. Pour les vis fraisées, le bord supérieur du [trou chanfreiné](Fasteners_ChamferHole/fr.md) doit être sélectionné.
3.  Sélectionnez la fixation souhaitée en cliquant sur son bouton ou en la choisissant dans le menu.
4.  Une fixation est attachée à chacun des bords circulaires sélectionnés.
5.  Les dimensions par défaut de chaque fixation dépendent du rayon du bord circulaire sur lequel elle est fixée. Les vis à tête fraisée sont assorties au diamètre de leur tête, les autres fixations sont assorties au diamètre de leur tige.
6.  Vous pouvez également modifier les dimensions et les autres propriétés des fixations. Voir ci-dessus.
7.  Les fixations qui apparaissent à l\'envers peuvent être inversées avec la commande <img alt="" src=images/Fasteners_Flip.svg  style="width:16px;"> [Fasteners Flip](Fasteners_Flip/fr.md) ou en modifiant leur propriété **invert**.
8.  Changez éventuellement la propriété **offset** pour créer un espace entre les fixations et les bords auxquels elles sont attachées.

## Remarques

-   Pour générer des filetages, la propriété **thread** d\'une fixation doit être changée en `True`. La génération de filetages est coûteuse. Les recalculs prennent beaucoup plus de temps s\'il y a beaucoup de fixations avec des filetages dans un document.
-   La propriété **invert** et la propriété **offset** sont ignorées pour les fixations non attachées.

## Commandes

-   <img alt="" src=images/Fasteners_Flip.svg  style="width:32px;"> [Invert fastener](Fasteners_Flip/fr.md) : inverse l\'orientation des fixations attachées.

-   <img alt="" src=images/Fasteners_Move.svg  style="width:32px;"> [Move fastener](Fasteners_Move/fr.md) : déplace et fixe une fixation sur un bord circulaire. Peut également être utilisé pour détacher une fixation.

-   <img alt="" src=images/Fasteners_Shape.svg  style="width:32px;"> [Simplify shape](Fasteners_Shape/fr.md) : crée des copies non paramétriques des fixations.

-   <img alt="" src=images/Fasteners_MatchTypeInner.svg  style="width:32px;"> [Match for tap hole](Fasteners_MatchTypeInner/fr.md) : prend les bords circulaires comme des trous à fileter lorsque de nouvelles fixations y sont attachées.

-   <img alt="" src=images/Fasteners_MatchTypeOuter.svg  style="width:32px;"> [Match for pass hole](Fasteners_MatchTypeOuter/fr.md) : prend les bords circulaires comme des trous de passage lorsque de nouvelles fixations y sont attachées.

-   <img alt="" src=images/Fasteners_BOM.svg  style="width:32px;"> [Generate BOM](Fasteners_BOM/fr.md) : crée une feuille de calcul avec une nomenclature pour les fixations du document.

-   <img alt="" src=images/Fasteners_ScrewCalculator.svg  style="width:32px;"> [Screw calculator](Fasteners_ScrewCalculator/fr.md) : affiche une calculatrice pour déterminer la taille des trous de vis.

-   <img alt="" src=images/Fasteners_ChamferHole.svg  style="width:32px;"> [Make countersunk](Fasteners_ChamferHole/fr.md) : chanfreine les trous pour les vis à tête fraisée.

-   <img alt="" src=images/Fasteners_ChangeParameters.svg  style="width:32px;"> [Change fastener parameters](Fasteners_ChangeParameters/fr.md) : change les paramètres des fixations.

## Fixations

Les fixations avec des dimensions métriques ont des icônes orange. Les fixations aux dimensions en pouces ont des icônes vertes.

#### Fixations autobloquantes et fixations pour PCB 

-   <img alt="" src=images/Fasteners_PEMPressNut.svg  style="width:32px;"> Ecrou autobloquant.

-   <img alt="" src=images/Fasteners_PEMTHStandoff.svg  style="width:32px;"> Fixation autobloquante.

-   <img alt="" src=images/Fasteners_PEMStud.svg  style="width:32px;"> Goujon autobloquant.

-   <img alt="" src=images/Fasteners_PCBStandoff.svg  style="width:32px;"> Support de PCB femelle/mâle.

-   <img alt="" src=images/Fasteners_PCBSpacer.svg  style="width:32px;"> Entretoise de PCB femelle/femelle.

-   <img alt="" src=images/Fasteners_IUTHeatInsert.svg  style="width:32px;"> Insert pour piquage à chaud.

### Vis et boulons à tête hexagonale 

-   <img alt="" src=images/Fasteners_ISO4017.svg  style="width:32px;"> 
**ISO 4017** Vis à tête hexagonale. *Catégories de produits A et B.*

-   <img alt="" src=images/Fasteners_ISO4014.svg  style="width:32px;"> 
**ISO 4014** Boulon à tête hexagonale. *Catégories de produits A et B.*

-   <img alt="" src=images/Fasteners_EN1662.svg  style="width:32px;"> **EN 1662** Boulon à tête hexagonale avec embase, série étroite.

-   <img alt="" src=images/Fasteners_EN1665.svg  style="width:32px;"> **EN 1665** Boulon à tête hexagonale avec embase, série large.

-   <img alt="" src=images/Fasteners_DIN571.svg  style="width:32px;"> **DIN 571** Tirefond vis à bois à tête hexagonale.

-   <img alt="" src=images/Fasteners_ASMEB18.2.1.6.svg  style="width:32px;"> **ASME B18.2.1.6** Vis à tête hexagonale UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.2.1.8.svg  style="width:32px;"> **ASME B18.2.1.8** Vis à tête hexagonale UNC avec bride.

### Vis à six pans creux 

-   <img alt="" src=images/Fasteners_ISO4762.svg  style="width:32px;"> **ISO 4762** Vis à tête cylindrique à six pans creux.

-   <img alt="" src=images/Fasteners_DIN7984.svg  style="width:32px;"> **DIN 7984** Vis à tête cylindrique à six pans creux à tête basse.

-   <img alt="" src=images/Fasteners_DIN6912.svg  style="width:32px;"> **DIN 6912** Vis à tête cylindrique à six pans creux à tête basse avec téton de sécurité.

-   <img alt="" src=images/Fasteners_ISO7380-1.svg  style="width:32px;"> **ISO 7380-1** Vis à tête ronde à six pans creux.

-   <img alt="" src=images/Fasteners_ISO7380-2.svg  style="width:32px;"> **ISO 7380-2** Vis à tête ronde à six pans creux avec embase.

-   <img alt="" src=images/Fasteners_ISO10642.svg  style="width:32px;"> **ISO 10642** Vis à tête fraisée à six pans creux.

-   <img alt="" src=images/Fasteners_ISO7379.svg  style="width:32px;"> **ISO 7379** Vis à épaulement à tête creuse hexagonale.

-   <img alt="" src=images/Fasteners_ISO4026.svg  style="width:32px;"> **ISO 4026** Vis sans tête à six pans creux à bout plat.

-   <img alt="" src=images/Fasteners_ISO4027.svg  style="width:32px;"> **ISO 4027** Vis sans tête à six pans creux à bout tronconique.

-   <img alt="" src=images/Fasteners_ISO4028.svg  style="width:32px;"> **ISO 4028** Vis sans tête à six pans creux à téton cylindrique.

-   <img alt="" src=images/Fasteners_ISO4029.svg  style="width:32px;"> **ISO 4029** Vis sans tête à six pans creux à bout cuvette.

-   <img alt="" src=images/Fasteners_ASMEB18.3.1A.svg  style="width:32px;"> **ASME B18.3.1A** Vis à tête cylindrique à six pans creux UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.3.1G.svg  style="width:32px;"> **ASME B18.3.1G** Vis à tête cylindrique à six pans creux UNC à tête basse.

-   <img alt="" src=images/Fasteners_ASMEB18.3.2.svg  style="width:32px;"> **ASME B18.3.2** Vis à tête fraisée à six pans creux UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.3.3A.svg  style="width:32px;"> **ASME B18.3.3A** Vis à tête ronde à six pans creux UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.3.3B.svg  style="width:32px;"> **ASME B18.3.3B** Vis à tête ronde à six pans creux UNC avec bride.

-   <img alt="" src=images/Fasteners_ASMEB18.3.4.svg  style="width:32px;"> **ASME B18.3.4** Vis à épaulement à tête creuse hexagonale UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.3.5A.svg  style="width:32px;"> **ASME B18.3.5A** Vis à tête hexagonale UNC à bout plat.

-   <img alt="" src=images/Fasteners_ASMEB18.3.5B.svg  style="width:32px;"> **ASME B18.3.5B** Vis à tête hexagonale UNC à bout tronconique.

-   <img alt="" src=images/Fasteners_ASMEB18.3.5C.svg  style="width:32px;"> **ASME B18.3.5C** Vis sans tête à six pans creux UNC à téton.

-   <img alt="" src=images/Fasteners_ASMEB18.3.5D.svg  style="width:32px;"> **ASME B18.3.5D** Vis à tête hexagonale UNC à bout cuvette.

### Vis à tête creuse hexalobulaire 

-   <img alt="" src=images/Fasteners_ISO14579.svg  style="width:32px;"> **ISO 14579** Vis à tête cylindrique à six pans creux.

-   <img alt="" src=images/Fasteners_ISO14580.svg  style="width:32px;"> **ISO 14580**Vis à tête cylindrique à six pans creux.

-   <img alt="" src=images/Fasteners_ISO14582.svg  style="width:32px;"> **ISO 14582** Vis à tête fraisée à six pans creux, tête haute.

-   <img alt="" src=images/Fasteners_ISO14583.svg  style="width:32px;"> **ISO 14583** Vis à tête cylindrique à six pans creux.

-   <img alt="" src=images/Fasteners_ISO14584.svg  style="width:32px;"> **ISO 14584** Vis à tête fraisée à six pans creux.

### Vis à tête fendue 

-   <img alt="" src=images/Fasteners_ISO2009.svg  style="width:32px;"> **ISO 2009** Vis à tête plate fendue et fraisée. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_ISO2010.svg  style="width:32px;"> **ISO 2010** Vis à tête fraisée surélevée fendue. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_ISO1580.svg  style="width:32px;"> **ISO 1580** Vis à tête cylindrique fendue. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_ISO1207.svg  style="width:32px;"> **ISO 1207** Vis à tête cylindrique fendue. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_DIN96.svg  style="width:32px;"> **DIN 96** Vis à bois à tête demi-ronde fendue.

-   <img alt="" src=images/Fasteners_GOST1144-1.svg  style="width:32px;"> **GOST 1144-1** Vis à bois à tête demi-ronde fendue.

-   <img alt="" src=images/Fasteners_GOST1144-2.svg  style="width:32px;"> **GOST 1144-2** Vis à bois à tête demi-ronde fendue.

-   <img alt="" src=images/Fasteners_ASMEB18.6.3.1A.svg  style="width:32px;"> **ASME B18.6.3.1A** Vis à tête plate fendue et fraisée UNC.

### Vis type H à tête cruciforme 

-   <img alt="" src=images/Fasteners_DIN967.svg  style="width:32px;"> **DIN 967** Vis à tête cylindrique à empreinte cruciforme avec embase.

-   <img alt="" src=images/Fasteners_ISO7045.svg  style="width:32px;"> 
**ISO 7045** Vis à tête cylindrique bombée type H à empreinte cruciforme. *Grade du produit A.*

-   <img alt="" src=images/Fasteners_ISO7046.svg  style="width:32px;"> 
**ISO 7046** Vis à tête plate fraisée à empreinte cruciforme. *Grade du produit A.*

-   <img alt="" src=images/Fasteners_ISO7047.svg  style="width:32px;"> 
**ISO 7047** Vis à tête fraisée surélevée à empreinte cruciforme. *Grade du produit A.*

-   <img alt="" src=images/Fasteners_ISO7048.svg  style="width:32px;"> **ISO 7048** Vis à tête cylindrique avec évidement transversal de type H.

-   <img alt="" src=images/Fasteners_GOST1144-3.svg  style="width:32px;"> **GOST 1144-3** Vis à bois à tête demi-ronde avec empreinte en croix de type H.

-   <img alt="" src=images/Fasteners_GOST1144-4.svg  style="width:32px;"> **GOST 1144-4** Vis à bois à tête demi-ronde avec empreinte en croix de type H.

### Autres têtes de boulon 

-   <img alt="" src=images/Fasteners_DIN603.svg  style="width:32px;"> **DIN 603** Boulon à tête carrée - boulon de carrosserie.

-   <img alt="" src=images/Fasteners_ASMEB18.5.2.svg  style="width:32px;"> **ASME B18.5** Boulon à tête carrée - boulon de carrosserie.

### Écrous

-   <img alt="" src=images/Fasteners_ISO4032.svg  style="width:32px;"> 
**ISO 4032** Écrou hexagonal, style 1. *Catégories de produits A et B.*

-   <img alt="" src=images/Fasteners_ISO4033.svg  style="width:32px;"> 
**ISO 4033** Écrou hexagonal, style 2. *Catégories de produits A et B.*

-   <img alt="" src=images/Fasteners_ISO4035.svg  style="width:32px;"> 
**ISO 4035** Écrou mince hexagonal, chanfreiné. *Catégories de produits A et B.*

-   <img alt="" src=images/Fasteners_EN1661.svg  style="width:32px;"> **EN 1661** Écrou hexagonal avec embase.

-   <img alt="" src=images/Fasteners_DIN917.svg  style="width:32px;"> **DIN 917** Écrou borgne, forme basse.

-   <img alt="" src=images/Fasteners_DIN1587.svg  style="width:32px;"> **DIN 1587** Écrou borgne.

-   <img alt="" src=images/Fasteners_GOST11860-1.svg  style="width:32px;"> **GOST 11860-1** Écrou borgne.

-   <img alt="" src=images/Fasteners_DIN557.svg  style="width:32px;"> **DIN 557** Écrou carré.

-   <img alt="" src=images/Fasteners_DIN562.svg  style="width:32px;"> **DIN 562** Écrou carré.

-   <img alt="" src=images/Fasteners_DIN985.svg  style="width:32px;"> **DIN 985** Écrou Nylstop.

-   <img alt="" src=images/Fasteners_ASMEB18.2.2.1A.svg  style="width:32px;"> **ASME B18.2.2.1A** Écrou à vis mécanique UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.2.2.4A.svg  style="width:32px;"> **ASME B18.2.2.4A** Écrou hexagonal UNC.

-   <img alt="" src=images/Fasteners_ASMEB18.2.2.4B.svg  style="width:32px;"> **ASME B18.2.2.4B** Écrou mince hexagonal UNC.

### Écrous pour rainures en T 

-   <img alt="" src=images/Fasteners_DIN508.svg  style="width:32px;"> **DIN 508** Écrou pour rainures en T.

-   <img alt="" src=images/Fasteners_GN507.svg  style="width:32px;"> **GN 507** Écrou pour rainures en T.

### Rondelles

-   <img alt="" src=images/Fasteners_ISO7089.svg  style="width:32px;"> **ISO 7089** Rondelle plate, série normale. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_ISO7090.svg  style="width:32px;"> **ISO 7090** Rondelle plate chanfreinée, série normale. *Grade de produit A*.

-   <img alt="" src=images/Fasteners_ISO7092.svg  style="width:32px;"> **ISO 7092** Rondelle plate, série étroite. *Produit de qualité A*.

-   <img alt="" src=images/Fasteners_ISO7093-1.svg  style="width:32px;"> **ISO 7093-1** Rondelle plate, série large. *Grade du produit A*.

-   <img alt="" src=images/Fasteners_ISO7094.svg  style="width:32px;"> **ISO 7094** Rondelle plate, série très large. *Produit de qualité C*.

-   <img alt="" src=images/Fasteners_NFE27-619.svg  style="width:32px;"> **NFE27-619** Rondelles cuvette décolletées.

-   <img alt="" src=images/Fasteners_ASMEB18.21.1.12A.svg  style="width:32px;"> **ASME B18.21.1.12A** Rondelle UN, série étroite.

-   <img alt="" src=images/Fasteners_ASMEB18.21.1.12B.svg  style="width:32px;"> **ASME B18.21.1.12B** Rondelle UN, série normale.

-   <img alt="" src=images/Fasteners_ASMEB18.21.1.12C.svg  style="width:32px;"> **ASME B18.21.1.12C** Rondelle UN, série large.

### Circlips

-   <img alt="" src=images/Fasteners_DIN471.svg  style="width:32px;"> **DIN 471** Circlips extérieurs.

-   <img alt="" src=images/Fasteners_DIN472.svg  style="width:32px;"> **DIN 472** Circlips intérieurs.

-   <img alt="" src=images/Fasteners_DIN6799.svg  style="width:32px;"> **DIN 6799** Bague d\'arrêt pour arbre.

### Divers

-   <img alt="" src=images/Fasteners_ScrewTap.svg  style="width:32px;"> Tige filetée de longueur personnalisée pour le taraudage des trous.

-   <img alt="" src=images/Fasteners_ScrewTapInch.svg  style="width:32px;"> Tige filetée de longueur personnalisée pour le taraudage des trous.

-   <img alt="" src=images/Fasteners_ScrewDie.svg  style="width:32px;"> Tube fileté de longueur personnalisée pour couper les filets extérieurs.

-   <img alt="" src=images/Fasteners_ScrewDieInch.svg  style="width:32px;"> Tube fileté de longueur personnalisée pour couper les filets extérieurs.

-   <img alt="" src=images/Fasteners_ThreadedRod.svg  style="width:32px;"> Tige filetée *DIN 975* de longueur arbitraire.

-   <img alt="" src=images/Fasteners_ThreadedRodInch.svg  style="width:32px;"> Tige filetée *UNC* de longueur arbitraire.

## Références

-   Auteur : [shaise](http://theseger.com/projects/author/shaise/)
    -   Concepteur d\'objets : Ulrich Brammer
    -   Architecture de l\'atelier : Shai Seger
-   Page d\'accueil : <http://theseger.com/projects/2015/06/fasteners-workbench-for-freecad/>
-   Code source : <https://github.com/shaise/FreeCAD_FastenersWB>
-   Rapports de bogues et demandes de fonctionnalités : <https://github.com/shaise/FreeCAD_FastenersWB/issues>
-   Sujet de forum : <https://forum.freecadweb.org/viewtopic.php?t=11429>

## Liens

-   [Génération de trous pour vis à tête fraisée dans freecad (en)](http://theseger.com/projects/2015/07/generating-holes-for-countersunk-screws-in-freecad/)
-   [BOLTS](https://github.com/jreinhardt/BOLTS): une librairie ouverte pour les spécifications techniques
-   [Ateliers externes](External_workbenches/fr.md)
-   [Macros](Macros_recipes/fr.md)



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Addons](Category_Addons.md) > [External Command Reference](Category_External Command Reference.md) > [External Workbenches](Category_External Workbenches.md) > [Fasteners](Category_Fasteners.md) > Fasteners Workbench/fr
