---
title: TextBox.CanGrow property (Access)
keywords: vbaac10.chm11068
f1_keywords:
- vbaac10.chm11068
ms.prod: access
api_name:
- Access.TextBox.CanGrow
ms.assetid: 5e96e693-9e1a-1f1f-5d5d-672e6232c330
ms.date: 02/28/2019
ms.localizationpriority: medium
---


# TextBox.CanGrow property (Access)

Gets or sets whether the specified control automatically adjusts vertically to print or preview all the data that the control contains. Read/write **Boolean**. 


## Syntax

_expression_.**CanGrow**

_expression_ A variable that represents a **[TextBox](Access.TextBox.md)** object.


## Remarks

The **CanGrow** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Yes|**True** (1)|The section or control grows vertically so that all data it contains can be printed or previewed.|
|No|**False** (0)|(Default) The section or control doesn't grow. Data that doesn't fit within the fixed size of the section or control won't be printed or previewed.|

This property setting is read-only in a macro or Visual Basic in any view but Design view.

Use this property to control the appearance of printed forms and reports. When you set the property to Yes, the object automatically adjusts so that any amount of data can be printed. When a control grows, the controls below it move down the page.

If you set a control's **CanGrow** property to Yes, Microsoft Access automatically sets the **CanGrow** property of the section containing the control to Yes.

Sections grow vertically across their entire width. To grow the data independently, you can place two subform or subreport controls side by side, and set their **CanGrow** property to Yes.

When you use the **CanGrow** property, remember that:

- The property settings don't affect the horizontal spacing between controls; they affect only the vertical space that the controls occupy.
    
- Overlapping controls can't grow.
    


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
