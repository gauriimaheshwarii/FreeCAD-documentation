# Arch API/hr
**(November 2018) The Arch API is listed in the [https://www.freecadweb.org/api autogenerated API documentation].**

The functions of the API are part of the [Arch Workbench](Arch_Workbench.md) and can be used in [macros](macros.md) and from the [Python](Python.md) console once the `Arch` module has been imported. The [Reinforcement Addon](Reinforcement_Addon.md) has its own [Reinforcement API](Reinforcement_API.md).

Primjer: 
```python
import FreeCAD, Draft, Arch

p1 = FreeCAD.Vector(0, 0, 0)
p2 = FreeCAD.Vector(2000, 0, 0)
baseline = Draft.makeLine(p1, p2)

Arch.makeWall(baseline, length=None, width=200, height=2000)
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [API](Category_API.md) > [Poweruser Documentation](Category_Poweruser Documentation.md) > [Arch](Arch_Workbench.md) > Arch API/hr
