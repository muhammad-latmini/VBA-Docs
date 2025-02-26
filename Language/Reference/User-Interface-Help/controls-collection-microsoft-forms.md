---
title: Controls collection (Microsoft Forms)
keywords: fm20.chm2000500
f1_keywords:
- fm20.chm2000500
ms.prod: office
api_name:
- Office.Controls
ms.assetid: b84e6c66-8773-58c7-d076-191e4397ee6a
ms.date: 11/15/2018
ms.localizationpriority: medium
---


# Controls collection (Microsoft Forms)

Includes all the controls contained in an object.

## Remarks

Each control in the **Controls** collection of an object has a unique index whose value can be either an integer or a string. The index value for the first control in a [collection](../../Glossary/vbe-glossary.md#collection) is 0; the value for the second control is 1, and so on. This value indicates the order in which controls were added to the collection.

If the index is a string, it represents the name of the control. The **Name** property of a control also specifies a control's name.

Use the **Controls** collection to enumerate or count individual controls, and to set their properties. For example, you can enumerate the **Controls** collection of a particular form and set the **Height** property of each control to a specified value.

> [!NOTE] 
> The **For Each...Next** statement is useful for enumerating a collection.

## See also

- [Microsoft Forms examples](examples-microsoft-forms.md)
- [Microsoft Forms reference](reference-microsoft-forms.md)
- [Microsoft Forms concepts](concepts-microsoft-forms.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]