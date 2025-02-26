---
title: CustomXMLPart.NodeAfterReplace event (Office)
keywords: vbaof11.chm296003
f1_keywords:
- vbaof11.chm296003
ms.prod: office
api_name:
- Office.CustomXMLPart.NodeAfterReplace
ms.assetid: acb4a1d6-7928-5f6b-938a-1e56ea3db1b3
ms.date: 01/07/2019
ms.localizationpriority: medium
---


# CustomXMLPart.NodeAfterReplace event (Office)

Occurs just after a node is replaced in a **CustomXMLPart** object.


## Syntax

_expression_.**NodeAfterReplace**(_OldNode_, _NewNode_, _InUndoRedo_)

_expression_ An expression that returns a **[CustomXMLPart](Office.CustomXMLPart.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _OldNode_|Required|**CustomXMLNode**|Corresponds to the node that was just removed from the **CustomXMLPart** object. Note that this node may have children if a subtree was just added to the document. Also, this node will be a "disconnected" node in that you can query down from the node, but cannot go up; it appears to exist alone.|
| _NewNode_|Required|**CustomXMLNode**|Corresponds to the node just added to the **CustomXMLPart** object.|
| _InUndoRedo_|Required|**Boolean**|Returns **True** if the node was added as part of an Undo/Redo action by the user.|

## Example

The following example displays a message telling the user the results of replacing the node.


```vb
Sub CustomXMLParts_NodeAfterReplace(oldNode As CustomXMLNode, newNode As CustomXMLNode, boolInUndoRedo As Boolean) 
   MsgBox ("The part's node " & oldNode.BaseName & " was replaced with the node " & newNode.BaseName) 
End Sub
```


## See also

- [CustomXMLPart object members](overview/library-reference/customxmlpart-members-office.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]