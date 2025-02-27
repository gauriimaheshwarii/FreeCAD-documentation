---
- GuiCommand:
   Name:TechDraw Image
   Name/pl:Rysunek Techniczny: Obraz
   MenuLocation:Rysunek Techniczny → Wstaw obraz bitmapy
   Workbenches:[Rysunek Techniczny](TechDraw_Workbench/pl.md)
   SeeAlso:[SVG Symbol](TechDraw_Symbol/pl.md)
---

# TechDraw Image/pl

## Opis

Narzędzie **Obraz** wstawia z pliku do strony widok obrazu [bitmapy](Bitmap/pl.md) *(PNG, TIFF, JPEG itp.)*.

![](images/TechDraw_Image_example.png ) 
*Obraz wstawiony do strony rysunku.*

## Użycie

1.  Naciśnij przycisk **<img src="images/TechDraw_Image.svg" width=16px> [Wstaw obraz bitmapy](TechDraw_Image/pl.md)**.
2.  Otworzy się okno dialogowe pliku. Wybierz lokalizację i nazwę pliku.

## Właściwości

Zapoznaj się również informacjami na stronie [właściwości widoku](TechDraw_View/pl#Widok.md) środowiska Rysunek Techniczny.

### Dane


{{TitleProperty|Obraz}}

-    **Plik obrazu|File**: Plik zawierający tę bitmapę.

-    **Obraz dołączony|FileIncluded**: Wbudowany plik graficzny. Tylko do użytku systemowego.

-    **Szerokość|Float**: Szerokość wykadrowanego obrazu w mm. Używane tylko wtedy, gdy **Przytnij** ma wartość {{TRUE/pl}}.

-    **Wysokość|Float**: Wysokość wykadrowanego obrazu w mm. Analogicznie.

### Widok


{{TitleProperty|Obraz}}

-    **Przytnmij|Bool**: Przycina obraz do parametrów **Szerokość** x **Wysokość**.

## Tworzenie skryptów 

Zobacz również stronę: [Dokumentacja API generowana automatycznie](https://freecad.github.io/SourceDoc/) oraz [Podstawy pisania skryptów dla FreeCAD](FreeCAD_Scripting_Basics/pl.md).

Narzędzie Obraz może być używane w [makrodefinicjach](macros/pl.md) i z konsoli [Python](Python/pl.md) za pomocą następujących funkcji:


```python
dvi = FreeCAD.ActiveDocument.addObject('TechDraw::DrawViewImage','TestImage')
rc = page.addView(dvi)
dvi.ImageFile = "pathToMy/imageFile.png"
dvi.Height = 200
dvi.Width  = 200
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw Image/pl
