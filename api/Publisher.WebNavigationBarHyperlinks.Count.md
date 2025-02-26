---
title: WebNavigationBarHyperlinks.Count property (Publisher)
keywords: vbapb10.chm8585219
f1_keywords:
- vbapb10.chm8585219
ms.prod: publisher
api_name:
- Publisher.WebNavigationBarHyperlinks.Count
ms.assetid: 55e62f9b-7d7e-50bd-bd3b-0c2fdae903df
ms.date: 06/18/2019
ms.localizationpriority: medium
---


# WebNavigationBarHyperlinks.Count property (Publisher)

Returns a **Long** that represents the number of items in the specified collection.


## Syntax

_expression_.**Count**

_expression_ A variable that represents a **[WebNavigationBarHyperlinks](publisher.webnavigationbarhyperlinks.md)** object.


## Example

This example displays the number of pages in the active document.

```vb
Sub CountNumberOfPages() 
 MsgBox "Your publication contains " & _ 
 ActiveDocument.Pages.Count & " page(s)." 
End Sub
```

<br/>

This example displays the number of shapes in the active document.

```vb
Sub CountNumberOfShapes() 
 Dim intShapes As Integer 
 Dim pg As Page 
 
 For Each pg In ActiveDocument.Pages 
 intShapes = intShapes + pg.Shapes.Count 
 Next 
 
 MsgBox "Your publication contains " & intShapes & " shape(s)." 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]