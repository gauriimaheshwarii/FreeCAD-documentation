---
- GuiCommand:/ru
   Name:Std TreeMultiDocument
   Name/ru:Std TreeMultiDocument
   MenuLocation:Вид → Дерево документа → Многокомпонентный документ
   Workbenches:All
   SeeAlso:[Std TreeSingleDocument](Std_TreeSingleDocument/ru.md), [Std TreeCollapseDocument](Std_TreeCollapseDocument/ru.md)
---

# Std TreeMultiDocument/ru


</div>

## Описание

The **Std TreeMultiDocument** command switches the [Tree view](Tree_view.md) DocumentMode to MultiDocument. In this mode all documents are visible in the Tree view and multiple documents can be expanded. The other modes are [SingleDocument](Std_TreeSingleDocument.md) and [CollapseDocument](Std_TreeCollapseDocument.md).

## Применение

1.  There are several ways to invoke the command:
    -   Click on the black down arrow to the right of the **<img src="images/Std_TreeSyncView.svg" width=16px>** button and select the **Multi document** option from the flyout. Note: the button image will change depending on the selected option.
    -   Select the **View → TreeView actions → <img src="images/Std_TreeMultiDocument.svg" width=16px> Multi document** option from the menu.

## Настройки

The Tree view DocumentMode mode is stored: **Tools → Edit parameters... → BaseApp → Preferences → TreeView → DocumentMode**. It is an integer value. Possible values are `0` (SingleDocument), `1` (MultiDocument) or `2` (CollapseDocument). The default is `2`.





{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std TreeMultiDocument/ru
