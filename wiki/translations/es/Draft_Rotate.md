---
- GuiCommand:/es
   Name:Draft Rotate
   Name/es:Draft Rotate
   Workbenches:[Croquis](Draft_Workbench/es.md), [Arquitectura](Arch_Workbench/es.md)
   MenuLocation:Croquis → Girar
   Shortcut:**R** **O**
---

# Draft Rotate/es


</div>

## Descripción


<div class="mw-translate-fuzzy">

Esta herramienta gira o copia y gira los objetos seleccionados un ángulo dado alrededor de un punto en el [plano de trabajo](Draft_SelectPlane/es.md) actual. Si no se han seleccionado objetos, te invitará a seleccionar uno. Luego, se pregunta al usuario por el centro de rotación, el ángulo de inicio y el ángulo de giro.


</div>

The command can be used on 2D objects created with the [Draft Workbench](Draft_Workbench.md) or [Sketcher Workbench](Sketcher_Workbench.md), but also on many 3D objects such as those created with the [Part Workbench](Part_Workbench.md), [PartDesign Workbench](PartDesign_Workbench.md) or [Arch Workbench](Arch_Workbench.md).

<img alt="" src=images/Draft_Rotate_example.jpg  style="width:400px;"> 
*Rotating an object around a center point*


<div class="mw-translate-fuzzy">

## Utilización


</div>

See also: [Draft Snap](Draft_Snap.md) and [Draft Constrain](Draft_Constrain.md).


<div class="mw-translate-fuzzy">

1.  Selecciona los objetos que desees girar o copiar
2.  Presiona el botón **<img src="images/Draft_Rotate.png" width=16px> [girar](Draft_Rotate/es.md)
**, o presiona las teclas **R** y **O**
3.  Designa un punto central en la vista 3D, o escribe unas coordenadas
4.  Designa un segundo punto en la vista 3D, o indica un ángulo de referencia
5.  Designa un tercer punto en la vista 3D, o indica un ángulo de rotación


</div>

## Opciones

The single character keyboard shortcuts and the modifier key mentioned here can be changed. See [Draft Preferences](Draft_Preferences.md).


<div class="mw-translate-fuzzy">

-   Presiona **X**, **Y** o **Z** después de un punto para restringir el siguiente punto sobre el eje indicado.
-   Para introducir coordenadas manualmente, simplemente introduce los números y presiona **ENTER** entre cada componente X, Y y Z.
-   Presiona **T** o selecciona la casilla para activar/desactivar el botón **'''Continuar'''**. Si el modo continuar está activado, la herramienta Girar se reiniciará al terminar permitiendo que gires o copies otros objetos sin necesidad de volver a presionar el botón de Girar.
-   Presionando **ALT** o **C** o seleccionando el botón **'''Copiar'''** se creará una copia de los objetos, en lugar de girarlos. Si mantienes presionada la tecla **ALT** después de indicar el tercer punto, podrás situar más copias, hasta que liberes la tecla **ALT**.
-   Presiona **CTRL** mientras dibujas para forzar el [ajuste](Draft_Snap/es.md) de tu punto a la posición de ajuste más cercana, independientemente de la distancia.
-   Presiona **SHIFT** mientras dibujas para [restringir](Draft_Constrain/es.md) tu siguiente punto horizontal o verticalmente en relación al centro de giro.
-   Presiona **ESC** o el botón **'''Cancelar'''** para abortar el comando actual.


</div>

## Notes

-   An Object that is [attached](Part_EditAttachment.md) cannot be rotated with the Draft Rotate command. To rotate it either its **Support** object has to be rotated, or its **Attachment Offset** has to be changed.

## Preferences

See also: [Preferences Editor](Preferences_Editor.md) and [Draft Preferences](Draft_Preferences.md).

-   To change the number of decimals used for the input of coordinates and angles: **Edit → Preferences... → General → Units → Units settings → Number of decimals**.
-   To store and reuse the same copy mode setting across commands: **Edit → Preferences... → Draft → General settings → Draft tools options → Global copy mode**.
-   To reselect the base objects after copying objects: **Edit → Preferences... → Draft → General settings → Draft tools options → Select base objects after copying**.

## Scripting


<div class="mw-translate-fuzzy">

## Programación


</div>


<div class="mw-translate-fuzzy">

La herramienta Girar puede utilizarse en [macros](macros/es.md) y desde la consola de Python utilizando la siguiente función:


</div>


```python
rotated_list = rotate(objectslist, angle, center=Vector(0,0,0), axis=Vector(0,0,1), copy=False)
```


<div class="mw-translate-fuzzy">

-   Gira el objeto dado o los objetos contenidos

en la lista dada alrededor de un centro indicado si se proporciona, utilizando el eje como eje de rotación.

-   Si se omite el eje, la rotación se realizará alrededor del eje vertical Z.
-   Si copymode es True, los objetos en realidad no se mueven sino que se crean unas copias.
-   Devuelve los objetos (o sus copias si copymode es True).


</div>

Ejemplo:


```python
import FreeCAD as App
import Draft

doc = App.newDocument()

polygon1 = Draft.make_polygon(3, radius=300)
Draft.move(polygon1, App.Vector(1000, 0, 0))

# Rotation around the origin
angle1 = 45
rot2 = Draft.rotate(polygon1, angle1, copy=True)
rot3 = Draft.rotate(polygon1, 2*angle1, copy=True)
rot4 = Draft.rotate(polygon1, 4*angle1, copy=True)

polygon2 = Draft.make_polygon(3, radius=1000)
polygon3 = Draft.make_polygon(5, radius=500)
Draft.move(polygon2, App.Vector(2000, 0, 0))
Draft.move(polygon3, App.Vector(2000, 0, 0))

# Rotation around another point
angle2 = 60
cen = App.Vector(3100, 0, 0)
list2 = [polygon2, polygon3]
rot_list2 = Draft.rotate(list2, angle2, center=cen, copy=True)
rot_list3 = Draft.rotate(list2, 2*angle2, center=cen, copy=True)
rot_list4 = Draft.rotate(list2, 4*angle2, center=cen, copy=True)

doc.recompute()
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft Rotate/es
