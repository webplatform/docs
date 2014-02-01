{{Page_Title}}
{{Flags}}
{{Summary_Section|Creates a new Boolean value.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= boolObj = new Boolean([ boolValue ])}}
|Values={{JS_Syntax_Parameter
|Name=boolObj
|Required=Required
|Description=The variable name to which the '''Boolean''' object is assigned.}}{{JS_Syntax_Parameter
|Name=boolValue
|Required=Optional
|Description=The initial Boolean value for the new object. If boolvalue is omitted, or is false , 0, null , NaN , or an empty string, the initial value of the Boolean object is false. Otherwise, the initial value is true.}}
}}
{{Remarks_Section
|Remarks=The '''Boolean''' object is a wrapper for the Boolean data type. JavaScript implicitly uses the '''Boolean''' object whenever a Boolean data type is converted to a '''Boolean''' object.

You rarely instantiate the '''Boolean''' object explicitly.
}}
==Properties==
The following table lists the properties of the '''Boolean''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Boolean/constructor|constructor Property]]
| Specifies the function that creates a Boolean.
|-
| [[javascript/Boolean/prototype|prototype Property]]
| Returns a reference to the prototype for a Boolean.
|}
==Methods==
The following table lists the methods of the '''Boolean''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Boolean/toString|toString Method]]
| Returns a string representation of a Boolean.
|-
| [[javascript/Boolean/valueOf|valueOf Method]]
| Gets a reference to the Boolean.
|}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t7bkhaz6(v=vs.94).aspx
|HTML5Rocks_link=
}}