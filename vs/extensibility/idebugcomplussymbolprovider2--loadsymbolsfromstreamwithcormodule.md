---
title: "IDebugComPlusSymbolProvider2::LoadSymbolsFromStreamWithCorModule"
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
  - "IDebugComPlusSymbolProvider2::LoadSymbolsFromStreamWithCorModule"
  - "LoadSymbolsFromStreamWithCorModule"
ms.assetid: f79b894f-52c4-43c2-9a68-c71536451f6c
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
# IDebugComPlusSymbolProvider2::LoadSymbolsFromStreamWithCorModule
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Load debug symbols from a data stream given the <embeddedLabel>ICorDebugModule</embeddedLabel> object.</para>
  </introduction>
  <syntaxSection>
    <legacySyntax language="cpp#">HRESULT LoadSymbolsFromStreamWithCorModule(
   ULONG32   <parameterReference>ulAppDomainID</parameterReference>,
   GUID      <parameterReference>guidModule</parameterReference>,
   ULONGLONG <parameterReference>baseAddress</parameterReference>,
   IUnknown* <parameterReference>pUnkMetadataImport</parameterReference>,
   IUnknown* <parameterReference>pUnkCorDebugModule</parameterReference>,
   IStream*  <parameterReference>pStream</parameterReference>
);</legacySyntax>
    <legacySyntax language="c#">int LoadSymbolsFromStreamWithCorModule(
   uint    <parameterReference>ulAppDomainID</parameterReference>,
   Guid    <parameterReference>guidModule</parameterReference>,
   ulong   <parameterReference>baseAddress</parameterReference>,
   object  <parameterReference>pUnkMetadataImport</parameterReference>,
   object  <parameterReference>pUnkCorDebugModule</parameterReference>,
   IStream <parameterReference>pStream</parameterReference>
);</legacySyntax>
  </syntaxSection>
  <parameters>
    <content>
      <definitionTable>
        <definedTerm>
          <parameterReference>ulAppDomainID</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Identifier of the application domain.</para>
        </definition>
        <definedTerm>
          <parameterReference>guidModule</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Unique identifier of the module.</para>
        </definition>
        <definedTerm>
          <parameterReference>baseAddress</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Base memory address.</para>
        </definition>
        <definedTerm>
          <parameterReference>pUnkMetadataImport</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Object that contains the symbol metadata.</para>
        </definition>
        <definedTerm>
          <parameterReference>pUnkCorDebugModule</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Object that implements the ICorDebugModule Interface.</para>
        </definition>
        <definedTerm>
          <parameterReference>pStream</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Data stream that contains the debug symbols to load.</para>
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
        <para>The following example shows how to implement this method for a <embeddedLabel>CDebugSymbolProvider</embeddedLabel> object that exposes the \<link xlink:href="fa2f9b49-03ad-43c7-92d6-6dcb9c3d0531">IDebugComPlusSymbolProvider2</link> interface.</para>
      </content>
    </description>
    <code language="cpp#">HRESULT CDebugSymbolProvider::LoadSymbolsFromStreamWithCorModule(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    ULONGLONG baseOffset,
    IUnknown* pUnkMetadataImport,
    IUnknown* pUnkCorDebugModule,
    IStream* pStream
)
{
    CAutoLock Lock(this);

    HRESULT hr = S_OK;
    CComPtr&lt;IMetaDataImport&gt; pMetadata;
    CComPtr&lt;ICorDebugModule&gt; pCorModule;

    CModule* pmodule = NULL;
    CModule* pmoduleNew = NULL;
    bool fAlreadyLoaded = false;
    Module_ID idModule(ulAppDomainID, guidModule);
    DWORD dwCurrentState = 0;

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidInterfacePtr(pUnkMetadataImport, IUnknown));

    METHOD_ENTRY( CDebugSymbolProvider::LoadSymbolsFromStream );

    IfFalseGo( pUnkMetadataImport, E_INVALIDARG );
    IfFalseGo( pUnkCorDebugModule, E_INVALIDARG );

    IfFailGo( pUnkMetadataImport-&gt;QueryInterface( IID_IMetaDataImport,
              (void**)&amp;pMetadata) );

    IfFailGo( pUnkCorDebugModule-&gt;QueryInterface( IID_ICorDebugModule,
              (void**)&amp;pCorModule) );

    ASSERT(guidModule != GUID_NULL);

    fAlreadyLoaded = GetModule( idModule, &amp;pmodule ) == S_OK;

    IfNullGo( pmoduleNew = new CModule, E_OUTOFMEMORY );

    dwCurrentState = m_pSymProvGroup ? m_pSymProvGroup-&gt;GetCurrentState() : 0;

    IfFailGo( pmoduleNew-&gt;Create( idModule,
                                  dwCurrentState,
                                  pMetadata,
                                  pCorModule,
                                  pStream,
                                  baseOffset ) );

    if (fAlreadyLoaded)
    {
        IfFailGo(pmoduleNew-&gt;AddEquivalentModulesFrom(pmodule));
        RemoveModule(pmodule);
    }

    IfFailGo( AddModule( pmoduleNew ) );

Error:

    RELEASE (pmodule);
    RELEASE (pmoduleNew);

    METHOD_EXIT( CDebugSymbolProvider::LoadSymbolsFromStream, hr );

    return hr;
}</code>
  </codeExample>
  <relatedTopics>
\<link xlink:href="fa2f9b49-03ad-43c7-92d6-6dcb9c3d0531">IDebugComPlusSymbolProvider2</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>