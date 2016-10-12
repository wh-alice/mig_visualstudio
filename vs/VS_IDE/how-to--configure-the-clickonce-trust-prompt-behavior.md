---
title: "How to: Configure the ClickOnce Trust Prompt Behavior"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-deployment"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "ClickOnce deployment, install without prompting"
  - "deploying applications [ClickOnce], trust prompt"
  - "ClickOnce applications, install without prompting"
  - "ClickOnce applications, trust prompt"
  - "ClickOnce deployment, trust prompt"
ms.assetid: cc04fa75-012b-47c9-9347-f4216be23cf2
caps.latest.revision: 11
ms.author: "shoag"
manager: "wpickett"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# How to: Configure the ClickOnce Trust Prompt Behavior
You can configure the ClickOnce trust prompt to control whether end users are given the option of installing ClickOnce applications, such as Windows Forms applications, Windows Presentation Foundation applications, console applications, WPF browser applications, and Office solutions. You configure the trust prompt by setting registry keys on each end user's computer.  
  
 The following table shows the configuration options that can be applied to each of the five zones (Internet, UntrustedSites, MyComputer, LocalIntranet, and TrustedSites).  
  
|Option|Registry setting value|Description|  
|------------|----------------------------|-----------------|  
|Enable the trust prompt.|`Enabled`|The ClickOnce trust prompt is display so that end users can grant trust to ClickOnce applications.|  
|Restrict the trust prompt.|`AuthenticodeRequired`|The ClickOnce trust prompt is only displayed if ClickOnce applications are signed with a certificate that identifies the publisher.|  
|Disable the trust prompt.|`Disabled`|The ClickOnce trust prompt is not displayed for any ClickOnce applications that are not signed with an explicitly trusted certificate.|  
  
 The following table shows the default behavior for each zone. The Applications column refers to Windows Forms applications, Windows Presentation Foundation applications, WPF browser applications, and console applications.  
  
|Zone|Applications|Office solutions|  
|----------|------------------|----------------------|  
|`MyComputer`|`Enabled`|`Enabled`|  
|`LocalIntranet`|`Enabled`|`Enabled`|  
|`TrustedSites`|`Enabled`|`Enabled`|  
|`Internet`|`Enabled`|`AuthenticodeRequired`|  
|`UntrustedSites`|`Disabled`|`Disabled`|  
  
 You can override these settings by enabling, restricting, or disabling the ClickOnce trust prompt.  
  
## Enabling the ClickOnce Trust Prompt  
 Enable the trust prompt for a zone when you want end users to be presented with the option of installing and running any ClickOnce application that comes from that zone.  
  
#### To enable the ClickOnce trust prompt by using the registry editor  
  
1.  Open the registry editor:  
  
    1.  Click **Start**, and then click **Run**.  
  
    2.  In the **Open** box, type `regedit32`, and then click **OK**.  
  
2.  Find the following registry key:  
  
     \HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\.NETFramework\Security\TrustManager\PromptingLevel  
  
     If the key does not exist, create it.  
  
3.  Add the following subkeys as **String Value**, if they do not already exist, with the associated values shown in the following table.  
  
    |String Value subkey|Value|  
    |-------------------------|-----------|  
    |`Internet`|`Enabled`|  
    |`UntrustedSites`|`Disabled`|  
    |`MyComputer`|`Enabled`|  
    |`LocalIntranet`|`Enabled`|  
    |`TrustedSites`|`Enabled`|  
  
     For Office solutions, `Internet` has the default value `AuthenticodeRequired` and `UntrustedSites` has the value `Disabled`. For all others, `Internet` has the default value `Enabled`.  
  
#### To enable the ClickOnce trust prompt programmatically  
  
1.  Create a Visual Basic or Visual C# console application in Visual Studio.  
  
