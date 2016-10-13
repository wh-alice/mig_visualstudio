---
title: "New Project Generation: Under the Hood, Part Two"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "projects [Visual Studio], new project dialog"
  - "projects [Visual Studio], new project generation"
ms.assetid: 73ce91d8-0ab1-4a1f-bf12-4d3c49c01e13
caps.latest.revision: 12
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# New Project Generation: Under the Hood, Part Two
\<?xml version="1.0" encoding="utf-8"?>
\<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    \<?Comment jf: Moved this comment from part 1, &quot; Save this comment for Part Two -- Without wizard extensions, VS calls CreateProject of registered project factory with dictionary of name-value pairs of collected info. New project dialog is still open. Second half of vstemplate runs as silent wizard to create file items and folders, then recursively calls part of CreateProject, but this time with Open rather than Copy flag. If wizard extensions are present, CreateProject runs them at this time as a modal dialog to collect more info.&quot; 2007-10-01T12:36:00Z  Id='0?>
    \<?Comment jf: Moved this comment from part 1, &quot; Save this comment for Part Two -- Without wizard extensions, VS calls CreateProject of registered project factory with dictionary of name-value pairs of collected info. New project dialog is still open. Second half of vstemplate runs as silent wizard to create file items and folders, then recursively calls part of CreateProject, but this time with Open rather than Copy flag. If wizard extensions are present, CreateProject runs them at this time as a modal dialog to collect more info.&quot; 2007-10-01T12:36:00Z?>
    <para>In \<link xlink:href="66778698-0258-467d-8b8b-c351744510eb">New Project Generation : Under the Hood</link> we saw how the <ui>New Project</ui> dialog Box is populated. Let's assume you've selected a <ui>Visual C# Windows Application</ui>, filled out the <ui>Name</ui> and <ui>Location</ui> text boxes, and clicked OK.</para>
  </introduction>
  <section>
    <title>Generating the Solution Files</title>
    <content>
      <para>Choosing an application template directs <token>vsprvs</token> to unzip and open the corresponding .vstemplate file, and to launch a template to interpret the XML commands in this file. These commands create projects and project items in the new or existing solution.</para>
      <para>The template unpacks source files, called item templates, from the same .zip folder that holds the .vstemplate file. The template copies these files to the new project, customizing them accordingly. For an overview of project and item templates, see \<legacyLink xlink:href="141fccaa-d68f-4155-822b-27f35dd94041">NIB: Visual Studio Templates</legacyLink>.</para>
    </content>
    <sections>
      <section>
        <title>Template Parameter Replacement</title>
        <content>
          <para>When the template copies an item template to a new project, it replaces any template parameters with strings to customize the file. A template parameter is a special token that is preceded and followed by a dollar sign, for example, $date$. </para>
          <para>Let's look at a typical project item template. Extract and examine Program.cs in the Program Files\Microsoft Visual Studio 8\Common7\IDE\ProjectTemplates\CSharp\Windows\1033\WindowsApplication.zip folder. </para>
          <code>using System;
using System.Collections.Generic;
using System.Windows.Forms;

namespace <codeFeaturedElement>$safeprojectname$</codeFeaturedElement>
{
    static class Program
    {
        // source code deleted here for brevity
    }
}</code>
          <para>If you create a new Windows application project named Simple, the template replaces the <languageKeyword>$safeprojectname$</languageKeyword> parameter with the name of the project. </para>
          <code>using System;
using System.Collections.Generic;
using System.Windows.Forms;

namespace <codeFeaturedElement>Simple</codeFeaturedElement>
{
    static class Program
    {
        // source code deleted here for brevity
    }
}</code>
          <para>For a complete list of template parameters, see \<link xlink:href="1b567143-08c6-4d7a-b484-49f0671754fe">Template Parameters</link>.</para>
        </content>
      </section>
    </sections>
  </section>
  <section>
    <title>A Look Inside a .VSTemplate File</title>
    <content>
      <para>A basic .vstemplate file has this format</para>
      <code>&lt;VSTemplate Version="2.0.0"     xmlns="http://schemas.microsoft.com/developer/vstemplate/2005"     Type="Project"&gt;
    &lt;TemplateData&gt;
    &lt;/TemplateData&gt;
    &lt;TemplateContent&gt;
    &lt;/TemplateContent&gt;
