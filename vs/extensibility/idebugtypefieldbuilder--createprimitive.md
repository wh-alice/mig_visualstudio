---
title: "IDebugTypeFieldBuilder::CreatePrimitive"
ms.custom: na
ms.date: "10/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "CreatePrimitive"
  - "IDebugTypeFieldBuilder::CreatePrimitive"
ms.assetid: 512c6ff0-97c5-409f-939f-4cc969bc4bb9
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
# IDebugTypeFieldBuilder::CreatePrimitive
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Creates an object that represents a primitive type.</para>
  </introduction>
  <syntaxSection>
    <legacySyntax language="cpp#">HRESULT CreatePrimitive (
   DWORD          <parameterReference>dwElementType</parameterReference>,
   IDebugField ** <parameterReference>pTypeField</parameterReference>
);</legacySyntax>
    <legacySyntax language="c#">int CreatePrimitive (
   uint            <parameterReference>dwElementType</parameterReference>,
   out IDebugField <parameterReference>pTypeField</parameterReference>
);</legacySyntax>
  </syntaxSection>
  <parameters>
    <content>
      <definitionTable>
        <definedTerm>
          <parameterReference>dwElementType</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Value from the CorElementType Enumeration that represents the primitive type.</para>
        </definition>
        <definedTerm>
          <parameterReference>pTypeField</parameterReference>
        </definedTerm>
        <definition>
          <para>[out] Returns the IDebugField interface for the new type.</para>
        </definition>
      </definitionTable>
    </content>
  </parameters>
  <returnValue>
    <content>
      <para>If successful, returns <languageKeyword>S_OK</languageKeyword>; otherwise, returns an error code.</para>
    </content>
  </returnValue>
  <relatedTopics>
\<link xlink:href="2dfed0be-6972-4bec-baec-f0b78df9ef97">IDebugTypeFieldBuilder</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>