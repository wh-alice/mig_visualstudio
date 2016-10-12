---
title: "Debugging a T4 Text Template"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "text templates, troubleshooting"
  - "text templates, debugging"
ms.assetid: 0877fdf2-20bf-42da-b3cc-4c5856b80821
caps.latest.revision: 28
ms.author: "awills"
manager: "kamrani"
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
# Debugging a T4 Text Template
You can set breakpoints in text templates. To debug a design-time text template, save the text template file, and then choose **Debug T4 Template** on the shortcut menu of the file in Solution Explorer. To debug a run-time text template, simply debug the application to which it belongs.  
  
 To debug a text template, you should understand the steps of the template transformation process. Different kinds of errors can occur within each step. The steps are as follows.  
  
|Step|Design-time template: when it happens|Run-time template: when it happens|  
|----------|--------------------------------------------|-----------------------------------------|  
|Code is generated from the text template.<br /><br /> Errors in directives, or mismatched or disordered `<#…#>` tags.|When you save the template or invoke text transformation.|When you save the template or invoke text transformation.|  
|Generated code is compiled.<br /><br /> Compilation errors in your template code.|Immediately after the previous step.|Along with your application code.|  
|Code runs.<br /><br /> Run-time errors in your template code.|Immediately after the previous step.|When your application runs and invokes the template code.|  
  
 In most cases, line numbers in the template code are given in the error report. When the error report refers to a temporary filename, the usual cause is a mismatched bracket in the code of the text template.  
  
 You can set breakpoints in text templates and debug in the usual way.  
  
## Common Errors and Fixes  
 The following table lists the most common errors and their fixes.  
  
|Error Message|Description|Solution|  
|-------------------|-----------------|--------------|  
|Failed to load base class '{0}' from which Transformation class inherits.|Occurs if you cannot find the base class specified in the `inherits` parameter in a template directive. The message provides the line number of the template directive.|Be sure the specified class exists, and that the assembly that it exists in is specified in an assembly directive.|  
|Failed to resolve include text for file:{0}|Occurs when you cannot find an included template. The message provides the name of the requested include file.|Be sure that the file path is relative to the original template path, or that the file is in a location that is registered with the host, or that there is a full path to the file.|  
|Errors were generated when initializing the transformation object. The transformation will not be run.|Occurs when the 'Initialize()' of the transformation class failed or returned false.|The code in the Initialize() function comes from the base transformation class specified in the \<#@template#> directive and from directive processors. The error that caused initialize to fail probably is on the error list. Investigate why it failed. You can look at the actual generated code for Initialize() by following the procedures to debug a template.|  
|The assembly '{0}' for directive processor '{1}' was not granted the FullTrust permission set. Only trusted assemblies are allowed to provide directive processors. This directive processor will not be loaded.|Occurs when the system does not grant FullTrust permissions to an assembly containing a directive processor. The message provides the name of the assembly and the name of the directive processor.|Be sure that you only use trusted assemblies on the local machine.|  
|The path '{0}' must be either local to this computer or part of your trusted zone.|Occurs when a directive or assembly directive references a file that is not on your local machine or on your network's trusted zone.|Be sure that the directory where the directive or assembly directives are located is in your trusted zone. You can add a network directory to your trusted zone through Internet Explorer.|  
|Multiple syntax errors such as "Invalid token 'catch'" or "A namespace cannot directly contain members"|Too many closing braces in your template code. The compiler is confusing it with the standard generation code.|Check the number of closing braces and brackets inside code delimiters.|  
|Loops or conditionals not compiled or executed correctly. For example: `<#if (i>10)#> Number is: <#= i #>`.<br /><br /> This code always outputs the value of i. Only "Number is:" is conditional.|In C#, always use braces to surround text blocks that are embedded in control statements.|Add braces: `<#if (i>10) { #>    Number is: <#= i #><# } #>`.|  
|"Expression too complex" when processing a design-time template or compiling a runtime (preprocessed) template.<br /><br /> [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] stops working when attempting to inspect code generated by a runtime template.|Text block is too long. T4 converts text blocks to a string concatenation expression, with one string literal for each template line. Very long text blocks can overstep the compiler’s size limits.|Break up the long text block with an expression block such as:<br /><br /> `<#= "" #>`|  
  
