---
- GuiCommand:/fr
   Name:Std ViewIvStereoInterleavedRows
   Name/fr:Std Lignes stéréo entrelacées
   MenuLocation:Affichage → Stéréo → Lignes stéréo entrelacées
   Workbenches:Tous
   SeeAlso:[Std Stéréo rouge cyan](Std_ViewIvStereoRedGreen/fr.md), [Std Tampon stéréo quadruple](Std_ViewIvStereoQuadBuff/fr.md), [Std Colonnes stéréo entrelacées](Std_ViewIvStereoInterleavedColumns/fr.md), [Std Stéréo désactivée](Std_ViewIvStereoOff/fr.md)
---

# Std ViewIvStereoInterleavedRows/fr

## Description

La commande **Std Lignes stéréo entrelacées** change le mode actif de la [vue 3D](3D_view/fr.md) en mode d\'affichage stéréo des lignes entrelacées. Pour utiliser ce mode stéréo, une carte graphique spéciale, un écran spécial et des lunettes [avec verres polarisés](https://en.wikipedia.org/wiki/Polarized_3D_system) sont nécessaires.

## Utilisation

1.  Sélectionnez l\'option **Affichage → Stéréo → <img src="images/Std_ViewIvStereoInterleavedRows.svg" width=16px> Lignes stéréo entrelacées** dans le menu.

## Préférences

-   La distance entre les yeux peut être modifiée dans les préférences: **Édition → Préférences... → Affichage → Vue 3D → Eye to eye distance for stereo modes**. Voir l\'[Editeur de préférences](Preferences_Editor#3D_View/fr.md).

## Script


**Voir aussi:**

[FreeCAD Script de base](FreeCAD_Scripting_Basics/fr.md).

Pour modifier la vue en lignes entrelacées stéréo, utilisez la méthode `setStereoType` de l\'objet ActiveView. Cette méthode n\'est pas disponible si FreeCAD est en mode console.


```python
import FreeCADGui

FreeCADGui.ActiveDocument.ActiveView.setStereoType('InterleavedRows')
FreeCADGui.ActiveDocument.ActiveView.getStereoType()
```





{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std ViewIvStereoInterleavedRows/fr
