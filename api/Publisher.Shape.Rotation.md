---
title: Shape.Rotation property (Publisher)
keywords: vbapb10.chm2228294
f1_keywords:
- vbapb10.chm2228294
ms.prod: publisher
api_name:
- Publisher.Shape.Rotation
ms.assetid: 3cb55e8c-83fa-2f20-caac-a1e897e9a369
ms.date: 06/13/2019
ms.localizationpriority: medium
---


# Shape.Rotation property (Publisher)

Returns or sets a **Single** that represents the number of degrees that the specified shape is rotated around the z-axis. A positive value indicates clockwise rotation; a negative value indicates counterclockwise rotation. Read/write.


## Syntax

_expression_.**Rotation**

_expression_ A variable that represents a **[Shape](Publisher.Shape.md)** object.


## Remarks

To set the rotation of a three-dimensional shape around the x-axis or the y-axis, use the **[RotationX](Publisher.ThreeDFormat.RotationX.md)** property or the **[RotationY](Publisher.ThreeDFormat.RotationY.md)** property of the **ThreeDFormat** object.


## Example

This example matches the rotation of all shapes on the first page of the active publication to the rotation of the first shape. This example assumes that there are at least two shapes on the first page of the active publication.

```vb
Sub SetShapeRotation() 
 Dim sngRotation As Single 
 Dim intCount As Integer 
 With ActiveDocument.Pages(1).Shapes 
 sngRotation = .Item(1).Rotation 
 For intCount = 1 To .Count 
 .Item(intCount).Rotation = sngRotation 
 Next intCount 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]