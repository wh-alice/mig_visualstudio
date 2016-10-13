---
title: "IDebugPrimitiveTypeField::GetPrimitiveType"
ms.custom: na
ms.date: "10/11/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "GetPrimitiveType"
  - "IDebugPrimitiveTypeField::GetPrimitiveType"
ms.assetid: a186c922-bbfe-478c-a744-b21eb4672d8f
caps.latest.revision: 8
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
# IDebugPrimitiveTypeField::GetPrimitiveType
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Retrieves the primitive type that is associated with this field. </para>
  </introduction>
  <syntaxSection>
    <legacySyntax language="cpp#">HRESULT GetPrimitiveType (
   DWORD* <parameterReference>pdwType</parameterReference>
);</legacySyntax>
    <legacySyntax language="c#">int GetPrimitiveType (
   out uint <parameterReference>pdwType</parameterReference>
);</legacySyntax>
  </syntaxSection>
  <parameters>
    <content>
      <definitionTable>
        <definedTerm>
          <parameterReference>pdwType</parameterReference>
        </definedTerm>
        <definition>
          <para>[out] Value from the CorElementType Enumeration that represents the primitive type.</para>
        </definition>
      </definitionTable>
    </content>
  </parameters>
  <returnValue>
    <content>
      <para>If successful, returns <languageKeyword>S_OK</languageKeyword>; otherwise, returns <languageKeyword>S_FALSE</languageKeyword>.</para>
    </content>
  </returnValue>
  <relatedTopics>
\<link xlink:href="73a428fd-797e-4ceb-8392-ba16f1c5226b">IDebugPrimitiveTypeField</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>