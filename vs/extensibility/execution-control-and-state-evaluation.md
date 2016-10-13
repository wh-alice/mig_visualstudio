---
title: "Execution Control and State Evaluation"
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
  - "debugging [Debugging SDK], execution control"
  - "expression evaluation, control of execution"
ms.assetid: 55adde38-1622-4b51-83cb-ce1b04c1ca7a
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
# Execution Control and State Evaluation
\<?xml version="1.0" encoding="utf-8"?>
\<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Debugging an application requires implementing such execution control features as stepping into functions, stopping at breakpoints, and continuing execution. Visual Studio debugging bases its execution control on events sent between debugger components.</para>
  </introduction>
  <section>
    <title>In This Section</title>
    <content>
      <definitionTable>
        <definedTerm>
          \<legacyLink xlink:href="6BE80904-E66C-4CAE-8891-1113B799FB01">Program Control</legacyLink>
        </definedTerm>
        <definition>
          <para>Lists the following routines that occur at the program level: setting the next statement, executing, stepping, continuing, suspending, and resuming.</para>
        </definition>
        <definedTerm>
          \<legacyLink xlink:href="A6F77BF0-BF81-443F-8683-5F12075BBE10">Breakpoint-Related Methods</legacyLink>
        </definedTerm>
        <definition>
          <para>Defines the bound and pending types of breakpoints that Visual Studio supports. </para>
        </definition>
        <definedTerm>
          \<legacyLink xlink:href="373D6B49-0459-4CCE-816E-05745A44FE49">Call Stack Evaluation</legacyLink>
        </definedTerm>
        <definition>
          <para>Discusses implementation of the methods that allow viewing of the stack frames of the call stack during break mode. </para>
        </definition>
        <definedTerm>
          \<legacyLink xlink:href="5044CED5-C18C-4534-B0BF-CC3E50CD57AC">Expression Evaluation</legacyLink>
        </definedTerm>
        <definition>
          <para>Explains how the debug engine (DE), expression evaluation (EE), and session debug manager are involved in the parsing and evaluation of an expression entered into one of the windows of the IDE.</para>
        </definition>
        <definedTerm>
          Control Events
        </definedTerm>
        <definition>
          <para>Discusses the interface used to send events during the controlled execution of the program. </para>
        </definition>
      </definitionTable>
    </content>
  </section>
  <relatedTopics />
</developerConceptualDocument>