{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Determines whether a supplied number is finite.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=isFinite(number)
}}
|Values={{JS Syntax Parameter
|Name=number
|Required=Required
|Description=Any numeric value
}}
}}
{{JS_Return_Value
|Description=Returns true if ''number'' is any value other than '''NaN''', -Infinity or Infinity. In those three cases, it returns '''false'''.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=isFinite(); // false, because its NaN
isFinite(42); // true
isFinite(-Infinity); //false
isFinite(4 / 0); //false
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/isNaN{{!}}isNaN Function]]
* [[javascript/Infinity{{!}}Infinity]]
* [[javascript/NaN{{!}}NaN]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/h5s8dazc(v=vs.94).aspx
|HTML5Rocks_link=
}}