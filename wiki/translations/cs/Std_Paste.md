# Std Paste/cs
---
- GuiCommand:/cs   Name:Std_Paste   Name/cs:Std_Paste   MenuLocation:Edit → Paste   Shortcut:Ctrl+V   Workbenches:All   SeeAlso:[Copy](Std_Copy/cs.md), [Duplicate Selection](Std_DuplicateSelection/cs.md)---


</div>

## Description

The **Std Paste** command pastes objects from the Clipboard into the active document.

## Usage

1.  There are several ways to invoke the command:
    -   Select the **Edit → <img src="images/Std_Paste.svg" width=16px> Paste** option from the menu.
    -   Select the **<img src="images/Std_Paste.svg" width=16px> Paste** option from the [Tree view](Tree_view.md) context menu. Note that this option is only available when an existing object has been selected.
    -   Use the keyboard shortcut: **Ctrl**+**V**.

## Notes

-   FreeCAD will automatically change the internal names and, depending on the preferences, labels of objects to avoid name conflicts.
-   A spreadsheet cell alias that already exists in the spreadsheet will not be pasted.
-   When you are working in a FreeCAD text window, an input box or a spreadsheet, the standard keyboard shortcut **Ctrl**+**V**, in almost all cases, does not call the **Std Paste** command but uses the Paste function from the OS instead.
-   It is not possible to copy-paste native objects between FreeCAD and other applications.

## Preferences

-   Duplicate labels are allowed if **Tools → Edit parameters... → BaseApp → Preferences → Document → DuplicateLabels** is set to `True`. This setting can also be changed in the [Preferences Editor](Preferences_Editor#Document.md).





{{Std Base navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Std Paste/cs
