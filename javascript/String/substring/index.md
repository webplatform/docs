{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the substring at the specified location within a String object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=strVariable. substring( start [, end ])
}}{{JS Syntax Format
|Format="String Literal".substring( start [, end ] ''')'''
}}
|Values={{JS Syntax Parameter
|Name=start
|Required=Required
|Description=The zero-based index integer indicating the beginning of the substring.
}}{{JS Syntax Parameter
|Name=end
|Required=Optional
|Description=The zero-based index integer indicating the end of the substring. The substring includes the characters up to, but not including, the character indicated by end.If end is omitted, the characters from start through the end of the original string are returned.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''substring''' method.
|Code=var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.substring(10, 15);
 document.write(ss);
 
 // Output:
 // brown
}}
}}
{{Remarks_Section
|Remarks=The substring method returns a string containing the substring from start up to, but not including, end.

The '''substring''' method uses the lower value of start and end as the beginning point of the substring. For example, strvar.substring(0, 3 ''')''' and strvar.substring(3, 0) return the same substring.

If either start or end is '''NaN''' or negative, it is replaced with zero.

The length of the substring is equal to the absolute value of the difference between start and end. For example, the length of the substring returned in strvar.substring(0, 3) and strvar.substring(3, 0) is three.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/substr{{!}}substr Method (String)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3cz15ahb(v=vs.94).aspx
|HTML5Rocks_link=
}}