2.  Open the Program.vb or Program.cs file for editing and add the following code.  
  
    ```vb#  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "Enabled")  
    key.SetValue("LocalIntranet", "Enabled")  
    key.SetValue("Internet", "Enabled")  
    key.SetValue("TrustedSites", "Enabled")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```c#  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "Enabled");  
    key.SetValue("LocalIntranet", "Enabled");  
    key.SetValue("Internet", "AuthenticodeRequired");  
    key.SetValue("TrustedSites", "Enabled");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
    ```  
  
3.  Build and run the application.  
  
## Restricting the ClickOnce Trust Prompt  
 Restrict the trust prompt so that solutions must be signed with Authenticode certificates that have known identity before users are prompted for a trust decision.  
  
#### To restrict the ClickOnce trust prompt by using the registry editor  
  
1.  Open the registry editor:  
  
    1.  Click **Start**, and then click **Run**.  
  
    2.  In the **Open** box, type `regedit`, and then click **OK**.  
  
2.  Find the following registry key:  
  
     \HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\.NETFramework\Security\TrustManager\PromptingLevel  
  
     If the key does not exist, create it.  
  
3.  Add the following subkeys as **String Value**, if they do not already exist, with the associated values shown in the following table.  
  
    |String Value subkey|Value|  
    |-------------------------|-----------|  
    |`UntrustedSites`|`Disabled`|  
    |`Internet`|`AuthenticodeRequired`|  
    |`MyComputer`|`AuthenticodeRequired`|  
    |`LocalIntranet`|`AuthenticodeRequired`|  
    |`TrustedSites`|`AuthenticodeRequired`|  
  
#### To restrict the ClickOnce trust prompt programmatically  
  
1.  Create a Visual Basic or Visual C# console application in Visual Studio.  
  
2.  Open the Program.vb or Program.cs file for editing and add the following code.  
  
    ```vb#  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "AuthenticodeRequired")  
    key.SetValue("LocalIntranet", "AuthenticodeRequired")  
    key.SetValue("Internet", "AuthenticodeRequired")  
    key.SetValue("TrustedSites", "AuthenticodeRequired")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```c#  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "AuthenticodeRequired");  
    key.SetValue("LocalIntranet", "AuthenticodeRequired");  
    key.SetValue("Internet", "AuthenticodeRequired");  
    key.SetValue("TrustedSites", "AuthenticodeRequired");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
    ```  
  
3.  Build and run the application.  
  
## Disabling the ClickOnce Trust Prompt  
 You can disable the trust prompt so that end users are not given the option to install solutions that are not already trusted in their security policy.  
  
#### To disable the ClickOnce trust prompt by using the registry editor  
  
1.  Open the registry editor:  
  
    1.  Click **Start**, and then click **Run**.  
  
    2.  In the **Open** box, type `regedit`, and then click **OK**.  
  
2.  Find the following registry key:  
  
     \HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\.NETFramework\Security\TrustManager\PromptingLevel  
  
     If the key does not exist, create it.  
  
3.  Add the following subkeys as **String Value**, if they do not already exist, with the associated values shown in the following table.  
  
    |String Value subkey|Value|  
    |-------------------------|-----------|  
    |`UntrustedSites`|`Disabled`|  
    |`Internet`|`Disabled`|  
    |`MyComputer`|`Disabled`|  
    |`LocalIntranet`|`Disabled`|  
    |`TrustedSites`|`Disabled`|  
  
#### To disable the ClickOnce trust prompt programmatically  
  
1.  Create a Visual Basic or Visual C# console application in Visual Studio.  
  
2.  Open the Program.vb or Program.cs file for editing and add the following code.  
  
    ```vb#  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "Disabled")  
    key.SetValue("LocalIntranet", "Disabled")  
    key.SetValue("Internet", "Disabled")  
    key.SetValue("TrustedSites", "Disabled")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```c#  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "Disabled");  
    key.SetValue("LocalIntranet", "Disabled");  
    key.SetValue("Internet", "Disabled");  
    key.SetValue("TrustedSites", "Disabled");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
  
    ```  
  
3.  Build and run the application.  
  
## See Also  
 [Securing ClickOnce Applications](../VS_IDE/securing-clickonce-applications.md)   
 [Code Access Security for ClickOnce Applications](../VS_IDE/code-access-security-for-clickonce-applications.md)   
 [ClickOnce and Authenticode](../VS_IDE/clickonce-and-authenticode.md)   
 [Trusted Application Deployment Overview](../VS_IDE/trusted-application-deployment-overview.md)   
 [How to: Enable ClickOnce Security Settings](../VS_IDE/how-to--enable-clickonce-security-settings.md)   
 [How to: Set a Security Zone for a ClickOnce Application](../VS_IDE/how-to--set-a-security-zone-for-a-clickonce-application.md)   
 [How to: Set Custom Permissions for a ClickOnce Application](../VS_IDE/how-to--set-custom-permissions-for-a-clickonce-application.md)   
 [How to: Debug a ClickOnce Application with Restricted Permissions](../VS_IDE/how-to--debug-a-clickonce-application-with-restricted-permissions.md)   
 [How to: Add a Trusted Publisher to a Client Computer for ClickOnce Applications](../VS_IDE/how-to--add-a-trusted-publisher-to-a-client-computer-for-clickonce-applications.md)   
 [How to: Re-sign Application and Deployment Manifests](../VS_IDE/how-to--re-sign-application-and-deployment-manifests.md)