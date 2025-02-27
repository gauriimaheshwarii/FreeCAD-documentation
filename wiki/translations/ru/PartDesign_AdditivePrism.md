---
- GuiCommand:/ru
   Name/ru:Аддитивная призма
   Name:PartDesign_AdditivePrism
   MenuLocation:Part Design → Создать аддитивный примитив → Аддитивная Призма
   Workbenches:[PartDesign](PartDesign_Workbench/ru.md)
   Version:0.17
   SeeAlso:[Создать аддитивный примитив](PartDesign_CompPrimitiveAdditive/ru.md), [Субтрактивная призма](PartDesign_SubtractivePrism/ru.md)
---

# PartDesign AdditivePrism/ru

## Описание

Вставляет в активное Тело простую геометрическую форму - призму, в качестве базового конструктивного элемента, или объединяет этот элемент с уже существующей совокупностью конструктивных элементов.

<img alt="" src=images/PartDesign_AdditivePrism_example.png  style="width:200px;">

## Применение

1.  Нажмите кнопку **<img src="images/PartDesign_AdditivePrism.svg" width=24px> '''Аддитивная призма'''**. **Примечание**: Инструмент Аддитивная призма входит в состав меню с названием \"Создать аддитивный примитив\". После запуска FreeCAD на панели инструментов в этом меню по умолчанию отображается инструмент Аддитивный куб. Чтобы перейти к кнопке создания Призмы, нажмите на стрелку указывающую вниз рядом со значком и выберите Аддитивная призма в выпадающем меню.
2.  Установите параметры геометрической формы и [настройки крепления](Part_EditAttachment/ru.md) к уже существующим конструктивным элементам, если это требуется.
3.  Нажмите **OK**.
4.  Конструктивный элемент Призма появится в иерархии документа под активным Телом.

## Опции

Возможно также создавать наклонные призмы, указав углы наклона её боковых рёбер относительно плоскости основания. {{Version/ru|0.19}}

Параметры Призмы после её создания можно изменить двумя способами:

-   Дважды щелкнув по ней в дереве модели или щелкнув правой кнопкой мыши и выбрав **Редактировать примитив** в контекстном меню; это откроет окно параметров примитива.
-   Через [Редактор свойств](Property_editor/ru.md).

## Свойства

-    **Attachment**: defines the attachment mode as well as the Attachment Offset. See [Part EditAttachment](Part_EditAttachment.md).

-    **Label**: label given to the Prism object. Change to suit your needs.

-    **Polygon**: number of sides in the polygon cross-section of the prism.

-    **Circumradius**: [circumscribed radius](https://en.wikipedia.org/wiki/Circumscribed_circle) of the polygon cross-section of the prism.

-    **Height**: height of the prism.

-    **First Angle**: angle in first direction. <small>(v0.19)</small> 

-    **Second Angle**: angle in second direction. <small>(v0.19)</small> 





{{PartDesign_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [PartDesign](PartDesign_Workbench.md) > PartDesign AdditivePrism/ru
