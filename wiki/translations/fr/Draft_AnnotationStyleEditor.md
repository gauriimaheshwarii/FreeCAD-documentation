---
- GuiCommand:/fr
   Name:Draft AnnotationStyleEditor
   Name/fr:Draft Éditeur de styles d'annotations
   MenuLocation:Annotation → Éditeur de styles d'annotations...
   Workbenches:[Draft](Draft_Workbench/fr.md)
   SeeAlso:[Draft Texte](Draft_Text/fr.md), [Draft Étiquette](Draft_Label/fr.md), [Draft Dimension](Draft_Dimension/fr.md)
   Version:0.19
---

# Draft AnnotationStyleEditor/fr

## Description

La commande <img alt="" src=images/Draft_AnnotationStyleEditor.svg  style="width:24px;"> **Draft Éditeur de styles d\'annotations** vous permet de définir des styles qui affectent les propriétés visuelles des objets de type annotation, comme ceux créés par les commandes [Draft Texte](Draft_Text/fr.md), [Draft Dimension](Draft_Dimension/fr.md) et [Draft Étiquette](Draft_Label/fr.md).


{{Version/fr|1.0}}

: plusieurs bogues ont été corrigés et un bouton séparé de couleur de texte a été ajouté.

![](images/Draft_AnnotationStyleEditor_Dialog.png ) 
*La boîte de dialogue de l'Éditeur de styles d'annotation*



## Utilisation

1.  Il existe plusieurs façons de lancer la commande :
    -   Appuyez sur le bouton **<img src="images/Draft_AnnotationStyleEditor.svg" width=16px> [Éditeur de styles d'annotations...](Draft_AnnotationStyleEditor/fr.md)**.
    -   Sélectionnez l\'option **Annotation → <img src="images/Draft_AnnotationStyleEditor.svg" width=16px> Éditeur de styles d'annotation...** dans le menu.
2.  La boîte de dialogue **Éditeur de styles d'annotation** s\'ouvre.
3.  Sélectionnez un style dans la liste déroulante **Nom du style** ou choisissez {{Value|Ajouter nouveau...}} pour définir un nouveau style.
4.  Vous pouvez également ajuster les propriétés du style.
5.  Vous pouvez également appuyer sur le bouton **[<img src=images/Accessories-text-editor.svg style="width:16px"> Renommer** pour renommer le style.
6.  Vous pouvez également appuyer sur le bouton **[<img src=images/Edit_Cancel.svg style="width:16px"> Supprimer** pour supprimer le style.
7.  Vous pouvez également appuyer sur le bouton **[<img src=images/Std_Import.svg style="width:16px">** pour importer tous les styles d\'un fichier **.json**. Cela écrasera les styles existants portant le même nom.
8.  Vous pouvez également appuyer sur le bouton **[<img src=images/Std_Export.svg style="width:16px">** pour exporter tous les styles vers un fichier **.json**.
9.  Appuyez sur le bouton **OK** pour fermer la boîte de dialogue et terminer la commande.



## Script

Voir aussi : [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) et [FreeCAD Débuter avec les scripts](FreeCAD_Scripting_Basics/fr.md).


{{Version/fr|1.0}}

: les informations de ce paragraphe ont été mises à jour et reflètent la version 1.0 de FreeCAD.

Les styles d\'annotation sont enregistrés en tant que dictionnaires sérialisés dans l\'attribut `Meta` du document. Cet attribut est inspecté par l\'éditeur de style d\'annotation lorsqu\'il est ouvert.


```python
>>> print(App.ActiveDocument.Meta["Draft_Style_Text red"])
{"FontName": "DejaVu Sans", "FontSize": 10.0, "LineSpacing": 1.0, "TextColor": 4278190335, "ScaleMultiplier": 1.0, "ShowUnit": false, "UnitOverride": "", "Decimals": 2, "ShowLine": true, "LineWidth": 2, "ArrowType": 0, "ArrowSize": 2.0, "LineColor": 255, "DimOvershoot": 0.0, "ExtLines": 0.0, "ExtOvershoot": 4.0}
```

Chaque style qui apparaît dans l\'éditeur est enregistré en interne avec le nom de style préfixé par `Draft_Style_`. Cela empêchera des conflits de noms avec d\'autres clés qui peuvent être enregistrées dans `Meta` et qui peuvent contenir des informations arbitraires.

Vous pouvez définir tout nouveau style en ajoutant les informations nécessaires à une clé commençant par `Draft_Style_`. La valeur correspondante de cette clé doit être un dictionnaire sérialisé à l\'aide de `json`.


```python
import json

meta = App.ActiveDocument.Meta
props = {"LineWidth": 6, "ArrowSize": 7.0}
meta["Draft_Style_Thick_lines"] = json.dumps(props)
App.ActiveDocument.Meta = meta
```

Les propriétés non saisies seront remplies automatiquement lorsque ce style sera sélectionné dans l\'éditeur de style et que le bouton **OK** sera activé.

De la même manière, tout dictionnaire sérialisé peut être décompressé pour l\'édition.


```python
import json

meta = App.ActiveDocument.Meta
new_dict = json.loads(meta["Draft_Style_Thick_lines"])
```

Les propriétés doivent avoir les types suivants :

Les chaînes de caractères :


```python
props = {
    "FontName": "DejaVu Sans",
    "UnitOverride": ""
}
```

Les valeurs flottantes (doivent être fournies avec un point décimal) :


```python
props = {
    "FontSize": 10.0,
    "LineSpacing": 1.0,
    "ScaleMultiplier": 1.0,
    "ArrowSize": 2.0,
    "DimOvershoot": 0.0,
    "ExtLines": 0.0,
    "ExtOvershoot": 4.0
}
```

Les entiers :


```python
props = {
    "TextColor": 4278190335,
    "Decimals": 2,
    "LineWidth": 2,
    "ArrowType": 0,
    "LineColor": 255
}
```


{{Incode|TextColor}}

et {{Incode|LineColor}} correspondent à un entier de 32 bits, dont on peut extraire chacunr des valeurs RGBA. {{Incode|ArrowType}} est un énumérateur.

Booléens :


```python
props = {
    "ShowUnit": false,
    "ShowLine": true
}
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft AnnotationStyleEditor/fr
