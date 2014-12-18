{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.}}
{{API_Object_Property
|Property_applies_to=apis/resource timing/PerformanceResourceTiming
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
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
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example assumes an HTML page containing a resource such as
<img src="https://www.webplatform.org/logo/logo-with-text.png" />
|Code=var resources = window.performance.getEntriesByType('resource');
alert("initiatorType: " + resources[0].initiatorType);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}