{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns an error message string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=errorObj.'''message'''
}}
|Values={{JS Syntax Parameter
|Name=errorObj
|Required=Required
|Description=Instance of Error object.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example causes a TypeError exception to be thrown and displays the name of the error and its message.
|Code=try
 {
     // Cause an error.
     var x = y;
 }
 catch(e)
 {
     document.write ("Error Message: " + e.message);
     document.write ("&lt;br /&gt;");
     document.write ("Error Code: ");
     document.write (e.number &amp; 0xFFFF)
     document.write ("&lt;br /&gt;");
     document.write ("Error Name: " + e.name);
 }
}}{{Single Example
|Language=JavaScript
|Description=The output of this code is as follows.
|Code=Error Message: 'y' is undefined
 Error Code: 5009
 Error Name: TypeError
}}
}}
{{Remarks_Section
|Remarks=The message property returns a string that contains an error message associated with a specific error.

The description and message properties provide the same functionality. The description property provides backwards compatibility; the message property complies with the ECMA standard.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/description{{!}}description Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/5z00ybxa(v=vs.94).aspx
|HTML5Rocks_link=
}}