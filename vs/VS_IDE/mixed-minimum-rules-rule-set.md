---
title: "Mixed Minimum Rules rule set"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: bc8df61c-19af-40ab-a871-315807e5f4bf
caps.latest.revision: 4
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
# Mixed Minimum Rules rule set
The Microsoft Mixed Minimum Rules focus on the most critical problems in your C++ projects that support the Common Language Runtime, including potential security holes and application crashes. You should include this rule set in any custom rule set you create for your C++ projects that support the Common Language Runtime.  
  
|Rule|Description|  
|----------|-----------------|  
|[C6001](../VS_IDE/c6001.md)|Using Uninitialized Memory|  
|[C6011](../VS_IDE/c6011.md)|Dereferencing Null Pointer|  
|[C6029](../VS_IDE/c6029.md)|Use Of Unchecked Value|  
|[C6053](../VS_IDE/c6053.md)|Zero Termination From Call|  
|[C6059](../VS_IDE/c6059.md)|Bad Concatenation|  
|[C6063](../VS_IDE/c6063.md)|Missing String Argument To Format Function|  
|[C6064](../VS_IDE/c6064.md)|Missing Integer Argument To Format Function|  
|[C6066](../VS_IDE/c6066.md)|Missing Pointer Argument To Format Function|  
|[C6067](../VS_IDE/c6067.md)|Missing String Pointer Argument To Format Function|  
|[C6101](../VS_IDE/c6101.md)|Returning uninitialized memory|  
|[C6200](../VS_IDE/c6200.md)|Index Exceeds Buffer Maximum|  
|[C6201](../VS_IDE/c6201.md)|Index Exceeds Stack Buffer Maximum|  
|[C6270](../VS_IDE/c6270.md)|Missing Float Argument To Format Function|  
|[C6271](../VS_IDE/c6271.md)|Extra Argument To Format Function|  
|[C6272](../VS_IDE/c6272.md)|Non-Float Argument To Format Function|  
|[C6273](../VS_IDE/c6273.md)|Non-Integer Argumen To Format Function|  
|[C6274](../VS_IDE/c6274.md)|Non-Character Argument To Format Function|  
|[C6276](../VS_IDE/c6276.md)|Invalid String Cast|  
|[C6277](../VS_IDE/c6277.md)|Invalid CreateProcess Call|  
|[C6284](../VS_IDE/c6284.md)|Invalid Object Argument To Format Function|  
|[C6290](../VS_IDE/c6290.md)|Logical-Not Bitwise-And Precedence|  
|[C6291](../VS_IDE/c6291.md)|Logical-Not Bitwise-Or Precedence|  
|[C6302](../VS_IDE/c6302.md)|Invalid Character String Argument To Format Function|  
|[C6303](../VS_IDE/c6303.md)|Invalid Wide Character String Argument To Format Function|  
|[C6305](../VS_IDE/c6305.md)|Mismatched Size And Count Use|  
|[C6306](../VS_IDE/c6306.md)|Incorrect Variable Argument Function Call|  
|[C6328](../VS_IDE/c6328.md)|Potential Argument Type Mismatch|  
|[C6385](../VS_IDE/c6385.md)|Read Overrun|  
|[C6386](../VS_IDE/c6386.md)|Write Overrun|  
|[C6387](../VS_IDE/c6387.md)|Invalid Parameter Value|  
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
|[C28021](../VS_IDE/c28021.md)|The parameter being annotated must be a pointer|  
|[C28182](../VS_IDE/c28182.md)|Dereferencing NULL pointer. The pointer contains the same NULL value as another pointer did.|  
|[C28202](../VS_IDE/c28202.md)|Illegal reference to non-static member|  
|[C28203](../VS_IDE/c28203.md)|Ambiguous reference to class member.|  
|[C28205](../VS_IDE/c28205.md)|_Success\_ or _On_failure\_ used in an illegal context|  
|[C28206](../VS_IDE/c28206.md)|Left operand points to a struct, use '->'|  
|[C28207](../VS_IDE/c28207.md)|Left operand is a struct, use '.'|  
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
|[C28350](../VS_IDE/c28350.md)|The annotation describes a situation that is not conditionally applicable.|  
|[C28351](../VS_IDE/c28351.md)|The annotation describes where a dynamic value (a variable) cannot be used in the condition.|  
|[CA1001](../VS_IDE/ca1001--types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1821](../VS_IDE/ca1821--remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA2213](../VS_IDE/ca2213--disposable-fields-should-be-disposed.md)|Disposable fields should be disposed|  
|[CA2231](../VS_IDE/ca2231--overload-operator-equals-on-overriding-valuetype.equals.md)|Overload operator equals on overriding ValueType.Equals|