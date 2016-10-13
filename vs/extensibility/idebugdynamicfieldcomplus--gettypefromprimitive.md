---
title: "IDebugDynamicFieldCOMPlus::GetTypeFromPrimitive"
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
  - "IDebugDynamicFieldCOMPlus::GetTypeFromPrimitive"
  - "GetTypeFromPrimitive"
ms.assetid: d7f51e2a-1b72-489c-b7b6-4af7b7e4d663
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
# IDebugDynamicFieldCOMPlus::GetTypeFromPrimitive
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Retrieves a type given its primitive type.</para>
  </introduction>
  <syntaxSection>
    <legacySyntax language="cpp#">HRESULT GetTypeFromPrimitive(
   DWORD         <parameterReference>dwCorElementType</parameterReference>,
   IDebugField** <parameterReference>ppType</parameterReference>
);</legacySyntax>
    <legacySyntax language="c#">int GetTypeFromPrimitive(
   uint            <parameterReference>dwCorElementType</parameterReference>,
   out IDebugField <parameterReference>ppType</parameterReference>
);</legacySyntax>
  </syntaxSection>
  <parameters>
    <content>
      <definitionTable>
        <definedTerm>
          <parameterReference>dwCorElementType</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Value from the CorElementType Enumeration that represents the primitive type.</para>
        </definition>
        <definedTerm>
          <parameterReference>ppType</parameterReference>
        </definedTerm>
        <definition>
          <para>[out] Returns the \<link xlink:href="adecdd1c-b1b9-4027-92da-74cbe910636f">IDebugField</link> that represents the type.</para>
        </definition>
      </definitionTable>
    </content>
  </parameters>
  <returnValue>
    <content>
      <para>If successful, returns <languageKeyword>S_OK</languageKeyword>; otherwise, returns an error code. </para>
    </content>
  </returnValue>
  <relatedTopics>
\<link xlink:href="c3a25f27-327a-4bdb-b026-27d436ddcd0c">IDebugDynamicFieldCOMPlus</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>