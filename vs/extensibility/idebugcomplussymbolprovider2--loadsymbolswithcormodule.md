---
title: "IDebugComPlusSymbolProvider2::LoadSymbolsWithCorModule"
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
  - "IDebugComPlusSymbolProvider2::LoadSymbolsWithCorModule"
  - "LoadSymbolsWithCorModule"
ms.assetid: b6abf3a4-ce60-4e66-9637-82ce911148de
caps.latest.revision: 10
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
# IDebugComPlusSymbolProvider2::LoadSymbolsWithCorModule
\<?xml version="1.0" encoding="utf-8"?>
\<developerReferenceWithSyntaxDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Loads debug symbols given the <embeddedLabel>ICorDebugModule</embeddedLabel> object.</para>
  </introduction>
  <syntaxSection>
    <legacySyntax language="cpp#">HRESULT LoadSymbolsWithCorModule(
   ULONG32   <parameterReference>ulAppDomainID</parameterReference>,
   GUID      <parameterReference>guidModule</parameterReference>,
   ULONGLONG <parameterReference>baseAddress</parameterReference>,
   IUnknown* <parameterReference>pUnkMetadataImport</parameterReference>,
   IUnknown* <parameterReference>pUnkCorDebugModule</parameterReference>,
   BSTR      <parameterReference>bstrModuleName</parameterReference>,
   BSTR      <parameterReference>bstrSymSearchPath</parameterReference>
);</legacySyntax>
    <legacySyntax language="c#">int LoadSymbolsWithCorModule(
   uint   <parameterReference>ulAppDomainID</parameterReference>,
   Guid   <parameterReference>guidModule</parameterReference>,
   ulong  <parameterReference>baseAddress</parameterReference>,
   object <parameterReference>pUnkMetadataImport</parameterReference>,
   object <parameterReference>pUnkCorDebugModule</parameterReference>,
   string <parameterReference>bstrModuleName</parameterReference>,
   string <parameterReference>bstrSymSearchPath</parameterReference>
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
          <para>[in] Object that contains the debug symbol metadata.</para>
        </definition>
        <definedTerm>
          <parameterReference>pUnkCorDebugModule</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Object that implements the ICorDebugModule Interface.</para>
        </definition>
        <definedTerm>
          <parameterReference>bstrModuleName</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Name of the module.</para>
        </definition>
        <definedTerm>
          <parameterReference>bstrSymSearchPath</parameterReference>
        </definedTerm>
        <definition>
          <para>[in] Path to search for the symbol file.</para>
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
    <code language="cpp#">HRESULT CDebugSymbolProvider::LoadSymbolsWithCorModule(
    ULONG32 ulAppDomainID,
    GUID guidModule,
    ULONGLONG baseOffset,
    IUnknown* _pMetadata,
    IUnknown* _pCorModule,
    BSTR bstrModule,
    BSTR bstrSearchPath)
{
    EMIT_TICK_COUNT("Entry -- Loading symbols for the following target:");
    USES_CONVERSION;
    EmitTickCount(W2A(bstrModule));

    CAutoLock Lock(this);

    HRESULT hr = S_OK;
    CComPtr&lt;IMetaDataImport&gt; pMetadata;
    CComPtr&lt;ICorDebugModule&gt; pCorModule;

    CModule* pmodule = NULL;
    CModule* pmoduleNew = NULL;
    bool fAlreadyLoaded = false;
    Module_ID idModule(ulAppDomainID, guidModule);
    bool fSymbolsLoaded = false;
    DWORD dwCurrentState = 0;

    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));
    ASSERT(IsValidInterfacePtr(_pMetadata, IUnknown));

    METHOD_ENTRY( CDebugSymbolProvider::LoadSymbol );

    IfFalseGo( _pMetadata, E_INVALIDARG );
    IfFalseGo( _pCorModule, E_INVALIDARG );

    IfFailGo( _pMetadata-&gt;QueryInterface( IID_IMetaDataImport,
                                          (void**)&amp;pMetadata) );

    IfFailGo( _pCorModule-&gt;QueryInterface( IID_ICorDebugModule,
                                           (void**)&amp;pCorModule) );

    ASSERT(guidModule != GUID_NULL);

    fAlreadyLoaded = GetModule( idModule, &amp;pmodule ) == S_OK;

    IfNullGo( pmoduleNew = new CModule, E_OUTOFMEMORY );

    //
    //  We are now allowing modules to be created that do not have SymReaders.
    //  It is likely there are a number of corner cases being ignored
    //  that will require knowledge of the hr result below.
    //
    dwCurrentState = m_pSymProvGroup ? m_pSymProvGroup-&gt;GetCurrentState() : 0;

    HRESULT hrLoad = pmoduleNew-&gt;Create( idModule,
                                         dwCurrentState,
                                         pMetadata,
                                         pCorModule,
                                         bstrModule,
                                         bstrSearchPath,
                                         baseOffset );

    if (hrLoad == S_OK)
    {
        fSymbolsLoaded = true;
    }

    // Remove the old module
    if (fAlreadyLoaded)
    {
        IfFailGo(pmoduleNew-&gt;AddEquivalentModulesFrom(pmodule));
        RemoveModule( pmodule );
    }

    IfFailGo( AddModule( pmoduleNew ) );

Error:

    RELEASE (pmodule);
    RELEASE (pmoduleNew);

    if (SUCCEEDED(hr) &amp;&amp; !fSymbolsLoaded)
    {
        hr = hrLoad;
    }

    METHOD_EXIT( CDebugSymbolProvider::LoadSymbol, hr );
    EMIT_TICK_COUNT("Exit");
    return hr;
}</code>
  </codeExample>
  <relatedTopics>
\<link xlink:href="fa2f9b49-03ad-43c7-92d6-6dcb9c3d0531">IDebugComPlusSymbolProvider2</link>
</relatedTopics>
</developerReferenceWithSyntaxDocument>