&lt;/VSTemplate&gt;</code>
      <para>We looked at the &lt;TemplateData&gt; section in the \<link xlink:href="66778698-0258-467d-8b8b-c351744510eb">first part of this article</link>. The tags in this section are used to control the appearance of the <ui>New Project</ui> dialog box.</para>
      <para>The tags in the &lt;TemplateContent&gt; section control the generation of new projects and project items. Here's the &lt;TemplateContent&gt; section from the cswindowsapplication.vstemplate file in the \Program Files\Microsoft Visual Studio 8\Common7\IDE\ProjectTemplates\CSharp\Windows\1033\WindowsApplication.zip folder.</para>
      <code>&lt;TemplateContent&gt;
  &lt;Project File="WindowsApplication.csproj" ReplaceParameters="true"&gt;
    &lt;ProjectItem ReplaceParameters="true"
      TargetFileName="Properties\AssemblyInfo.cs"&gt;
      AssemblyInfo.cs
    &lt;/ProjectItem&gt;
    &lt;ProjectItem TargetFileName="Properties\Resources.resx"&gt;
      Resources.resx
    &lt;/ProjectItem&gt;
    &lt;ProjectItem ReplaceParameters="true"       TargetFileName="Properties\Resources.Designer.cs"&gt;
      Resources.Designer.cs
    &lt;/ProjectItem&gt;
    &lt;ProjectItem TargetFileName="Properties\Settings.settings"&gt;
      Settings.settings
    &lt;/ProjectItem&gt;
    &lt;ProjectItem ReplaceParameters="true"       TargetFileName="Properties\Settings.Designer.cs"&gt;
      Settings.Designer.cs
    &lt;/ProjectItem&gt;
    &lt;ProjectItem ReplaceParameters="true" OpenInEditor="true"&gt;
      Form1.cs
    &lt;/ProjectItem&gt;
    &lt;ProjectItem ReplaceParameters="true"&gt;
      Form1.Designer.cs
    &lt;/ProjectItem&gt;
    &lt;ProjectItem ReplaceParameters="true"&gt;
      Program.cs
    &lt;/ProjectItem&gt;
  &lt;/Project&gt;
&lt;/TemplateContent&gt;</code>
      <para>The &lt;Project&gt; tag controls the generation of a project, and the &lt;ProjectItem&gt; tag controls the generation of a project item. If the parameter ReplaceParameters is true, the template will customize all template parameters in the project file or item. In this case, all project items are customized, except for Settings.settings.</para>
      <para>The TargetFileName parameter specifies the name and relative path of the resulting project file or item. This lets you create a folder structure for your project. If you don't specify this argument, the project item will have the same name as the project item template.</para>
      <para>The resulting Windows application folder structure looks like this:</para>
      <mediaLink>
        \<image xlink:href="4b678e0c-3e4d-41ef-96cc-46c91fd19247" />
      </mediaLink>
      <para />
      <para>The first and only &lt;Project&gt; tag in the template reads:</para>
      <code>&lt;Project File="WindowsApplication.csproj" ReplaceParameters="true"&gt;</code>
      <para>This instructs the New Project template to create the Simple.csproj project file by copying and customizing the template item windowsapplication.csproj.</para>
    </content>
    <sections>
      <section>
        <title>Designers and References</title>
        <content>
          <para>You can see in the Solution Explorer that the Properties folder is present and contains the expected files. But what about project references and designer file dependencies, such as Resources.Designer.cs to Resources.resx, and Form1.Designer.cs to Form1.cs?  These are set up in the Simple.csproj file when it is generated.</para>
          <para>Here's the &lt;ItemGroup&gt; from Simple.csproj that creates the project references:</para>
          <code>&lt;ItemGroup&gt;
    &lt;Reference Include="System" /&gt;
    &lt;Reference Include="System.Data" /&gt;
    &lt;Reference Include="System.Deployment" /&gt;
    &lt;Reference Include="System.Drawing" /&gt;
    &lt;Reference Include="System.Windows.Forms" /&gt;
    &lt;Reference Include="System.Xml" /&gt;
&lt;/ItemGroup&gt;</code>
          <para>You can see that these are the six project references that appear in the Solution Explorer. Here's a section from another &lt;ItemGroup&gt;. Many lines of code have been deleted for clarity. This section makes Settings.Designer.cs dependent on Settings.settings:</para>
          <code>&lt;ItemGroup&gt;
    &lt;Compile Include="Properties\Settings.Designer.cs"&gt;
        &lt;DependentUpon&gt;Settings.settings&lt;/DependentUpon&gt;
    &lt;/Compile&gt;
&lt;/ItemGroup&gt;</code>
        </content>
      </section>
    </sections>
  </section>
  <relatedTopics>
\<link xlink:href="66778698-0258-467d-8b8b-c351744510eb">New Project Generation: Under the Hood</link>

</relatedTopics>
</developerConceptualDocument>