## Warning Descriptions and Fixes  
 The following table lists the most common warnings together with fixes, if available.  
  
|Warning Message|Description|Solution|  
|---------------------|-----------------|--------------|  
|Loading the include file '{0}' returned a null or empty string.|Occurs if an included text template file is blank. The message provides the file name of the included file.|Either remove the include directive or be sure the file has some content.|  
|Compiling transformation:|Prepends this string to all errors or warnings originating from the compiler when it compiles the transformation. This string means that the compiler threw an error or warning.|If you have a problem finding the DLL, you may need to provide either the full path or a fully qualified strong name if the DLL is in the GAC.|  
|The parameter '{0}' already exists in the directive. The duplicate parameter will be ignored.|Occurs when a parameter is specified more than once in a directive. The message provides the name of the parameter and the line number of the directive.|Remove the duplicate parameter specification.|  
|There was an error loading the include file '{0}'. The include directive will be ignored.|Occurs when you cannot find a file specified in an `include` directive. The message provides the name of the file and the line number of the directive.|Be sure the include file exists either in the same directory as the original text template file or in one of the include directories that are registered with the host.|  
|An invalid base class was specified for the Transformation class. The base class must derive from Microsoft.VisualStudio.TextTemplating.TextTransformation.|Occurs when the `inherits` parameter in a template directive specifies a class that does not inherit from `TextTransformation`. The message provides the line number of the template directive.|Specify a class that derives from `TextTransformation`.|  
|An invalid culture was specified in the 'template' directive. The culture must be in the "xx-XX" format. The invariant culture will be used.|Occurs when the culture parameter in a template directive is specified incorrectly. The message provides the line number of the template directive.|Change the culture parameter to a valid culture in the "xx-XX" format.|  
|An invalid debug value '{0}' was specified in the template directive. The debug value must be either "true" or "false". The default of "false" will be used.|Occurs when the `debug` parameter in a template directive is specified incorrectly. The message provides the line number of the template directive.|Set the debug parameter to "true" or "false".|  
|An invalid HostSpecific value '{0}' was specified in the template directive. The HostSpecific value must be either "true" or "false". The default of "false" will be used.|Occurs when the host-specific parameter in a `template` directive is specified incorrectly. The message provides the line number of the template directive.|Set the host-specific parameter to "true" or "false".|  
|An invalid language '{0}' was specified in the 'template' directive. The language must be either "C#" or "VB". The default value of "C#" will be used.|Occurs when an unsupported language is specified in the `template` directive. Only "C#" or "VB" are allowed (case insensitive). The message provides the line number of the template directive.|Set the `language` parameter in the template directive to "C#" or"VB".|  
|Multiple output directives were found in the template. All but the first one will be ignored.|Occurs when multiple `output` directives are specified in a template file. The message provides the line number of the duplicate output directive.|Remove duplicate `output` directives.|  
|Multiple template directives were found in the template. All but the first one will be ignored. Multiple parameters to the template directive should be specified within one template directive.|Occurs if you specify multiple `template` directives within a text template file (including included files). The message provides the line number of the duplicate template directive.|Aggregate the different `template` directives into one `template` directive.|  
|No processor was specified for a directive named '{0}'. The directive will be ignored.|Occurs if you specify a `custom` directive, but do not provide a `processor` attribute. The message provides the name of the directive and the line number.|Provide a `processor` attribute with the name of the `directive` processor for the directive.|  
|A processor named '{0}' could not be found for the directive named '{1}'. The directive will be ignored.|Occurs when the system cannot find the `directive` processor you specified within a `custom` directive. The message provides the directive name, processor name, and the line number of the directive.|Set the `processor` attribute in the directive to the name of the directive processor.|  
|A required parameter '{0}' for the directive '{1}' was not found. The directive will be ignored.|Occurs when the system does not provide a required directive parameter. The message provides the name of the missing parameter, the directive name, and the line number.|Provide the missing parameter.|  
|The processor named '{0}' does not support the directive named '{1}'. The directive will be ignored.|Occurs when a directive processor does not support a directive. The message provides the name and line number of the offending directive along with the name of the directive processor.|Correct the name of the directive.|  
|The include directive for file '{0}' causes an infinite loop.|Displayed if circular include directives are specified (for example, file A includes file B, which includes file A).|Do not specify circular include directives.|  
|Running transformation:|Prepends this string to all errors or warnings that are generated while running the transform.|Not applicable.|  
|An unexpected start or end tag was found within a block. Make sure that you did not mis-type a start or end tag, and that you don't have any nested blocks in the template.|Displayed when you have an unexpected \<# or #>. That is, if you have a \<# after another open tag that has not been closed, or you have a #> when there is no unclosed open tag before it. The message provides the line number of the mismatched tag.|Either remove the mismatched start or end tag, or use an escape character.|  
|A directive was specified in the wrong format. The directive will be ignored. Please specify the directive in the format `<#@ name [parametername="parametervalue"]*  #>`|Displayed by the parser if a directive is not specified in the correct format. The message provides the line number of the incorrect directive.|Be sure all directives are in the form `<#@ name [parametername="parametervalue"]*  #>`. For more information, see [T4 Text Template Directives](../VS_IDE/t4-text-template-directives.md).|  
|Failed to load Assembly '{0}' for registered directive processor '{1}'<br /><br /> {2}|Occurs when a directive processor could not be loaded by the host. The message identifies the assembly provided for the directive processor and the name of the directive processor.|Be sure the directive processor is registered correctly and that the assembly exists.|  
|Failed to find type '{0}' in Assembly '{1}' for registered directive processor '{2}'<br /><br /> {3}|Occurs when a directive processor type could not be loaded from its assembly. The message provides the name of the type, assembly, and directive processor.|The vshost finds directive processor information (name, assembly, and type) in the registry. Be sure the directive processor is registered correctly, and that the type exists in the assembly.|  
|There was a problem loading the assembly '{0}'|Occurs when there is a problem loading an assembly. The message provides the name of the assembly.|You can specify assemblies to be loaded in \<@#assembly#> directives, and by directive processors. The error message that follows this string should provide more data on why the assembly load failed.|  
|There was a problem creating and initializing the processor for a directive named '{1}'. The type of the processor is {0}. The directive will be ignored.|Occurs when the system could not create or initialize a directive processor. The message provides the name and line number of the directive and the type of the processor.|Be sure you use the correct directive processor, and that the directive processor has a public default constructor. Otherwise, use the debug options to find out why the Initialize() method of the directive processor is failing. For more information, see [Troubleshooting Text Templates](../VS_IDE/debugging-a-t4-text-template.md).|  
|An Exception was thrown while processing a directive named '{0}'.|Occurs when a directive processor throws an exception when processing a directive.|Be sure that the parameters to the directive processor are correct.|  
|The host threw an exception while trying to resolve the assembly reference '{0}'.|Occurs when the host throws an exception when it tries to resolve an assembly reference. The message provides the assembly reference string.|Assembly references come from \<@#assembly#> directives and from directive processors. Be sure that the 'name' parameter provided in the assembly parameter is correct.|  
|Attempt to specify unsupported {1} value '{0}' for directive {2}|Occurs by the RequiresProvidesDirectiveProcessor (all our generated directive processors derive from it), when you supply an unsupported requires or provides argument.|Be sure that the names in the name='value' pairs provided in the requires and provides parameters are correct.|