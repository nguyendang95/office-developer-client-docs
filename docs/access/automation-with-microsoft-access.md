---
title: "Automation with Microsoft Access"
  
  
manager: soliver
ms.date: 7/29/2015
ms.audience: Developer
 
f1_keywords:
- vbaac10.chm13783
  
localization_priority: Normal
ms.assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
description: "Microsoft Access is a COM component that supports Automation, formerly called OLE Automation. Microsoft Access supports Automation in two ways. From Microsoft Access, you can work with objects supplied by another component. Microsoft Access also supplies its objects to other COM components."
---

# Automation with Microsoft Access

Microsoft Access is a COM component that supports Automation, formerly called OLE Automation. Microsoft Access supports Automation in two ways. From Microsoft Access, you can work with objects supplied by another component. Microsoft Access also supplies its objects to other COM components.
  
You can use the **New** keyword or the **CreateObject** method to create a new instance of a component. You can use the **GetObject** method to assign a variable to an existing instance of a component. 
  
In Microsoft Access, you can set a reference to a component's type library to improve performance when you work with that component through Automation. Microsoft Access also includes the Object Browser, a tool that enables you to view objects in another component's type library, as well as their methods and properties.
  
The Microsoft Access type library provides information about Microsoft Access objects to other components. You can [set a reference](http://msdn.microsoft.com/library/6314a89b-89e9-d8c1-5964-889a361afcd1%28Office.15%29.aspx)to the Microsoft Access type library from a component and view its objects in the Object Browser.
  
To work with Microsoft Access objects through Automation, you must create an instance of the Microsoft Access **[Application](http://msdn.microsoft.com/library/aefb0713-97e6-e2c7-e530-8fd2e1316a55%28Office.15%29.aspx)** object. For example, suppose you want to display data from Microsoft Excel in a Microsoft Access form or report. To launch Microsoft Access from Microsoft Excel, you can use the **New** keyword to create an instance of the Microsoft Access **Application** object. You can also use the **CreateObject** method to create a new instance of the Microsoft Access **Application** object, or you can use the **GetObject** method to point an object variable to an existing instance of Microsoft Access. Check your component's documentation to determine which syntax it supports. 
  
Once you've launched an instance of Microsoft Access, if you want to control any Microsoft Access objects, you must open a database or project (.adp) in the Microsoft Access window by using either the **[OpenCurrentDatabase](http://msdn.microsoft.com/library/fd214849-02ac-eaa6-7525-9aee42b92f3d%28Office.15%29.aspx)** or the **[NewCurrentDatabase](http://msdn.microsoft.com/library/6934a77e-5fa0-7e43-e159-2ffc2a944dca%28Office.15%29.aspx)** method for a database or by using the **[OpenAccessProject](http://msdn.microsoft.com/library/fdc1b231-1512-cbcd-f376-935555861b38%28Office.15%29.aspx)** or the **[NewAccessProject](http://msdn.microsoft.com/library/e3b3b9ef-31f8-885c-5c92-d269b824fbdb%28Office.15%29.aspx)** method for a project. 
  
If you've opened Microsoft Access only as a means of using the Data Access Objects provided by Microsoft DAO, then you don't need to open a database in the Microsoft Access window. You can use the **[DBEngine](http://msdn.microsoft.com/library/ad4638e4-0c72-ce24-e322-e147e2f0cfc2%28Office.15%29.aspx)** property of the Microsoft Access **Application** object to access objects in the Microsoft Office 12.0 Access Database Engine Object Library object library during an Automation operation. 
  
