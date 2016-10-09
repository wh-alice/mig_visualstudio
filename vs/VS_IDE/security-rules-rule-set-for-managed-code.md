---
title: "Security Rules rule set for managed code"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 564aeac6-03fa-41b0-b655-88179f0ab01b
caps.latest.revision: 9
ms.author: "susanno"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Security Rules rule set for managed code
You should include the Microsoft Security Rules rule set to maximize the number of potential security issues that are reported.  
  
|Rule|Description|  
|----------|-----------------|  
|[CA2100](../VS_IDE/ca2100--review-sql-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2102](../VS_IDE/ca2102--catch-non-clscompliant-exceptions-in-general-handlers.md)|Catch non-CLSCompliant exceptions in general handlers|  
|[CA2103](../VS_IDE/ca2103--review-imperative-security.md)|Review imperative security|  
|[CA2104](../VS_IDE/ca2104--do-not-declare-read-only-mutable-reference-types.md)|Do not declare read only mutable reference types|  
|[CA2105](../VS_IDE/ca2105--array-fields-should-not-be-read-only.md)|Array fields should not be read only|  
|[CA2106](../VS_IDE/ca2106--secure-asserts.md)|Secure asserts|  
|[CA2107](../VS_IDE/ca2107--review-deny-and-permit-only-usage.md)|Review deny and permit only usage|  
|[CA2108](../VS_IDE/ca2108--review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2109](../VS_IDE/ca2109--review-visible-event-handlers.md)|Review visible event handlers|  
|[CA2111](../VS_IDE/ca2111--pointers-should-not-be-visible.md)|Pointers should not be visible|  
|[CA2112](../VS_IDE/ca2112--secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../VS_IDE/ca2114--method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2115](../VS_IDE/ca2115--call-gc.keepalive-when-using-native-resources.md)|Call GC.KeepAlive when using native resources|  
|[CA2116](../VS_IDE/ca2116--aptca-methods-should-only-call-aptca-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../VS_IDE/ca2117--aptca-types-should-only-extend-aptca-base-types.md)|APTCA types should only extend APTCA base types|  
|[CA2118](../VS_IDE/ca2118--review-suppressunmanagedcodesecurityattribute-usage.md)|Review SuppressUnmanagedCodeSecurityAttribute usage|  
|[CA2119](../VS_IDE/ca2119--seal-methods-that-satisfy-private-interfaces.md)|Seal methods that satisfy private interfaces|  
|[CA2120](../VS_IDE/ca2120--secure-serialization-constructors.md)|Secure serialization constructors|  
|[CA2121](../VS_IDE/ca2121--static-constructors-should-be-private.md)|Static constructors should be private|  
|[CA2122](../VS_IDE/ca2122--do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../VS_IDE/ca2123--override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../VS_IDE/ca2124--wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../VS_IDE/ca2126--type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2130](../VS_IDE/ca2130--security-critical-constants-should-be-transparent.md)|Security critical constants should be transparent|  
|[CA2131](../VS_IDE/ca2131--security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../VS_IDE/ca2132--default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../VS_IDE/ca2133--delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../VS_IDE/ca2134--methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2135](../VS_IDE/ca2135--level-2-assemblies-should-not-contain-linkdemands.md)|Level 2 assemblies should not contain LinkDemands|  
|[CA2136](../VS_IDE/ca2136--members-should-not-have-conflicting-transparency-annotations.md)|Members should not have conflicting transparency annotations|  
|[CA2137](../VS_IDE/ca2137--transparent-methods-must-contain-only-verifiable-il.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../VS_IDE/ca2138--transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2139](../VS_IDE/ca2139--transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute.md)|Transparent methods may not use the HandleProcessCorruptingExceptions attribute|  
|[CA2140](../VS_IDE/ca2140--transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../VS_IDE/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2142](../VS_IDE/ca2142--transparent-code-should-not-be-protected-with-linkdemands.md)|Transparent code should not be protected with LinkDemands|  
|[CA2143](../VS_IDE/ca2143--transparent-methods-should-not-use-security-demands.md)|Transparent methods should not use security demands|  
|[CA2144](../VS_IDE/ca2144--transparent-code-should-not-load-assemblies-from-byte-arrays.md)|Transparent code should not load assemblies from byte arrays|  
|[CA2145](../VS_IDE/ca2145--transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute.md)|Transparent methods should not be decorated with the SuppressUnmanagedCodeSecurityAttribute|  
|[CA2146](../VS_IDE/ca2146--types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../VS_IDE/ca2147--transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../VS_IDE/ca2149--transparent-methods-must-not-call-into-native-code.md)|Transparent methods must not call into native code|  
|[CA2210](../VS_IDE/ca2210--assemblies-should-have-valid-strong-names.md)|Assemblies should have valid strong names|