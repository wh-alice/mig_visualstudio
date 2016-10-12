---
title: "Mixed Recommended Rules rule set"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: c3186b5b-0149-4a75-826e-e3539e4e703f
caps.latest.revision: 3
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
# Mixed Recommended Rules rule set
The Microsoft Mixed Recommended Rules focus on the most common and critical problems in your C++ projects that support the Common Language Runtime, including potential security holes, application crashes, and other important logic and design errors. You should include this rule set in any custom rule set you create for your C++ projects that support the Common Language Runtime. This ruleset is designed to be configured with the Visual Studio Professional edition and higher.  
  
|Rule|Description|  
|----------|-----------------|  
|[C6001](../VS_IDE/c6001.md)|Using Uninitialized Memory|  
|[C6011](../VS_IDE/c6011.md)|Dereferencing Null Pointer|  
|[C6029](../VS_IDE/c6029.md)|Use Of Unchecked Value|  
|[C6031](../VS_IDE/c6031.md)|Return Value Ignored|  
|[C6053](../VS_IDE/c6053.md)|Zero Termination From Call|  
|[C6054](../VS_IDE/c6054.md)|Zero Termination Missing|  
|[C6059](../VS_IDE/c6059.md)|Bad Concatenation|  
|[C6063](../VS_IDE/c6063.md)|Missing String Argument To Format Function|  
|[C6064](../VS_IDE/c6064.md)|Missing Integer Argument To Format Function|  
|[C6066](../VS_IDE/c6066.md)|Missing Pointer Argument To Format Function|  
|[C6067](../VS_IDE/c6067.md)|Missing String Pointer Argument To Format Function|  
|[C6101](../VS_IDE/c6101.md)|Returning uninitialized memory|  
|[C6200](../VS_IDE/c6200.md)|Index Exceeds Buffer Maximum|  
|[C6201](../VS_IDE/c6201.md)|Index Exceeds Stack Buffer Maximum|  
|[C6214](../VS_IDE/c6214.md)|Invalid Cast HRESULT To BOOL|  
|[C6215](../VS_IDE/c6215.md)|Invalid Cast BOOL To HRESULT|  
|[C6216](../VS_IDE/c6216.md)|Invalid Compiler-Inserted Cast BOOL To HRESULT|  
|[C6217](../VS_IDE/c6217.md)|Invalid HRESULT Test With NOT|  
|[C6220](../VS_IDE/c6220.md)|Invalid HRESULT Compare To -1|  
|[C6226](../VS_IDE/c6226.md)|Invalid HRESULT Assignment To -1|  
|[C6230](../VS_IDE/c6230.md)|Invalid HRESULT Use As Boolean|  
|[C6235](../VS_IDE/c6235.md)|Non-Zero Constant With Logical-Or|  
|[C6236](../VS_IDE/c6236.md)|Logical-Or With Non-Zero Constant|  
|[C6237](../VS_IDE/c6237.md)|Zero With Logical-And Loses Side Effects|  
|[C6242](../VS_IDE/c6242.md)|Local Unwind Forced|  
|[C6248](../VS_IDE/c6248.md)|Creating Null DACL|  
|[C6250](../VS_IDE/c6250.md)|Unreleased Address Descriptors|  
|[C6255](../VS_IDE/c6255.md)|Unprotected Use Of Alloca|  
|[C6258](../VS_IDE/c6258.md)|Using Terminate Thread|  
|[C6259](../VS_IDE/c6259.md)|Dead Code In Bitwise-Or Limited Switch|  
|[C6260](../VS_IDE/c6260.md)|Use Of Byte Arithmetic|  
|[C6262](../VS_IDE/c6262.md)|Excessive Stack Usage|  
|[C6263](../VS_IDE/c6263.md)|Using Alloca In Loop|  
|[C6268](../VS_IDE/c6268.md)|Missing Parentheses In Cast|  
|[C6269](../VS_IDE/c6269.md)|Pointer Dereference Ignored|  
|[C6270](../VS_IDE/c6270.md)|Missing Float Argument To Format Function|  
|[C6271](../VS_IDE/c6271.md)|Extra Argument To Format Function|  
|[C6272](../VS_IDE/c6272.md)|Non-Float Argument To Format Function|  
|[C6273](../VS_IDE/c6273.md)|Non-Integer Argumen To Format Function|  
|[C6274](../VS_IDE/c6274.md)|Non-Character Argument To Format Function|  
|[C6276](../VS_IDE/c6276.md)|Invalid String Cast|  
|[C6277](../VS_IDE/c6277.md)|Invalid CreateProcess Call|  
|[C6278](../VS_IDE/c6278.md)|Array-New Scalar-Delete Mismatch|  
|[C6279](../VS_IDE/c6279.md)|Scalar-New Array-Delete Mismatch|  
|[C6280](../VS_IDE/c6280.md)|Memory Allocation-Deallocation Mismatch|  
|[C6281](../VS_IDE/c6281.md)|Bitwise Relation Precedence|  
|[C6282](../VS_IDE/c6282.md)|Assignment Replaces Test|  
|[C6283](../VS_IDE/c6283.md)|Primitive Array-New Scalar-Delete Mismatch|  
|[C6284](../VS_IDE/c6284.md)|Invalid Object Argument To Format Function|  
|[C6285](../VS_IDE/c6285.md)|Logical-Or Of Constants|  
|[C6286](../VS_IDE/c6286.md)|Non-Zero Logical-Or Losing Side Effects|  
|[C6287](../VS_IDE/c6287.md)|Redundant Test|  
|[C6288](../VS_IDE/c6288.md)|Mutual Inclusion Over Logical-And Is False|  
|[C6289](../VS_IDE/c6289.md)|Mutual Exclusion Over Logical-Or Is True|  
|[C6290](../VS_IDE/c6290.md)|Logical-Not Bitwise-And Precedence|  
|[C6291](../VS_IDE/c6291.md)|Logical-Not Bitwise-Or Precedence|  
|[C6292](../VS_IDE/c6292.md)|Loop Counts Up From Maximum|  
|[C6293](../VS_IDE/c6293.md)|Loop Counts Down From Minimum|  
|[C6294](../VS_IDE/c6294.md)|Loop Body Never Executed|  
|[C6295](../VS_IDE/c6295.md)|Infinite Loop|  
|[C6296](../VS_IDE/c6296.md)|Loop Only Executed Once|  
|[C6297](../VS_IDE/c6297.md)|Result Of Shift Cast To Larger Size|  
|[C6299](../VS_IDE/c6299.md)|Bitfield To Boolean Comparison|  
|[C6302](../VS_IDE/c6302.md)|Invalid Character String Argument To Format Function|  
|[C6303](../VS_IDE/c6303.md)|Invalid Wide Character String Argument To Format Function|  
|[C6305](../VS_IDE/c6305.md)|Mismatched Size And Count Use|  
|[C6306](../VS_IDE/c6306.md)|Incorrect Variable Argument Function Call|  
|[C6308](../VS_IDE/c6308.md)|Realloc Leak|  
|[C6310](../VS_IDE/c6310.md)|Illegal Exception Filter Constant|  
|[C6312](../VS_IDE/c6312.md)|Exception Continue Execution Loop|  
|[C6314](../VS_IDE/c6314.md)|Bitwise-Or Precedence|  
|[C6317](../VS_IDE/c6317.md)|Not Not Complement|  
|[C6318](../VS_IDE/c6318.md)|Exception Continue Search|  
|[C6319](../VS_IDE/c6319.md)|Ignored By Comma|  
|[C6324](../VS_IDE/c6324.md)|String Copy Instead Of String Compare|  
|[C6328](../VS_IDE/c6328.md)|Potential Argument Type Mismatch|  
|[C6331](../VS_IDE/c6331.md)|VirtualFree Invalid Flags|  
|[C6332](../VS_IDE/c6332.md)|VirtualFree Invalid Parameter|  
|[C6333](../VS_IDE/c6333.md)|VirtualFree Invalid Size|  
|[C6335](../VS_IDE/c6335.md)|Leaking Process Handle|  
|[C6381](../VS_IDE/c6381.md)|Shutdown Information Missing|  
|[C6383](../VS_IDE/c6383.md)|Element-Count Byte-Count Buffer Overrun|  
|[C6384](../VS_IDE/c6384.md)|Pointer Size Division|  
|[C6385](../VS_IDE/c6385.md)|Read Overrun|  
|[C6386](../VS_IDE/c6386.md)|Write Overrun|  
|[C6387](../VS_IDE/c6387.md)|Invalid Parameter Value|  
|[C6388](../VS_IDE/c6388.md)|Invalid Parameter Value|  
|[C6500](../VS_IDE/c6500.md)|Invalid Attribute Property|  
|[C6501](../VS_IDE/c6501.md)|Conflicting Attribute Property Values|  
|[C6503](../VS_IDE/c6503.md)|References Cannot Be Null|  
|[C6504](../VS_IDE/c6504.md)|Null On Non-Pointer|  
|[C6505](../VS_IDE/c6505.md)|MustCheck On Void|  
|[C6506](../VS_IDE/c6506.md)|Buffer Size On Non-Pointer Or Array|  
|[C6507](assetId:///18f88cd1-d035-4403-a6a4-12dd0affcf21)|Null Mismatch At Dereference Zero|  
|[C6508](../VS_IDE/c6508.md)|Write Access On Constant|  
|[C6509](../VS_IDE/c6509.md)|Return Used On Precondition|  
|[C6510](../VS_IDE/c6510.md)|Null Terminated On Non-Pointer|  
|[C6511](../VS_IDE/c6511.md)|MustCheck Must Be Yes Or No|  
|[C6513](../VS_IDE/c6513.md)|Element Size Without Buffer Size|  
|[C6514](../VS_IDE/c6514.md)|Buffer Size Exceeds Array Size|  
|[C6515](../VS_IDE/c6515.md)|Buffer Size On Non-Pointer|  
|[C6516](../VS_IDE/c6516.md)|No Properties On Attribute|  
|[C6517](../VS_IDE/c6517.md)|Valid Size On Non-Readable Buffer|  
|[C6518](../VS_IDE/c6518.md)|Writable Size On Non-Writable Buffer|  
|[C6519](assetId:///2b6326b0-0539-4d26-8fb1-720114933232)|Invalid annotation: value of the 'NeedsRelease' property must be Yes or No|  
|[C6521](assetId:///e98d0ae3-6f13-47b2-9a15-15d4055af9ef)|Invalid Size String Dereference|  
|[C6522](../VS_IDE/c6522.md)|Invalid Size String Type|  
|[C6523](assetId:///11397a31-b224-46b0-afb7-d49ca576a3bb)|Invalid Size String Parameter|  
|[C6525](../VS_IDE/c6525.md)|Invalid Size String Unreachable Location|  
|[C6526](assetId:///59c590c7-0098-4166-a1ac-87f324596002)|Invalid Size String Buffer Type|  
|[C6527](../VS_IDE/c6527.md)|Invalid annotation: 'NeedsRelease' property may not be used on values of void type|  
|[C6530](../VS_IDE/c6530.md)|Unrecognized Format String Style|  
|[C6540](../VS_IDE/c6540.md)|The use of attribute annotations on this function will invalidate all of its existing __declspec annotations|  
|[C6551](../VS_IDE/c6551.md)|Invalid size specification: expression not parsable|  
|[C6552](../VS_IDE/c6552.md)|Invalid Deref= or Notref=: expression not parsable|  
|[C6701](../VS_IDE/c6701.md)|The value is not a valid Yes/No/Maybe value|  
|[C6702](../VS_IDE/c6702.md)|The value is not a string value|  
|[C6703](../VS_IDE/c6703.md)|The value is not a number|  
|[C6704](../VS_IDE/c6704.md)|Unexpected Annotation Expression Error|  
|[C6705](../VS_IDE/c6705.md)|Expected number of arguments for annotation does not match actual number of arguments for annotation|  
|[C6706](../VS_IDE/c6706.md)|Unexpected Annotation Error for annotation|  
|[C6995](../VS_IDE/c6995.md)|Failed to save XML Log file|  
|[C26100](../VS_IDE/c26100.md)|Race condition|  
|[C26101](../VS_IDE/c26101.md)|Failing to use interlocked operation properly|  
|[C26110](../VS_IDE/c26110.md)|Caller failing to hold lock|  
|[C26111](../VS_IDE/c26111.md)|Caller failing to release lock|  
|[C26112](../VS_IDE/c26112.md)|Caller cannot hold any lock|  
|[C26115](../VS_IDE/c26115.md)|Failing to release lock|  
|[C26116](../VS_IDE/c26116.md)|Failing to acquire or to hold lock|  
|[C26117](../VS_IDE/c26117.md)|Releasing unheld lock|  
|[C26140](../VS_IDE/c26140.md)|Concurrency SAL annotation error|  
|[C28020](../VS_IDE/c28020.md)|The expression is not true at this call|  
|[C28021](../VS_IDE/c28021.md)|The parameter being annotated must be a pointer|  
|[C28022](../VS_IDE/c28022.md)|The function class(es) on this function do not match the function class(es) on the typedef used to define it.|  
|[C28023](../VS_IDE/c28023.md)|The function being assigned or passed should have a _Function_class\_ annotation for at least one of the class(es)|  
|[C28024](../VS_IDE/c28024.md)|The function pointer being assigned to is annotated with the function class, which is not contained in the function class(es) list.|  
|[C28039](../VS_IDE/c28039.md)|The type of actual parameter should exactly match the type|  
|[C28112](../VS_IDE/c28112.md)|A variable which is accessed via an Interlocked function must always be accessed via an Interlocked function.|  
|[C28113](../VS_IDE/c28113.md)|Accessing a local variable via an Interlocked function|  
|[C28125](../VS_IDE/c28125.md)|The function must be called from within a try/except block|  
|[C28137](../VS_IDE/c28137.md)|The variable argument should instead be a (literal) constant|  
|[C28138](../VS_IDE/c28138.md)|The constant argument should instead be variable|  
|[C28159](../VS_IDE/c28159.md)|Consider using another function instead.|  
|[C28160](../VS_IDE/c28160.md)|Error annotation|  
|[C28163](../VS_IDE/c28163.md)|The function should never be called from within a try/except block|  
|[C28164](../VS_IDE/c28164.md)|The argument is being passed to a function that expects a pointer to an object (not a pointer to a pointer)|  
|[C28182](../VS_IDE/c28182.md)|Dereferencing NULL pointer. The pointer contains the same NULL value as another pointer did.|  
|[C28183](../VS_IDE/c28183.md)|The argument could be one value, and is a copy of the value found in the pointer|  
|[C28193](../VS_IDE/c28193.md)|The variable holds a value that must be examined|  
|[C28196](../VS_IDE/c28196.md)|The requirement is not satisfied. (The expression does not evaluate to true.)|  
|[C28202](../VS_IDE/c28202.md)|Illegal reference to non-static member|  
|[C28203](../VS_IDE/c28203.md)|Ambiguous reference to class member.|  
|[C28205](../VS_IDE/c28205.md)|_Success\_ or _On_failure\_ used in an illegal context|  
|[C28206](../VS_IDE/c28206.md)|Left operand points to a struct, use '->'|  
|[C28207](../VS_IDE/c28207.md)|Left operand is a struct, use '.'|  
|[C28209](../VS_IDE/c28209.md)|The declaration for symbol has a conflicting declaration|  
|[C28210](../VS_IDE/c28210.md)|Annotations for the __on_failure context must not be in explicit pre context|  
|[C28211](../VS_IDE/c28211.md)|Static context name expected for SAL_context|  
|[C28212](../VS_IDE/c28212.md)|Pointer expression expected for annotation|  
|[C28213](../VS_IDE/c28213.md)|The _Use_decl_annotations\_ annotation must be used to reference, without modification, a prior declaration.|  
|[C28214](../VS_IDE/c28214.md)|Attribute parameter names must be p1...p9|  
|[C28215](../VS_IDE/c28215.md)|The typefix cannot be applied to a parameter that already has a typefix|  
|[C28216](../VS_IDE/c28216.md)|The checkReturn annotation only applies to postconditions for the specific function parameter.|  
|[C28217](../VS_IDE/c28217.md)|For function, the number of parameters to annotation does not match that found at file|  
|[C28218](../VS_IDE/c28218.md)|For function paramteer, the annotation's parameter does not match that found at file|  
|[C28219](../VS_IDE/c28219.md)|Member of enumeration expected for annotation the parameter in the annotation|  
|[C28220](../VS_IDE/c28220.md)|Integer expression expected for annotation the parameter in the annotation|  
|[C28221](../VS_IDE/c28221.md)|String expression expected for the parameter in the annotation|  
|[C28222](../VS_IDE/c28222.md)|__yes, \__no, or \__maybe expected for annotation|  
|[C28223](../VS_IDE/c28223.md)|Did not find expected Token/identifier for annotation, parameter|  
|[C28224](../VS_IDE/c28224.md)|Annotation requires parameters|  
|[C28225](../VS_IDE/c28225.md)|Did not find the correct number of required parameters in annotation|  
|[C28226](../VS_IDE/c28226.md)|Annotation cannot also be a PrimOp (in current declaration)|  
|[C28227](../VS_IDE/c28227.md)|Annotation cannot also be a PrimOp (see prior declaration)|  
|[C28228](../VS_IDE/c28228.md)|Annotation parameter: cannot use type in annotations|  
|[C28229](../VS_IDE/c28229.md)|Annotation does not support parameters|  
|[C28230](../VS_IDE/c28230.md)|The type of parameter has no member.|  
|[C28231](../VS_IDE/c28231.md)|Annotation is only valid on array|  
|[C28232](../VS_IDE/c28232.md)|pre, post, or deref not applied to any annotation|  
|[C28233](../VS_IDE/c28233.md)|pre, post, or deref applied to a block|  
|[C28234](../VS_IDE/c28234.md)|__at expression does not apply to current function|  
|[C28235](../VS_IDE/c28235.md)|The function cannot stand alone as an annotation|  
|[C28236](../VS_IDE/c28236.md)|The annotation cannot be used in an expression|  
|[C28237](../VS_IDE/c28237.md)|The annotation on parameter is no longer supported|  
|[C28238](../VS_IDE/c28238.md)|The annotation on parameter has more than one of value, stringValue, and longValue. Use paramn=xxx|  
|[C28239](../VS_IDE/c28239.md)|The annotation on parameter has both value, stringValue, or longValue; and paramn=xxx. Use only paramn=xxx|  
|[C28240](../VS_IDE/c28240.md)|The annotation on parameter has param2 but no param1|  
|[C28241](../VS_IDE/c28241.md)|The annotation for function on parameter is not recognized|  
|[C28243](../VS_IDE/c28243.md)|The annotation for function on parameter requires more dereferences than the actual type annotated allows|  
|[C28244](../VS_IDE/c28244.md)|The annotation for function has an unparseable parameter/external annotation|  
|[C28245](../VS_IDE/c28245.md)|The annotation for function annotates 'this' on a non-member-function|  
|[C28246](../VS_IDE/c28246.md)|The parameter annotation for function does not match the type of the parameter|  
|[C28250](../VS_IDE/c28250.md)|Inconsistent annotation for function: the prior instance has an error.|  
|[C28251](../VS_IDE/c28251.md)|Inconsistent annotation for function: this instance has an error.|  
|[C28252](../VS_IDE/c28252.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28253](../VS_IDE/c28253.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28254](../VS_IDE/c28254.md)|dynamic_cast<>() is not supported in annotations|  
|[C28262](../VS_IDE/c28262.md)|A syntax error in the annotation was found in function, for annotation|  
|[C28263](../VS_IDE/c28263.md)|A syntax error in a conditional annotation was found for Intrinsic annotation|  
|[C28264](assetId:///bf6ea983-a06e-4752-a042-747a7dbf338c)|Result lists values must be constants.|  
|[C28267](../VS_IDE/c28267.md)|A syntax error in the annotations was found annotation in the function.|  
|[C28272](../VS_IDE/c28272.md)|The annotation for function, parameter when examining is inconsistent with the function declaration|  
|[C28273](../VS_IDE/c28273.md)|For function, the clues are inconsistent with the function declaration|  
|[C28275](../VS_IDE/c28275.md)|The parameter to _Macro_value\_ is null|  
|[C28279](../VS_IDE/c28279.md)|For symbol, a 'begin' was found without a matching 'end'|  
|[C28280](../VS_IDE/c28280.md)|For symbol, an 'end' was found without a matching 'begin'|  
|[C28282](../VS_IDE/c28282.md)|Format Strings must be in preconditions|  
|[C28285](../VS_IDE/c28285.md)|For function, syntax error in parameter|  
|[C28286](../VS_IDE/c28286.md)|For function, syntax error near the end|  
|[C28287](../VS_IDE/c28287.md)|For function, syntax Error in _At\_() annotation (unrecognized parameter name)|  
|[C28288](../VS_IDE/c28288.md)|For function, syntax Error in _At\_() annotation (invalid parameter name)|  
|[C28289](../VS_IDE/c28289.md)|For function: ReadableTo or WritableTo did not have a limit-spec as a parameter|  
|[C28290](../VS_IDE/c28290.md)|the annotation for function contains more Externals than the actual number of parameters|  
|[C28291](../VS_IDE/c28291.md)|post null/notnull at deref level 0 is meaningless for function.|  
|[C28300](../VS_IDE/c28300.md)|Expression operands of incompatible types for operator|  
|[C28301](../VS_IDE/c28301.md)|No annotations for first declaration of function.|  
|[C28302](../VS_IDE/c28302.md)|An extra _Deref\_ operator was found on annotation.|  
|[C28303](../VS_IDE/c28303.md)|An ambiguous _Deref\_ operator was found on annotation.|  
|[C28304](../VS_IDE/c28304.md)|An improperly placed _Notref\_ operator was found applied to token.|  
|[C28305](../VS_IDE/c28305.md)|An error while parsing a token was discovered.|  
|[C28306](../VS_IDE/c28306.md)|The annotation on parameter is obsolescent|  
|[C28307](../VS_IDE/c28307.md)|The annotation on parameter is obsolescent|  
|[C28350](../VS_IDE/c28350.md)|The annotation describes a situation that is not conditionally applicable.|  
|[C28351](../VS_IDE/c28351.md)|The annotation describes where a dynamic value (a variable) cannot be used in the condition.|  
|[CA1001](../VS_IDE/ca1001--types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1009](../VS_IDE/ca1009--declare-event-handlers-correctly.md)|Declare event handlers correctly|  
|[CA1016](../VS_IDE/ca1016--mark-assemblies-with-assemblyversionattribute.md)|Mark assemblies with AssemblyVersionAttribute|  
|[CA1033](../VS_IDE/ca1033--interface-methods-should-be-callable-by-child-types.md)|Interface methods should be callable by child types|  
|[CA1049](../VS_IDE/ca1049--types-that-own-native-resources-should-be-disposable.md)|Types that own native resources should be disposable|  
|[CA1060](../VS_IDE/ca1060--move-p-invokes-to-nativemethods-class.md)|Move P/Invokes to NativeMethods class|  
|[CA1061](../VS_IDE/ca1061--do-not-hide-base-class-methods.md)|Do not hide base class methods|  
|[CA1063](../VS_IDE/ca1063--implement-idisposable-correctly.md)|Implement IDisposable correctly|  
|[CA1065](../VS_IDE/ca1065--do-not-raise-exceptions-in-unexpected-locations.md)|Do not raise exceptions in unexpected locations|  
|[CA1301](../VS_IDE/ca1301--avoid-duplicate-accelerators.md)|Avoid duplicate accelerators|  
|[CA1400](../VS_IDE/ca1400--p-invoke-entry-points-should-exist.md)|P/Invoke entry points should exist|  
|[CA1401](../VS_IDE/ca1401--p-invokes-should-not-be-visible.md)|P/Invokes should not be visible|  
|[CA1403](../VS_IDE/ca1403--auto-layout-types-should-not-be-com-visible.md)|Auto layout types should not be COM visible|  
|[CA1404](../VS_IDE/ca1404--call-getlasterror-immediately-after-p-invoke.md)|Call GetLastError immediately after P/Invoke|  
|[CA1405](../VS_IDE/ca1405--com-visible-type-base-types-should-be-com-visible.md)|COM visible type base types should be COM visible|  
|[CA1410](../VS_IDE/ca1410--com-registration-methods-should-be-matched.md)|COM registration methods should be matched|  
|[CA1415](../VS_IDE/ca1415--declare-p-invokes-correctly.md)|Declare P/Invokes correctly|  
|[CA1821](../VS_IDE/ca1821--remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA1900](../VS_IDE/ca1900--value-type-fields-should-be-portable.md)|Value type fields should be portable|  
|[CA1901](../VS_IDE/ca1901--p-invoke-declarations-should-be-portable.md)|P/Invoke declarations should be portable|  
|[CA2002](../VS_IDE/ca2002--do-not-lock-on-objects-with-weak-identity.md)|Do not lock on objects with weak identity|  
|[CA2100](../VS_IDE/ca2100--review-sql-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2101](../VS_IDE/ca2101--specify-marshaling-for-p-invoke-string-arguments.md)|Specify marshaling for P/Invoke string arguments|  
|[CA2108](../VS_IDE/ca2108--review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2111](../VS_IDE/ca2111--pointers-should-not-be-visible.md)|Pointers should not be visible|  
|[CA2112](../VS_IDE/ca2112--secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../VS_IDE/ca2114--method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2116](../VS_IDE/ca2116--aptca-methods-should-only-call-aptca-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../VS_IDE/ca2117--aptca-types-should-only-extend-aptca-base-types.md)|APTCA types should only extend APTCA base types|  
|[CA2122](../VS_IDE/ca2122--do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../VS_IDE/ca2123--override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../VS_IDE/ca2124--wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../VS_IDE/ca2126--type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2131](../VS_IDE/ca2131--security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../VS_IDE/ca2132--default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../VS_IDE/ca2133--delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../VS_IDE/ca2134--methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2137](../VS_IDE/ca2137--transparent-methods-must-contain-only-verifiable-il.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../VS_IDE/ca2138--transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2140](../VS_IDE/ca2140--transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../VS_IDE/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2146](../VS_IDE/ca2146--types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../VS_IDE/ca2147--transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../VS_IDE/ca2149--transparent-methods-must-not-call-into-native-code.md)|Transparent methods must not call into native code|  
|[CA2200](../VS_IDE/ca2200--rethrow-to-preserve-stack-details.md)|Rethrow to preserve stack details|  
|[CA2202](../VS_IDE/ca2202--do-not-dispose-objects-multiple-times.md)|Do not dispose objects multiple times|  
|[CA2207](../VS_IDE/ca2207--initialize-value-type-static-fields-inline.md)|Initialize value type static fields inline|  
|[CA2212](../VS_IDE/ca2212--do-not-mark-serviced-components-with-webmethod.md)|Do not mark serviced components with WebMethod|  
|[CA2213](../VS_IDE/ca2213--disposable-fields-should-be-disposed.md)|Disposable fields should be disposed|  
|[CA2214](../VS_IDE/ca2214--do-not-call-overridable-methods-in-constructors.md)|Do not call overridable methods in constructors|  
|[CA2216](../VS_IDE/ca2216--disposable-types-should-declare-finalizer.md)|Disposable types should declare finalizer|  
|[CA2220](../VS_IDE/ca2220--finalizers-should-call-base-class-finalizer.md)|Finalizers should call base class finalizer|  
|[CA2229](../VS_IDE/ca2229--implement-serialization-constructors.md)|Implement serialization constructors|  
|[CA2231](../VS_IDE/ca2231--overload-operator-equals-on-overriding-valuetype.equals.md)|Overload operator equals on overriding ValueType.Equals|  
|[CA2232](../VS_IDE/ca2232--mark-windows-forms-entry-points-with-stathread.md)|Mark Windows Forms entry points with STAThread|  
|[CA2235](../VS_IDE/ca2235--mark-all-non-serializable-fields.md)|Mark all non-serializable fields|  
|[CA2236](../VS_IDE/ca2236--call-base-class-methods-on-iserializable-types.md)|Call base class methods on ISerializable types|  
|[CA2237](../VS_IDE/ca2237--mark-iserializable-types-with-serializableattribute.md)|Mark ISerializable types with SerializableAttribute|  
|[CA2238](../VS_IDE/ca2238--implement-serialization-methods-correctly.md)|Implement serialization methods correctly|  
|[CA2240](../VS_IDE/ca2240--implement-iserializable-correctly.md)|Implement ISerializable correctly|  
|[CA2241](../VS_IDE/ca2241--provide-correct-arguments-to-formatting-methods.md)|Provide correct arguments to formatting methods|  
|[CA2242](../VS_IDE/ca2242--test-for-nan-correctly.md)|Test for NaN correctly|