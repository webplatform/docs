{{Page_Title}}
{{Flags}}
{{Summary_Section|Encodes a text string as a valid Uniform Resource Identifier (URI)

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''encodeURI(''' URIString ''')'''}}
}}
{{Remarks_Section
|Remarks=The required URIString argument is a value representing an encoded URI.

The '''encodeURI''' function returns an encoded URI. If you pass the result to '''decodeURI''' , the original string is returned. The '''encodeURI''' function does not encode the following characters: ":", "/", ";", and "?". Use '''encodeURIComponent''' to encode these characters.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code first encodes and then decodes a URI.

|Code= var uriEncode = encodeURI ("http://www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);
 
 document.write(uriEncode);
 document.write("&lt;br/&gt;");
 document.write(uriDecode);
 
 // Output:
 // http://www.Not%20a%20URL.com
 // http://www.Not a URL.com
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/decodeURI{{!}}decodeURI Function]]
* [[javascript/decodeURIComponent{{!}}decodeURIComponent Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/xh9be5xc(v=vs.94).aspx
|HTML5Rocks_link=
}}