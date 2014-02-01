{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns or sets the numeric value associated with a specific error. The Error object's default property is '''number'''.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= object '''.number''' [ '''= ''' errorNumber ]}}
|Values={{JS_Syntax_Parameter
|Name=Object
|Required=
|Description=Any instance of the Error object.}}{{JS_Syntax_Parameter
|Name=errorNumber
|Required=
|Description=An integer representing an error.}}
}}
{{Remarks_Section
|Remarks=An error number is a 32-bit value. The upper 16-bit word is the facility code, and the lower word is the error code. To determine the error code, use the &amp; (bitwise And) operator to combine the number property with the hexadecimal number <code>0xFFFF</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example causes an exception to be thrown and displays the error code that is derived from the error number.

|Code= try
     {
     // Cause an error.
     var x = y;
     }
 catch(e)
     {
     document.write ("Error Code: ");
     document.write (e.number &amp; 0xFFFF)
     document.write ("&lt;br /&gt;");
     
     document.write ("Facility Code: ")
     document.write(e.number&gt;&gt;16 &amp; 0x1FFF)
     document.write ("&lt;br /&gt;");
  
     document.write ("Error Message: ")
     document.write (e.message)
     }
}}{{Single_Example
|Language=JavaScript
|Description=The output of this code is as follows.

|Code= Error Code: 5009
 Facility Code: 10
 Error Message: 'y' is undefined
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/description{{!}}description Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hc53e755(v=vs.94).aspx
|HTML5Rocks_link=
}}