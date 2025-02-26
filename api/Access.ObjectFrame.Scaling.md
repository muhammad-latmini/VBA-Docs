---
title: ObjectFrame.Scaling property (Access)
keywords: vbaac10.chm11611
f1_keywords:
- vbaac10.chm11611
ms.prod: access
api_name:
- Access.ObjectFrame.Scaling
ms.assetid: ec0ccdc1-edcd-14d1-05ca-2c3b2e200440
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# ObjectFrame.Scaling property (Access)

Controls how the contents of an object frame control are displayed. Read/write **Byte**.


## Syntax

_expression_.**Scaling**

_expression_ A variable that represents an **[ObjectFrame](Access.ObjectFrame.md)** object.


## Remarks

The **Scaling** property corresponds to the **Size Mode** box in the object frame's Properties window. This property accepts the following values:

- **0** (Clip) If the object exceeds the control's boundaries, the object is clipped at the boundaries of the control.
    
- **1** (Stretch) If the object does not exceed the control's boundaries, the object is stretched to the edges of the control's boundary.
    
- **2** (Zoom) The object is zoomed in or out to fit the control's boundaries. This is different from the Stretch setting, in that the object is not necessarily distorted to touch all boundaries of the control. In other words, the object may touch the horizontal edges of the control, but not necessarily the vertical edges of the control, and vice versa.
    

## Example

The following example sets the size mode of the OLE control **Customer Picture** on the **Order Entry** form to zoomed.

```vb
Forms("Order Entry").Controls("Customer Picture").Scaling = 2
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]