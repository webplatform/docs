{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object:
|LiveURL=
|Code=
if (window.XMLHttpRequest)
{
   var oReq {{=}} new XMLHttpRequest();
   if (oReq) {
      oReq.open("GET", "http://localhost/test.xml");
      oReq.send();
      console.log(oReq.statusText);
   }
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
Despite its name, this method does not return an '''XMLHttpRequest''' object directly. Instead, it returns an '''IHTMLXMLHttpRequestFactory''', which can be used to '''create''' an '''XMLHttpRequest''' object.
If the FEATURE_XMLHTTPREQUEST feature has been disabled, this method will return a '''Variant''' of type '''null'''. See '''CoInternetIsFeatureEnabled'''.
If the cross-domain request feature has been disabled in Windows Internet Explorer, this method returns null.
'''XMLHttpRequest''' was introduced in Windows Internet Explorer 7
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code><b/></code>
*<code>create</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}