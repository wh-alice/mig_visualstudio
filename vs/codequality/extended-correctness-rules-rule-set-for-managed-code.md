---
title: "Extended Correctness Rules rule set for managed code"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5b181f5b-6c7a-4e46-a783-360e1da427a0
caps.latest.revision: 11
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
# Extended Correctness Rules rule set for managed code
The Microsoft Extended Correctness Rules rule set maximizes the logic and framework usage errors that are reported by code analysis. Extra emphasis is placed on specific scenarios such as COM interoperability and mobile applications. You should consider including this rule set if one of these scenarios applies to your project or to find additional problems in your project.  
  
 The Microsoft Extended Correctness Rules rule set includes the rules that are in the Microsoft Basic Correctness Rules rule set. The Basic Correctness Rules include the rules that are in the Microsoft Minimum Recommended Rules rule set. For more information see [Basic Correctness Rules rule set for managed code](../codequality/basic-correctness-rules-rule-set-for-managed-code.md) and [Managed Recommended Rules rule set for managed code](../codequality/managed-recommended-rules-rule-set-for-managed-code.md)  
  
 The following table describes all of the rules in the Microsoft Extended Correctness Rules rule set.  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1001](../codequality/ca1001--types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1009](../codequality/ca1009--declare-event-handlers-correctly.md)|Declare event handlers correctly|  
