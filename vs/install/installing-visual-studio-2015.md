---
title: "Installing Visual Studio 2015 | Microsoft Docs"
ms.custom: ""
ms.date: "2016-10-12"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-install"
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
f1_keywords: 
  - "vs.about"
helpviewer_keywords: 
  - "Visual Studio, installing"
  - "installing Visual Studio"
  - "server installations [Visual Studio]"
  - "Setup [Visual Studio]"
  - "install Visual Studio"
  - "visual studio installer"
ms.assetid: da049020-cfda-40d7-8ff4-7492772b620f
caps.latest.revision: 173
ms.author: "tglee"
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
# Installing Visual Studio 2015
This page includes detailed information to help you with installing Visual Studio, our integrated suite of productivity tools for developers. We've also included links to get you quickly to information about [features](https://www.visualstudio.com/news/vs2015-vs.aspx), [editions](http://go.microsoft.com/fwlink/?LinkID=242142), [system requirements](https://www.visualstudio.com/products/visual-studio-2015-compatibility-vs), [downloads](http://go.microsoft.com/fwlink/?LinkId=517106), and more.  
  
 (To view installation information about previous versions of Visual Studio, click the "Other Versions" link at the top of this page. And, to view installation information about the next version of Visual Studio, see our [Installing Visual Studio "15" Preview 5](../install/installing-visual-studio--15--preview-5.md) page.
## Quick Links  
 Before we dig in to the details, here's a list of our most frequently requested links.  
  
|||  
|------------------|----------------| 
|![Learn more about features](../install/media/features.png "Features") |**Features**: To learn  more about new or updated features in Visual Studio 2015, see the release notes for [RTM](https://www.visualstudio.com/news/vs2015-vs), [Update 1](https://www.visualstudio.com/news/vs2015-update1-vs), [Update 2](https://www.visualstudio.com/news/vs2015-update2-vs), and [Update 3](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs).|  
|![Find out what's in each SKU](../install/media/sku.png "SKUs") |**SKUs**: To find out what's available in each edition of Visual Studio 2015, see our [Compare Visual Studio Offerings](http://go.microsoft.com/fwlink/?LinkID=242142) page.|  
|![View system requirements](../install/media/system-requirements.png "System Requirements") |**System Requirements**: To view the system requirements for each edition of Visual Studio 2015, see the [Visual Studio 2015 Compatibility](https://www.visualstudio.com/products/visual-studio-2015-compatibility-vs) page.|  
|![Download Visual Studio](../install/media/downloads.png "Downloads") |**Downloads**: To install Visual Studio, you can download the web installer from the [Visual Studio Downloads](http://go.microsoft.com/fwlink/?LinkId=517106) page, or you can download a product executable file from the  [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015) page (subscription required), or use the installation media from the boxed product.|  
|![Locate your Product Key](../install/media/product-keys.png "Product Keys") |**Product Keys**: To locate your product key, see the [How to: Locate the Visual Studio Product Key](../install/how-to--locate-the-visual-studio-product-key.md) topic.|  
|![Find out about licensing](../install/media/licensing.png "Licensing") |**Licensing**: To find out about licensing options for both individuals or enterprise customers, see  the [Visual Studio and MSDN Licensing](https://www.microsoft.com/download/details.aspx?id=13350) white paper.|  
  
##  <a name="custom"></a> Default vs. Custom Setup  
 When you install Visual Studio 2015, you can  include or exclude components that you'd use on a daily basis. This means that a Default installation will often be smaller and install faster than a Custom installation. It also means that many components that were installed by default in previous versions now are considered Custom components that you must explicitly select in this version.  
  
 ![Visual Studio 2015 Setup Dialog](../ide/media/vs2015_setup_screen.png "VS2015_Setup_screen")  
  
 Custom components include Visual C++, Visual F#, SQL Server Data Tools, Cross-platform mobile tools and SDKs, and third-party SDKs and extensions. You can install any of the custom components at a later time if you don't select them during the initial setup.  
  
> [!NOTE]
>  A Custom installation automatically includes the components that are in a Default installation.  
  
 The complete list of Custom components is as follows:  
  
|Feature Sets|Components|  
|------------------|----------------|  
|**Updates**|Visual Studio 2015 Update 3|  
|**Programming Languages**|Visual C++<br />Visual F#<br />Python Tools for Visual Studio|  
|**Windows and Web Development**|ClickOnce Publishing Tools<br />LightSwitch<br />Microsoft Office Developer Tools<br />Microsoft SQL Server Data Tools<br /> Microsoft Web Developer Tools<br />PowerShell Tools for Visual Studio (3rd Party)<br />Silverlight Development Kit<br />Universal Windows App Development Tools<br />Windows 10 Tools and SDKs<br />Windows 8.1 and Windows Phone 8.0/8.1 Tools<br />Windows 8.1 Tools and SDKs|  
|**Cross Platform Mobile Development**|C#/.NET (Xamarin)<br />HTML/JavaScript (Apache Cordova)<br />Visual C++ Mobile Development for iOS / Android<br />Clang with Microsoft CodeGen|  
|**Common Tools and Software Development Kits**|Android Native Development Kit (3rd Party)<br /> Android SDK [3rd Party]<br />Android SDK Setup APIs (3rd Party)<br />Apache Ant (3rd Party)<br /> Java SE Development Kit (3rd Party)<br /> Joyent Node.js (3rd Party)|  
|**Common Tools**|Git for Windows (3rd Party)<br />GitHub Extension for Visual Studio (3rd Party)<br /> Visual Studio Extensibility Tools|  
  
##  <a name="installing"></a> Installing Visual Studio  
 You can install Visual Studio by using installation media (DVDs), by using your Visual Studio subscription service from the [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015) website, by downloading  a web installer from the [Visual Studio Downloads](http://go.microsoft.com/fwlink/?LinkId=517106) website, or by creating an offline installation layout (see the [Creating an Offline Installation of Visual Studio](../install/creating-an-offline-installation-of-visual-studio.md) topic for more details).  
  
> [!IMPORTANT]
>  You need administrator credentials to install [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. However, you don't need them to use [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] after you install it.  
  
 Your local administrator account must have the following privileges enabled to install everything in Visual Studio.  
  
|Local Policy Object Display Name|User Right|  
|--------------------------------------|----------------|  
|Backup Files and directories|SeBackupPrivilege|  
|Debug programs|SeDebugPrivilege|  
|Manage auditing and security log|SeSecurityPrivilege|  
  
 For more information on this local administrator account requirement, see the Knowledge Base article, [SQL Server installation fails if the Setup account does not have certain user rights](https://support.microsoft.com/en-us/kb/2000257).  
  
###  <a name="BKMK_Media"></a> Using installation media  
 To install [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], in the root directory on the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] installation media, run the installation file for the edition you want:  
  
|Edition|Installation File|  
|-------------|-----------------------|  
|Visual Studio Enterprise|vs_enterprise.exe|  
|Visual Studio Professional|vs_professional.exe|  
|Visual Studio Community|vs_community.exe|  
  
###  <a name="BKMK_Website"></a> Downloading from the product website  
 Visit the [Visual Studio Downloads](http://go.microsoft.com/fwlink/?LinkId=517106) page, and select the edition of Visual Studio that you want.  
  
### Downloading from your subscription service  
 Visit  the [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015) page, and select the edition of Visual Studio that you want.  
  
###  <a name="BKMK_Offline"></a> Creating an offline installation  layout  
 If you do not have the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] installation media, or you do not have a Visual Studio subscription,  or you do not want to install [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] by using the web installer, you can perform a "disconnected" installation by creating what is known as an offline installation layout. For more information, see the [Creating an Offline Installation of Visual Studio](../install/creating-an-offline-installation-of-visual-studio.md) topic.  
  
##  <a name="enterprise"></a> Deploying Visual Studio in an Enterprise  
 For information about how to deploy [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] over a network, see the [Visual Studio Administrator Guide](../install/visual-studio-administrator-guide.md).  
  
###  <a name="BKMK_Virtualized"></a> Installing Visual Studio in a virtualized environment  
 **Video Issues with Hyper-V**  
  
 If you run Windows Server 2008 R2 with Hyper-V enabled and an accelerated graphics adapter, you may experience system slowdowns.  
  
 For more information, see the following page on the Microsoft website: [Video performance may decrease when a Windows Server 2008 or Windows Server 2008 R2 based computer has the Hyper-V role enabled and an accelerated display adapter installed](http://go.microsoft.com/fwlink/?LinkID=231084).  
  
 **Emulating Devices with Hyper-V**  
  
 When you install Visual Studio 2015 on real hardware without virtualization, you can choose features that enable emulation of Windows and Android devices using Hyper-V. When you install into Hyper-V, you will not be able to emulate the Windows or Android devices. This is because the emulators are themselves virtual machines, and you cannot currently host a VM inside another VM. The workaround is to have real Windows or Android devices to which you can directly deploy and debug your application.  
  
##  <a name="optionalComponents"></a> Installing optional components  
 If you want to install components that you might not have selected during your original installation, use the following procedure.  
  
#### To install optional components  
  
1.  In **Control Panel**, on the **Programs and Features** page, choose the product edition to which you want to add one or more components, and then choose **Change**.  
  
2.  In the Setup wizard, choose **Modify**, and then choose the components that you want to install.  
  
3.  Choose **Next**, and then follow the remaining instructions.  
  
##  <a name="helpContent"></a> Installing offline Help content  
 After you install [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], you can download additional Help content so that it will be available offline.  
  
#### To install or uninstall Help content  
  
1.  On the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] menu bar, choose **Help**, **Add and Remove Help Content**.  
  
2.  On the **Manage Content** tab of the **Microsoft Help Viewer**, select the installation source for your Help content.  
  
3.  If you're looking for a specific Help collection, enter the name or a keyword in the **Search** text box, and then press **Enter**.  
  
4.  Next to the name of the Help collection you want, choose the **Add** or **Remove** link.  
  
5.  Click the **Update** button.  
  
 For more information about how to install or deploy offline Help, see the [Help Viewer Administrator Guide](../ide/help-viewer-administrator-guide.md).  
  
##  <a name="serviceReleases"></a> Checking for Service Releases and Product Updates  
 Because not all extensions are compatible, Visual Studio doesn't automatically upgrade extensions when you upgrade from previous versions. You must reinstall the extensions from the [Visual Studio Gallery](http://go.microsoft.com/fwlink/?LinkId=178891) or from the software publisher.  
  
#### To automatically check for service releases  
  
1.  On the menu bar, choose **Tools**, **Options**.  
  
2.  In the **Options** dialog box, expand **Environment**, and then select **Extensions and Updates**. Make sure the **Automatically check for updates** check box is selected, and then choose **OK**.  
  
## Registering Visual Studio  
  
1.  On the menu bar, choose **Help**, **About**.  
  
     The **About** dialog box shows the product identification number (PID). You'll need the PID and Windows Account credentials (such as a Hotmail or Outlook.com email address and password) to register the product.  
  
2.  On the menu bar, choose **Help**, **Register Product**.  
  
##  <a name="repair"></a> Repairing Visual Studio  
  
#### To repair Visual Studio  
  
1.  In **Control Panel**, on the **Programs and Features** page, choose the product edition that you want to repair, and then choose **Change**.  
  
2.  In the Setup wizard, choose **Repair**, choose **Next**, and then follow the remaining instructions.  
  
#### To repair Visual Studio in silent or passive modes (that is, to repair from source)  
  
1.  On the computer where Visual Studio is installed, open the Windows command prompt.  
  
2.  Enter the following parameters:  
  
     *DVDRoot* \\<Installation File\> \</quiet&#124;/passive> [/norestart]/Repair  
  
##  <a name="troubleshooting"></a> Troubleshooting an installation  
 Use these resources to get help for setup and installation issues:  
  
-   [Visual Studio Setup and Installation](http://go.microsoft.com/fwlink/?LinkID=151190) forum. Review questions and answers from others in the Visual Studio community. If you don't find what you need, ask your own questions.  
  
-   [Microsoft Support for Visual Studio](http://go.microsoft.com/fwlink/?LinkID=251019) website. Read knowledge base (KB) articles and learn how to contact Microsoft Support for information about issues with Visual Studio installation.  
  
-   For releases of Visual Studio 2015, you can report your issue by using the Connect site at [https://connect.microsoft.com/visualstudio](https://connect.microsoft.com/visualstudio).  
  
     It’s best if your issue includes the installation logs. You can prepare your logs for the issue report by using the Microsoft Visual Studio and .NET Framework Log Collection Tool, as described in the following steps.  
  
    1.  Download the installation diagnostic tool from [http://aka.ms/vscollect](http://aka.ms/vscollect).  
  
    2.  From an elevated command prompt, run the collect.exe program.  
  
    3.  After the collect.exe program completes, fetch the vslogs.cab file from your Temp directory and upload that into the issue report.  
  
##  <a name="relatedTopics"></a> Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Installing Visual Studio Versions Side-by-Side](../install/installing-visual-studio-versions-side-by-side.md)|Provides information about how to install multiple versions of Visual Studio on the same computer.|  
|[Using Command-Line Parameters to Install Visual Studio](../install/using-command-line-parameters-to-install-visual-studio.md)|Lists the command-line parameters that you can use when you install Visual Studio from a command prompt.|  
|[Uninstalling Visual Studio](../install/uninstalling-visual-studio.md)|Describes how to uninstall Visual Studio.|  
|[Visual Studio Administrator Guide](../install/visual-studio-administrator-guide.md)|Provides information about deployment options for Visual Studio.|  
|[Installing Multiple Language Versions of Visual Studio](../install/installing-multiple-language-versions-of-visual-studio.md)|Provides information about how to install different language versions of Visual Studio.|  
|[How to: Locate the Visual Studio Product Key](../install/how-to--locate-the-visual-studio-product-key.md)|Describes how to locate the product key for your installation of Visual Studio.|  
|[The Visual Studio Image Library](../designers/the-visual-studio-image-library.md)|Provides information about how to install graphics that you can use in Visual Studio applications.|  
|[Get Started Developing with Visual Studio](../ide/get-started-developing-with-visual-studio.md)|Provides information and links that can help you use Visual Studio more effectively.|  
  
## See Also  
 [Signing in to Visual Studio](../ide/signing-in-to-visual-studio.md)