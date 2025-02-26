---
title: Application.GanttBarEditEx method (Project)
keywords: vbapj.chm2145
f1_keywords:
- vbapj.chm2145
ms.prod: project-server
api_name:
- Project.Application.GanttBarEditEx
ms.assetid: b574b975-a869-31ba-e525-df8775330b0a
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Application.GanttBarEditEx method (Project)

Changes or creates a Gantt bar style, where colors can be hexadecimal values.


## Syntax

_expression_. `GanttBarEditEx`( `_Item_`, `_Create_`, `_Name_`, `_StartShape_`, `_StartType_`, `_StartColor_`, `_MiddleShape_`, `_MiddleColor_`, `_MiddlePattern_`, `_EndShape_`, `_EndType_`, `_EndColor_`, `_ShowFor_`, `_Row_`, `_From_`, `_To_`, `_BottomText_`, `_TopText_`, `_LeftText_`, `_RightText_`, `_InsideText_` )

 _expression_ An expression that returns an **[Application](Project.Application.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Item_|Required|**String**|The name or row number of the Gantt bar style to change in the **Bar Styles** dialog box.|
| _Create_|Optional|**Boolean**|**True** if a new Gantt bar style is created and inserted in the **Bar Styles** dialog box before the Gantt bar style specified with **Item**. If **Item** is "-1", the new Gantt bar style is added to the end of the list of styles. The default value is **False**.|
| _Name_|Optional|**String**|A new name for the Gantt bar.|
| _StartShape_|Optional|**Integer**|The start shape of the Gantt bar. The default value is **pjNone**. Can be one of the **[PjBarEndShape](Project.PjBarEndShape.md)** constants.|
| _StartType_|Optional|**Integer**|The start type of the Gantt bar. Can be one of the following **[PjBarType](Project.PjBarType.md)** constants: **pjDashed**, **pjFramed**, or **pjSolid**. The default value is **pjSolid**.|
| _StartColor_|Optional|**Long**|The start color of the Gantt bar. Can be a hexadecimal RGB value, where red is the last byte. For example, &H00FFFF is yellow. The default value is &H0 (black). |
| _MiddleShape_|Optional|**Integer**|The middle shape of the Gantt bar. Can be one of the **[PjBarShape](Project.PjBarShape.md)** constants. The default value is **pjRectangleBar**.|
| _MiddleColor_|Optional|**Long**|The middle color of the Gantt bar. Can be a hexadecimal RGB value, where red is the last byte. For example, &HFFFF00 is blue-green. The default value is &H0 (black).|
| _MiddlePattern_|Optional|**Integer**|The middle pattern of the Gantt bar. Can be one of the **[PjFillPattern](Project.PjFillPattern.md)** constants. The default value is **pjMediumFillPattern**.|
| _EndShape_|Optional|**Integer**|The end shape of the Gantt bar. Can be one of the **[PjBarEndShape](Project.PjBarEndShape.md)** constants. The default value is **pjNone**.|
| _EndType_|Optional|**Integer**|The end type of the Gantt bar. Can be one of the following **PjBarType** constants: **pjDashed**, **pjFramed**, or **pjSolid**. The default value is **pjSolid**.|
| _EndColor_|Optional|**Long**|The end color of the Gantt bar. Can be a hexadecimal RGB value, where red is the last byte. The default value is &H0 (black).|
| _ShowFor_|Optional|**String**|One or more task types (such as normal, split, summary, milestone, and so on) separated by the list separator character.|
| _Row_|Optional|**Integer**|A number from 1 to 4 that specifies the row in which the Gantt bar appears. The default value is 1.|
| _From_|Optional|**String**|The name of a date field specifying the start of the Gantt bar.|
| _To_|Optional|**String**|The name of a date field specifying the end of the Gantt bar.|
| _BottomText_|Optional|**String**|The task field to display below the Gantt bar.|
| _TopText_|Optional|**String**|The task field to display above the Gantt bar.|
| _LeftText_|Optional|**String**|The task field to display to the left of the Gantt bar.|
| _RightText_|Optional|**String**|The task field to display to the right of the Gantt bar.|
| _InsideText_|Optional|**String**|The task field to display inside the Gantt bar.|

## Return value

 **Boolean**


## Remarks

To manually show the **Bar Styles** dialog box, click the **Format** tab under the **Gantt Chart Tools** tab. In the **Bar Styles** group, click **Bar Styles** in the **Format** drop-down list. The **Bar Styles** dialog box can contain up to 200 style entries.


## Example

The following example creates a bar style that has a light green color and ends with a star shape.


```vb
Sub CreateGanttBar() 
    GanttBarEditEx Item:=-1, Create:=True, Name:="My New Bar Style", _
        MiddleColor:=&H88FF88, EndShape:=pjStar 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]