|[CA1016](../codequality/ca1016--mark-assemblies-with-assemblyversionattribute.md)|Mark assemblies with AssemblyVersionAttribute|  
|[CA1033](../codequality/ca1033--interface-methods-should-be-callable-by-child-types.md)|Interface methods should be callable by child types|  
|[CA1049](../codequality/ca1049--types-that-own-native-resources-should-be-disposable.md)|Types that own native resources should be disposable|  
|[CA1060](../codequality/ca1060--move-p-invokes-to-nativemethods-class.md)|Move P/Invokes to NativeMethods class|  
|[CA1061](../codequality/ca1061--do-not-hide-base-class-methods.md)|Do not hide base class methods|  
|[CA1063](../codequality/ca1063--implement-idisposable-correctly.md)|Implement IDisposable correctly|  
|[CA1065](../codequality/ca1065--do-not-raise-exceptions-in-unexpected-locations.md)|Do not raise exceptions in unexpected locations|  
|[CA1301](../codequality/ca1301--avoid-duplicate-accelerators.md)|Avoid duplicate accelerators|  
|[CA1400](../codequality/ca1400--p-invoke-entry-points-should-exist.md)|P/Invoke entry points should exist|  
|[CA1401](../codequality/ca1401--p-invokes-should-not-be-visible.md)|P/Invokes should not be visible|  
|[CA1403](../codequality/ca1403--auto-layout-types-should-not-be-com-visible.md)|Auto layout types should not be COM visible|  
|[CA1404](../codequality/ca1404--call-getlasterror-immediately-after-p-invoke.md)|Call GetLastError immediately after P/Invoke|  
|[CA1405](../codequality/ca1405--com-visible-type-base-types-should-be-com-visible.md)|COM visible type base types should be COM visible|  
|[CA1410](../codequality/ca1410--com-registration-methods-should-be-matched.md)|COM registration methods should be matched|  
|[CA1415](../codequality/ca1415--declare-p-invokes-correctly.md)|Declare P/Invokes correctly|  
|[CA1821](../codequality/ca1821--remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA1900](../codequality/ca1900--value-type-fields-should-be-portable.md)|Value type fields should be portable|  
|[CA1901](../codequality/ca1901--p-invoke-declarations-should-be-portable.md)|P/Invoke declarations should be portable|  
|[CA2002](../codequality/ca2002--do-not-lock-on-objects-with-weak-identity.md)|Do not lock on objects with weak identity|  
|[CA2100](../codequality/ca2100--review-sql-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2101](../codequality/ca2101--specify-marshaling-for-p-invoke-string-arguments.md)|Specify marshaling for P/Invoke string arguments|  
|[CA2108](../codequality/ca2108--review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2111](../codequality/ca2111--pointers-should-not-be-visible.md)|Pointers should not be visible|  
|[CA2112](../codequality/ca2112--secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../codequality/ca2114--method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2116](../codequality/ca2116--aptca-methods-should-only-call-aptca-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../codequality/ca2117--aptca-types-should-only-extend-aptca-base-types.md)|APTCA types should only extend APTCA base types|  
|[CA2122](../codequality/ca2122--do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../codequality/ca2123--override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../codequality/ca2124--wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../codequality/ca2126--type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2131](../codequality/ca2131--security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../codequality/e758afa1-8bde-442a-8a0a-bd1ea7b0ce4d.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../codequality/ca2133--delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../codequality/ca2134--methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2137](../codequality/ca2137--transparent-methods-must-contain-only-verifiable-il.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../codequality/a14c4d32-f079-4f3a-956c-a1657cde0f66.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2140](../codequality/ca2140--transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../codequality/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2146](../codequality/ca2146--types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../codequality/ca2147--transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../codequality/ca2149--transparent-methods-must-not-call-into-native-code.md)|Transparent methods must not call into native code|  
|[CA2200](../codequality/ca2200--rethrow-to-preserve-stack-details.md)|Rethrow to preserve stack details|  
|[CA2202](../codequality/ca2202--do-not-dispose-objects-multiple-times.md)|Do not dispose objects multiple times|  
|[CA2207](../codequality/ca2207--initialize-value-type-static-fields-inline.md)|Initialize value type static fields inline|  
|[CA2212](../codequality/ca2212--do-not-mark-serviced-components-with-webmethod.md)|Do not mark serviced components with WebMethod|  
|[CA2213](../codequality/ca2213--disposable-fields-should-be-disposed.md)|Disposable fields should be disposed|  
|[CA2214](../codequality/ca2214--do-not-call-overridable-methods-in-constructors.md)|Do not call overridable methods in constructors|  
|[CA2216](../codequality/ca2216--disposable-types-should-declare-finalizer.md)|Disposable types should declare finalizer|  
|[CA2220](../codequality/ca2220--finalizers-should-call-base-class-finalizer.md)|Finalizers should call base class finalizer|  
|[CA2229](../codequality/ca2229--implement-serialization-constructors.md)|Implement serialization constructors|  
|[CA2231](../codequality/ca2231--overload-operator-equals-on-overriding-valuetype.equals.md)|Overload operator equals on overriding ValueType.Equals|  
|[CA2232](../codequality/ca2232--mark-windows-forms-entry-points-with-stathread.md)|Mark Windows Forms entry points with STAThread|  
|[CA2235](../codequality/ca2235--mark-all-non-serializable-fields.md)|Mark all non-serializable fields|  
|[CA2236](../codequality/ca2236--call-base-class-methods-on-iserializable-types.md)|Call base class methods on ISerializable types|  
|[CA2237](../codequality/ca2237--mark-iserializable-types-with-serializableattribute.md)|Mark ISerializable types with SerializableAttribute|  
|[CA2238](../codequality/ca2238--implement-serialization-methods-correctly.md)|Implement serialization methods correctly|  
|[CA2240](../codequality/ca2240--implement-iserializable-correctly.md)|Implement ISerializable correctly|  
|[CA2241](../codequality/ca2241--provide-correct-arguments-to-formatting-methods.md)|Provide correct arguments to formatting methods|  
|[CA2242](../codequality/ca2242--test-for-nan-correctly.md)|Test for NaN correctly|  
|[CA1008](../codequality/ca1008--enums-should-have-zero-value.md)|Enums should have zero value|  
|[CA1013](../codequality/ca1013--overload-operator-equals-on-overloading-add-and-subtract.md)|Overload operator equals on overloading add and subtract|  
|[CA1303](../codequality/ca1303--do-not-pass-literals-as-localized-parameters.md)|Do not pass literals as localized parameters|  
|[CA1308](../codequality/ca1308--normalize-strings-to-uppercase.md)|Normalize strings to uppercase|  
|[CA1806](../codequality/ca1806--do-not-ignore-method-results.md)|Do not ignore method results|  
|[CA1816](../codequality/ca1816--call-gc.suppressfinalize-correctly.md)|Call GC.SuppressFinalize correctly|  
|[CA1819](../codequality/ca1819--properties-should-not-return-arrays.md)|Properties should not return arrays|  
|[CA1820](../codequality/ca1820--test-for-empty-strings-using-string-length.md)|Test for empty strings using string length|  
|[CA1903](../codequality/ca1903--use-only-api-from-targeted-framework.md)|Use only API from targeted framework|  
|[CA2004](../codequality/ca2004--remove-calls-to-gc.keepalive.md)|Remove calls to GC.KeepAlive|  
|[CA2006](../codequality/ca2006--use-safehandle-to-encapsulate-native-resources.md)|Use SafeHandle to encapsulate native resources|  
|[CA2102](../codequality/ca2102--catch-non-clscompliant-exceptions-in-general-handlers.md)|Catch non-CLSCompliant exceptions in general handlers|  
|[CA2104](../codequality/ca2104--do-not-declare-read-only-mutable-reference-types.md)|Do not declare read only mutable reference types|  
|[CA2105](../codequality/ca2105--array-fields-should-not-be-read-only.md)|Array fields should not be read only|  
|[CA2106](../codequality/ca2106--secure-asserts.md)|Secure asserts|  
|[CA2115](../codequality/ca2115--call-gc.keepalive-when-using-native-resources.md)|Call GC.KeepAlive when using native resources|  
|[CA2119](../codequality/ca2119--seal-methods-that-satisfy-private-interfaces.md)|Seal methods that satisfy private interfaces|  
|[CA2120](../codequality/ca2120--secure-serialization-constructors.md)|Secure serialization constructors|  
|[CA2121](../codequality/ca2121--static-constructors-should-be-private.md)|Static constructors should be private|  
|[CA2130](../codequality/ca2130--security-critical-constants-should-be-transparent.md)|Security critical constants should be transparent|  
|[CA2205](../codequality/ca2205--use-managed-equivalents-of-win32-api.md)|Use managed equivalents of Win32 API|  
|[CA2215](../codequality/ca2215--dispose-methods-should-call-base-class-dispose.md)|Dispose methods should call base class dispose|  
|[CA2221](../codequality/ca2221--finalizers-should-be-protected.md)|Finalizers should be protected|  
|[CA2222](../codequality/ca2222--do-not-decrease-inherited-member-visibility.md)|Do not decrease inherited member visibility|  
|[CA2223](../codequality/ca2223--members-should-differ-by-more-than-return-type.md)|Members should differ by more than return type|  
|[CA2224](../codequality/ca2224--override-equals-on-overloading-operator-equals.md)|Override equals on overloading operator equals|  
|[CA2226](../codequality/ca2226--operators-should-have-symmetrical-overloads.md)|Operators should have symmetrical overloads|  
|[CA2227](../codequality/ca2227--collection-properties-should-be-read-only.md)|Collection properties should be read only|  
|[CA2239](../codequality/ca2239--provide-deserialization-methods-for-optional-fields.md)|Provide deserialization methods for optional fields|  
|[CA1032](../codequality/ca1032--implement-standard-exception-constructors.md)|Implement standard exception constructors|  
|[CA1054](../codequality/ca1054--uri-parameters-should-not-be-strings.md)|URI parameters should not be strings|  
|[CA1055](../codequality/ca1055--uri-return-values-should-not-be-strings.md)|URI return values should not be strings|  
|[CA1056](../codequality/ca1056--uri-properties-should-not-be-strings.md)|URI properties should not be strings|  
|[CA1057](../codequality/ca1057--string-uri-overloads-call-system.uri-overloads.md)|String URI overloads call System.Uri overloads|  
|[CA1402](../codequality/ca1402--avoid-overloads-in-com-visible-interfaces.md)|Avoid overloads in COM visible interfaces|  
|[CA1406](../codequality/ca1406--avoid-int64-arguments-for-visual-basic-6-clients.md)|Avoid Int64 arguments for Visual Basic 6 clients|  
|[CA1407](../codequality/ca1407--avoid-static-members-in-com-visible-types.md)|Avoid static members in COM visible types|  
|[CA1408](../codequality/ca1408--do-not-use-autodual-classinterfacetype.md)|Do not use AutoDual ClassInterfaceType|  
|[CA1409](../codequality/ca1409--com-visible-types-should-be-creatable.md)|Com visible types should be creatable|  
|[CA1411](../codequality/ca1411--com-registration-methods-should-not-be-visible.md)|COM registration methods should not be visible|  
|[CA1412](../codequality/ca1412--mark-comsource-interfaces-as-idispatch.md)|Mark ComSource Interfaces as IDispatch|  
|[CA1413](../codequality/ca1413--avoid-non-public-fields-in-com-visible-value-types.md)|Avoid non-public fields in COM visible value types|  
|[CA1414](../codequality/ca1414--mark-boolean-p-invoke-arguments-with-marshalas.md)|Mark boolean P/Invoke arguments with MarshalAs|  
|[CA1600](../codequality/ca1600--do-not-use-idle-process-priority.md)|Do not use idle process priority|  
|[CA1601](../codequality/ca1601--do-not-use-timers-that-prevent-power-state-changes.md)|Do not use timers that prevent power state changes|  
|[CA1824](../codequality/ca1824--mark-assemblies-with-neutralresourceslanguageattribute.md)|Mark assemblies with NeutralResourcesLanguageAttribute|  
|[CA2001](../codequality/ca2001--avoid-calling-problematic-methods.md)|Avoid calling problematic methods|  
|[CA2003](../codequality/ca2003--do-not-treat-fibers-as-threads.md)|Do not treat fibers as threads|  
|[CA2135](../codequality/ca2135--level-2-assemblies-should-not-contain-linkdemands.md)|Level 2 assemblies should not contain LinkDemands|  
|[CA2136](../codequality/ca2136--members-should-not-have-conflicting-transparency-annotations.md)|Members should not have conflicting transparency annotations|  
|[CA2139](../codequality/45a0328a-add7-40f9-8934-dff59beb02b3.md)|Transparent methods may not use the HandleProcessCorruptingExceptions attribute|  
|[CA2142](../codequality/ca2142--transparent-code-should-not-be-protected-with-linkdemands.md)|Transparent code should not be protected with LinkDemands|  
|[CA2143](../codequality/ca2143--transparent-methods-should-not-use-security-demands.md)|Transparent methods should not use security demands|  
|[CA2144](../codequality/ca2144--transparent-code-should-not-load-assemblies-from-byte-arrays.md)|Transparent code should not load assemblies from byte arrays|  
|[CA2145](../codequality/81970700-b438-4b3b-9239-16887e16f7b7.md)|Transparent methods should not be decorated with the SuppressUnmanagedCodeSecurityAttribute|  
|[CA2204](../codequality/ca2204--literals-should-be-spelled-correctly.md)|Literals should be spelled correctly|  
|[CA2211](../codequality/ca2211--non-constant-fields-should-not-be-visible.md)|Non-constant fields should not be visible|  
|[CA2217](../codequality/ca2217--do-not-mark-enums-with-flagsattribute.md)|Do not mark enums with FlagsAttribute|  
|[CA2218](../codequality/ca2218--override-gethashcode-on-overriding-equals.md)|Override GetHashCode on overriding Equals|  
|[CA2219](../codequality/ca2219--do-not-raise-exceptions-in-exception-clauses.md)|Do not raise exceptions in exception clauses|  
|[CA2225](../codequality/ca2225--operator-overloads-have-named-alternates.md)|Operator overloads have named alternates|  
|[CA2228](../codequality/ca2228--do-not-ship-unreleased-resource-formats.md)|Do not ship unreleased resource formats|  
|[CA2230](../codequality/ca2230--use-params-for-variable-arguments.md)|Use params for variable arguments|  
|[CA2233](../codequality/ca2233--operations-should-not-overflow.md)|Operations should not overflow|  
|[CA2234](../codequality/ca2234--pass-system.uri-objects-instead-of-strings.md)|Pass System.Uri objects instead of strings|  
|[CA2243](../codequality/ca2243--attribute-string-literals-should-parse-correctly.md)|Attribute string literals should parse correctly|