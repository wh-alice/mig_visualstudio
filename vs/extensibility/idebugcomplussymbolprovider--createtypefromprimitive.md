---
title: "IDebugComPlusSymbolProvider::CreateTypeFromPrimitive"
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
  - "IDebugComPlusSymbolProvider::CreateTypeFromPrimitive"
  - "CreateTypeFromPrimitive"
ms.assetid: 37213cc2-a038-42ea-9b28-3ae40d4cfe69
caps.latest.revision: 11
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
# IDebugComPlusSymbolProvider::CreateTypeFromPrimitive
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Creates a type from the specified primitive type. </para>
  </introduction>
  <syntaxSection>
    <legacySyntax>[C++]
HRESULT CreateTypeFromPrimitive(
   DWORD          <parameterReference>dwPrimType</parameterReference>,
   IDebugAddress* <parameterReference>pAddress</parameterReference>,
   IDebugField**  <parameterReference>ppType</parameterReference>
);</legacySyntax>
    <legacySyntax>[C#]
int CreateTypeFromPrimitive(
   uint          <parameterReference>dwPrimType</parameterReference>,
   IDebugAddress <parameterReference>pAddress</parameterReference>,
   IDebugField   <parameterReference>ppType</parameterReference>
);</legacySyntax>
  </syntaxSection>
  <parameters>
    <content>
      <definitionTable>
        <definedTerm>
          <parameterReference>dwPrimType</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Value from the CorElementType Enumeration that represents the primitive type.</para>
        </definition>
        <definedTerm>
          <parameterReference>pAddress</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] An address object represented by an \<link xlink:href="bc709ff7-4966-4f36-9af2-690efe2cea1d">IDebugAddress</link> interface.</para>
        </definition>
        <definedTerm>
          <parameterReference>ppType</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Returns an \<link xlink:href="adecdd1c-b1b9-4027-92da-74cbe910636f">IDebugField</link> object that describes the type.</para>
        </definition>
      </definitionTable>
    </content>
  </parameters>
  <returnValue>
    <content>
      <para>If successful, returns <languageKeyword>S_OK</languageKeyword>; otherwise, returns an error code.</para>
    </content>
  </returnValue>
  <codeExample>
    <description>
      <content>
        <para>The following example shows how to implement this method for a <embeddedLabel>CDebugSymbolProvider</embeddedLabel> object that exposes the \<link xlink:href="5b98e908-fd15-49a6-9010-933c9b948085">IDebugComPlusSymbolProvider</link> interface.</para>
      </content>
    </description>
    <code language="cpp#">HRESULT CDebugSymbolProvider::CreateTypeFromPrimitive(
    DWORD dwPrimType,
    IDebugAddress* pAddress,
    IDebugField** ppType)
{
    HRESULT hr = S_OK;
    CDEBUG_ADDRESS addr;
    const COR_SIGNATURE* pTypeInfo = (const COR_SIGNATURE*) &amp; dwPrimType;
    CDebugGenericParamScope* pGenScope = NULL;

    //
    // This function will only work for primitive types
    //

    METHOD_ENTRY( CDebugSymbolProvider::CreateTypeFromPrimitive );

    IfFailGo( pAddress-&gt;GetAddress( &amp;addr ) );

    IfNullGo( pGenScope = new CDebugGenericParamScope(addr.GetModule(), addr.tokClass, addr.GetMethod()), E_OUTOFMEMORY );

    IfFailGo( CreateType( pTypeInfo,
                          1,
                          addr.GetModule(),
                          addr.GetMethod(),
                          pGenScope,
                          ppType ) );

    METHOD_EXIT( CDebugSymbolProvider::CreateTypeFromPrimitive, hr );

Error:

    RELEASE( pGenScope );
    return hr;
}</code>
  </codeExample>
  <relatedTopics>
\<link xlink:href="5b98e908-fd15-49a6-9010-933c9b948085">IDebugComPlusSymbolProvider</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>