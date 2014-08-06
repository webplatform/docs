{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the unencoded version of an encoded component of a Uniform Resource Identifier (URI).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=decodeURIComponent( encodedURIString ''')'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code first encodes and then decodes a URI.
|Code=var uriEncode = encodeURI ("http://www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);
 
 document.write (uriEncode);
 document.write("&lt;br/&gt;");
 document.write (uriDecode);
 
 // Output:
 // http://www.Not%20a%20URL.com
 // http://www.Not a URL.com
}}
}}
{{Remarks_Section
|Remarks=The required encodedURIString argument is a value representing an encoded URI component.

A URIComponent is part of a complete URI.

If the encodedURIString is not valid, a URIError occurs.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/decodeURI{{!}}decodeURI Function]]
* [[javascript/encodeURI{{!}}encodeURI Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/91b80x6x(v=vs.94).aspx
|HTML5Rocks_link=
}}