---
title: Form.OnMouseMove property (Access)
keywords: vbaac10.chm13452
f1_keywords:
- vbaac10.chm13452
ms.prod: access
api_name:
- Access.Form.OnMouseMove
ms.assetid: c0d5b1f8-edbc-d319-6edd-e48768b61f40
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# Form.OnMouseMove property (Access)

Sets or returns the value of the **On Mouse Move** box in the Properties window. Read/write **String**.


## Syntax

_expression_.**OnMouseMove**

_expression_ A variable that represents a **[Form](Access.Form.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The **MouseMove** event occurs when the user moves the mouse over the object.

The **OnMouseMove** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Mouse Move** box in the object's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Mouse Move** box is blank, the property value is an empty string.


## Example

The following example prints the value of the **OnMouseMove** property in the Immediate window for the button named **OK** on the **Order Entry** form.

```vb
Debug.Print Forms("Order Entry").Controls("OK").OnMouseMove
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]