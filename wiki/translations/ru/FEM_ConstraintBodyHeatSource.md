---
- GuiCommand:/ru
   Name:FEM ConstraintBodyHeatSource
   Name/ru:FEM ConstraintBodyHeatSource
   Icon:Fem-constraint-heatflux.svg
   MenuLocation: Model → Thermal constraints → Constraint body heat source
   Workbenches:[FEM](FEM_Workbench/ru.md)
   Shortcut:
   SeeAlso:[FEM tutorial](FEM_tutorial/ru.md)
---

# FEM ConstraintBodyHeatSource/ru


</div>

## Описание

Defines an internally generated body heat given in W/kg.

## Применение

1.  Either press the **<img src="images/FEM_ConstraintBodyHeatSource.svg" width=16px> '''FEM ConstraintBodyHeatSource'''** or select the menu **Model → Thermal Constraints → <img src="images/FEM_ConstraintBodyHeatSource.svg" width=16px> Constraint body heat source**.
2.  Set the value:
    -   
        <small>(v1.0)</small> 
        
        : For a 3D analysis, select a \'solid\' (body) from your model, for a 2D analysis select a face.

    -   
        {{VersionMinus|0.20}}
        
        : Since the constraint has no task dialog, use the [property editor](Property_editor.md) and set the property **Heat Source**.

## Limitation


{{VersionMinus|0.20}}

: The body heat source is applied to the whole model, meaning all bodies of the setup. It is not possible to select an individual body.

## Примечания

-   This constraint works only with the Elmer solver.
-   For more information see [this forum thread](https://forum.freecadweb.org/viewtopic.php?f=18&t=44705&start=490#p422539) and following posts. [This thread](https://forum.freecadweb.org/viewtopic.php?f=18&t=28926) may also be useful.
-   Elmer examples can also be found in [Elmer GUI Tutorials](https://www.nic.funet.fi/pub/sci/physics/elmer/doc/ElmerTutorials.pdf).




{{FEM Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM ConstraintBodyHeatSource/ru
