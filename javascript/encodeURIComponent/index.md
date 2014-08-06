{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Encodes a text string as a valid component of a Uniform Resource Identifier (URI).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=encodeURIComponent( encodedURIString ''')'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code first encodes a URI component and then decodes it.
|Code=var uriEncode = encodeURIComponent ("www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);
 
 document.write(uriEncode);
 document.write("&lt;br/&gt;");
 document.write(uriDecode);
 
 // Output:
 // www.Not%20a%20URL.com
 // www.Not a URL.com
}}
}}
{{Remarks_Section
|Remarks=The required encodedURIString argument is a value representing an encoded URI component.

The '''encodeURIComponent''' function returns an encoded URI. If you pass the result to '''decodeURIComponent''' , the original string is returned. Because the '''encodeURIComponent''' function encodes all characters, be careful if the string represents a path such as /folder1/folder2/default.html. The slash characters will be encoded and will not be valid if sent as a request to a web server. Use the '''encodeURI''' function if the string contains more than a single URI component.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/decodeURI{{!}}decodeURI Function]]
* [[javascript/decodeURIComponent{{!}}decodeURIComponent Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/aeh9cef7(v=vs.94).aspx
|HTML5Rocks_link=
}}