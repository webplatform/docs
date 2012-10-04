{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/xhr/objects/XMLHttpRequest
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the XML DOM to display the response body:
|LiveURL=
|Code=
var oReq {{=}} new XMLHttpRequest();
oReq.open("GET", "http://localhost/books.xml", false);
oReq.send();
console.log(oReq.responseXML.xml);
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use '''QueryInterface''' to convert the returned pointer ''p'' into '''IXMLDOMDocument'''.
For properties and methods supported by ''p'', refer to the documentation of IXMLDOMDocument/DOMDocument Members.
'''responseXML''' was introduced in Windows Internet Explorer 7.

====Using responseXML in Metro style apps using JavaScript====
In Metro style apps using JavaScript, this property returns a [[apis/xhr/objects/DOMParser|'''DOMParser''']] object instead of an IXMLDOMDocument object.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.7.7


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>Reference</code>
*<code>[[apis/xhr/properties/responseBody|responseBody]]</code>
*<code>responseText</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}