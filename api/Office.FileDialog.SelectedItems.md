---
title: FileDialog.SelectedItems property (Office)
keywords: vbaof11.chm256009
f1_keywords:
- vbaof11.chm256009
ms.prod: office
api_name:
- Office.FileDialog.SelectedItems
ms.assetid: af45013a-c745-3f14-9c12-64a1c2b50279
ms.date: 01/09/2019
ms.localizationpriority: medium
---


# FileDialog.SelectedItems property (Office)

Gets a **FileDialogSelectedItems** collection. This collection contains a list of the paths of the files that a user selected from a file dialog box displayed by using the **Show** method of the **FileDialog** object. Read-only.


## Syntax

_expression_.**SelectedItems**

_expression_ A variable that represents a **[FileDialog](Office.FileDialog.md)** object.


## Example

The following example displays a **File Picker** dialog box by using the **FileDialog** object, and displays each selected file in a message box.


```vb
Sub Main() 
 
 'Declare a variable as a FileDialog object. 
 Dim fd As FileDialog 
 
 'Create a FileDialog object as a File Picker dialog box. 
 Set fd = Application.FileDialog(msoFileDialogFilePicker) 
 
 'Declare a variable to contain the path 
 'of each selected item. Even though the path is aString, 
 'the variable must be a Variant because For Each...Next 
 'routines only work with Variants and Objects. 
 Dim vrtSelectedItem As Variant 
 
 'Use a With...End With block to reference the FileDialog object. 
 With fd 
 
 'Allow the user to select multiple files. 
 .AllowMultiSelect = True 
 
 'Use the Show method to display the File Picker dialog box and return the user's action. 
 'If the user presses the button... 
 If .Show = -1 Then 
 'Step through each string in the FileDialogSelectedItems collection. 
 For Each vrtSelectedItem In .SelectedItems 
 
 'vrtSelectedItem is aString that contains the path of each selected item. 
 'Use any file I/O functions that you want to work with this path. 
 'This example displays the path in a message box. 
 MsgBox "Selected item's path: " & vrtSelectedItem 
 
 Next 
 'If the user presses Cancel... 
 Else 
 End If 
 End With 
 
 'Set the object variable to Nothing. 
 Set fd = Nothing 
 
End Sub
```


## See also

- [FileDialog object members](overview/library-reference/filedialog-members-office.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
