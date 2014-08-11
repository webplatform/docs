{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
}}
{{Summary_Section|Returns the primitive value of the specified object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=object.valueOf( )
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=The required object reference is any intrinsic JavaScript object.

The '''valueOf''' method is defined differently for each intrinsic JavaScript object.

{{{!}} class='wikitable'
{{!}}-
! Object
! Return Value
{{!}}-
{{!}} Array
{{!}} Returns the array instance.
{{!}}-
{{!}} Boolean
{{!}} The Boolean value.
{{!}}-
{{!}} Date
{{!}} The stored time value in milliseconds since midnight, January 1, 1970 UTC.
{{!}}-
{{!}} Function
{{!}} The function itself.
{{!}}-
{{!}} Number
{{!}} The numeric value.
{{!}}-
{{!}} Object
{{!}} The object itself. This is the default.
{{!}}-
{{!}} String
{{!}} The string value.
{{!}}} 
The '''Math''' and Error objects do not have a '''valueOf''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/toString{{!}}toString Method (Object)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ftx8swz5(v=vs.94).aspx
|HTML5Rocks_link=
}}