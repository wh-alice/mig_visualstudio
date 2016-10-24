---
title: "Application Page, Project Designer (C#) | testtitle"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "cs.ProjectPropertiesApplicationWPF"
  - "cs.ProjectPropertiesApplication"
helpviewer_keywords: 
  - "Project Designer, Application page"
  - "Application page in Project Designer"
ms.assetid: f13701a8-4e2e-4474-9d60-bb43decbe0c1
caps.latest.revision: 56
ms.author: "kempb"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Application Page, Project Designer (C#)
Use the **Application** page of the **Project Designer** to specify the project's application settings and properties.  
  
 To access the **Application** page, choose a project node (not the **Solution** node) in **Solution Explorer**. Then choose **Project**, **Properties** on the menu bar. When the Project Designer appears, click the **Application** tab.  
  
 [!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]  
  
## General Application Settings  
 The following options enable you to configure general settings for the application.  
  
 **Assembly name**  
 Specifies the name of the output file that will hold the assembly manifest. Changing this property will also change the **Output Name** property. You can also make this change from the command line by using [/out (C# Compiler Options)](../Topic/-out%20\(C%23%20Compiler%20Options\).md). To access this property programmatically, see <xref:VSLangProj.ProjectProperties.AssemblyName*>.  
  
 **Default namespace**  
 Specifies the base namespace for files added to the project.  
  
 See [namespace](../Topic/namespace%20\(C%23%20Reference\).md) for more information about creating namespaces in your code.  
  
 To access this property programmatically, see <xref:VSLangProj.ProjectProperties.RootNamespace*>.  
  
 **Target Framework**  
 Specifies the version of the .NET Framework that the application targets. This option can have different values depending on which versions of the .NET Framework are installed on your computer.  
  
 By default, the value is the same as the target framework that you selected in the **New Project** dialog box.  
  
> [!NOTE]
>  The prerequisite packages listed in the [Prerequisites Dialog Box](../reference/prerequisites-dialog-box.md) are set automatically the first time that you open the dialog box. If you subsequently change the project's target framework, you will have to select the prerequisites manually to match the new target framework.  
  
 For more information, see [How to: Target a Version of the .NET Framework](../ide/how-to--target-a-version-of-the-.net-framework.md) and [Visual Studio Multi-Targeting Overview](../ide/visual-studio-multi-targeting-overview.md).  
  
 **Application type**  
 Specifies the type of application to build. For [!INCLUDE[win8_appname_long](../code-quality/includes/win8_appname_long_md.md)] apps, you can specify **Windows Store App**, **Class Library**, or **WinMD File**. For most other application types, you can specify **Windows Application**, **Console Application**, **Class Library**, **Windows Service**, or **Web Control Library**.  
  
 For a web application project, you must specify **Class Library**.  
  
 If you specify the **WinMD File** option, types can be projected into any Windows Runtime programming language. By packaging the project's output as a WinMD file, you can code an application in multiple languages and have code interoperate as if you wrote it all in the same language. You can specify this option for solutions that target the Windows Runtime libraries, including [!INCLUDE[win8_appname_long](../code-quality/includes/win8_appname_long_md.md)] apps. For more information, see [Creating Windows Runtime Components in C# and Visual Basic](http://go.microsoft.com/fwlink/?LinkId=231895).  
  
> [!NOTE]
>  The Windows Runtime can project types so that they appear as native objects in whichever language uses them. For example, JavaScript applications that interact with Windows Runtime use it as a set of JavaScript objects, and C# applications use the library as a collection of .NET objects. By packaging the project’s output as a WinMD file, you can take advantage of the same technology that Windows Runtime uses.  
  
 For more information about the **Application type** property, see [/target (C# Compiler Options)](../Topic/-target%20\(C%23%20Compiler%20Options\).md). For information about how to access this property programmatically, see <xref:VSLangProj.ProjectProperties.OutputType*>.  
  
 **Assembly Information**  
 Clicking this button displays the [Assembly Information Dialog Box](../reference/assembly-information-dialog-box.md).  
  
 **Startup object**  
 Defines the entry point to be called when the application loads. Generally this is set either to the main form in your application or to the `Main` procedure that should run when the application starts. Because class libraries do not have an entry point, their only option for this property is **(Not Set)**.  
  
 By default, in a WPF Browser Application project, this option is **(Not set)**. The other option is *Projectname*.App. In this kind of project, you have to set the startup URI to load a UI resource when the application starts. To do this, open the Application.xaml file in your project and set the `StartupUri` property to a .xaml file in your project, such as Window1.xaml. For a list of acceptable root elements, see <xref:System.Windows.Application.StartupUri*>. You also have to define a `public static void Main()` method in a class in the project. This class will appear in the **Startup object** list as *ProjectName.ClassName*. You can then select the class as the startup object.  
  
 See [/main (C# Compiler Options)](../Topic/-main%20\(C%23%20Compiler%20Options\).md) for more information. To access this property programmatically, see <xref:VSLangProj.ProjectProperties.StartupObject*>.  
  
## Resources  
 The following options enable you to configure general settings for the application.  
  
 **Icon and manifest**  
 By default, this radio button is selected and the **Icon** and **Manifest** options are enabled. This enables you to select your own icon, or to select different manifest generation options. Leave this radio button selected unless you are providing a resource file for the project.  
  
 **Icon**  
 Sets the .ico file that you want to use as your program icon. Click the ellipsis button to browse for an existing graphic, or type the name of the file that you want. See [/win32icon (C# Compiler Options)](../Topic/-win32icon%20\(C%23%20Compiler%20Options\).md) for more information. To access this property programmatically, see <xref:VSLangProj.ProjectProperties.ApplicationIcon*>.  
  
 **Manifest**  
 Selects a manifest generation option when the application runs on Windows Vista under User Account Control (UAC). This option can have the following values:  
  
-   **Embed manifest with default settings**. Supports the typical manner in which Visual Studio operates on Windows Vista, which is to embed security information in the application's executable file, specifying that `requestedExecutionLevel` be `AsInvoker`. This is the default option.  
  
-   **Create application without a manifest**. This method is known as *virtualization*. Use this option for compatibility with earlier applications.  
  
-   **Properties\app.manifest**. This option is required for applications deployed by ClickOnce or Registration-Free COM. If you publish an application by using ClickOnce deployment, **Manifest** is automatically set to this option.  
  
 **Resource File**  
 Select this radio button when you are providing a resource file for the project. Selecting this option disables the **Icon** and **Manifest** options.  
  
 Enter a path name or use the Browse button (**...**) to add a Win32 resource file to the project.  
  
## See Also  
[Managing Application Properties](../ide/application-properties.md)  
 [Writing Code in Office Solutions](../Topic/Writing%20Code%20in%20Office%20Solutions.md)