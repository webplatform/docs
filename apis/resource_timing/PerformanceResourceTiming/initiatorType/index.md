{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.}}
{{API_Object_Property
|Property_applies_to=apis/resource timing/PerformanceResourceTiming
|Read_only=Yes
|Return_value_description=DOMString (one of the following):
*css: The initiator is any CSS resource downloaded via the url() syntax, such as @import url(), background: url(), etc.
*embed: The initiator is the src attribute of the HTML <embed> element.
*img: The initiator is the src attribute of the HTML <img> element.
*link: The initiator is the href attribute of the HTML <link> element.
*object: The initiator is the data attribute of the HTML <object> element.
*script: The initiator is the src attribute of the HTML <script> element.
*subdocument: The initiator is the src attribute of the HTML <frame> or HTML <iframe> elements.
*svg: The initiator is the <svg> element and all resources downloaded as children of the <svg> element.
*xmlhttprequest: The initiator is a XMLHttpRequest object.
*other: The initiator is not of any type listed above.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}