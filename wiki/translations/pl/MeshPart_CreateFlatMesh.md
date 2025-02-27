---
- GuiCommand:/pl
   Name:MeshPart CreateFlatMesh
   Name/pl:Projekt Siatki: Rozwiń siatkę
   MenuLocation:Siatki → Rozwiń siatkę
   Workbenches:[Siatka](Mesh_Workbench/pl.md)
   SeeAlso:[Rozwiń powierzchnię](MeshPart_CreateFlatFace/pl.md)
---

# MeshPart CreateFlatMesh/pl

## Opis

Polecenie **Rozwiń powierzchnię** tworzy płaską reprezentację obiektu siatkowego poprzez jego rozwinięcie, rozłożenie. Utworzony kontur jest [cechą części](Part_Feature/pl.md) środowiska Część.

![](images/MeshPart_CreateFlatMesh_example.png ) 
*Obiekt siatkowy i w kolorze czerwonym, jego płaska reprezentacja.*

## Użycie

1.  Wybierz pojedynczy obiekt siatki. Siatka musi być \"rozpakowalna\". Na przykład, aby rozwinąć siatkę cylindryczną musi ona mieć otwarte końce i otwarty szew. Również zakrzywione powierzchnie muszą mieć stosunkowo drobną siatkę. Użyj polecenia [Ulepsz przez Gmsh](Mesh_RemeshGmsh/pl.md) jeśli to konieczne.
2.  Wybierz z menu opcję **Siatki → <img src="images/MeshPart_CreateFlatMesh.svg" width=16px> Rozwiń siatkę**.

## Właściwości

Zapoznaj się z informacjami na stronie: [cecha](Part_Feature/pl.md) środowiska Część.





{{Mesh Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Mesh](Category_Mesh.md) > [MeshPart](MeshPart_Workbench.md) > MeshPart CreateFlatMesh/pl
