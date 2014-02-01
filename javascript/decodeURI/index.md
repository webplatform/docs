{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the unencoded version of an encoded Uniform Resource Identifier (URI).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= decodeURI( URIstring )}}
}}
{{Remarks_Section
|Remarks=The required URIstring argument is a value representing an encoded URI.

Use the '''decodeURI''' function instead of the deprecated '''unescape''' function.

The '''decodeURI''' function returns a string value.

If the URIString is not valid, a URIError occurs.

'''Applies To''' : [[javascript/Global{{!}}Global Object]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code first encodes a URI component and then decodes it.

|Code= var uriEncode = encodeURIComponent ("www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);
 
 document.write (uriEncode);
 document.write ("&lt;br/&gt;");
 document.write (uriDecode);
 
 // Output:
 // www.Not%20a%20URL.com
 // www.Not a URL.com
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/decodeURIComponent{{!}}decodeURIComponent Function]]
* [[javascript/encodeURI{{!}}encodeURI Function]]
* [[javascript/Global{{!}}Global Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ht8a077w(v=vs.94).aspx
|HTML5Rocks_link=
}}