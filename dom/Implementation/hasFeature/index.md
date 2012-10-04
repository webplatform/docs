{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrfeature|Data type=BSTR|Description=The name of the standard.|Optional=}}
{{Method Parameter|Name=version|Data type=VARIANT|Description=The version number of the standard.|Optional=}}
|Method_applies_to=dom/implementation
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

{| class="wikitable"
|-
!Return value
!Description
|-
|true
|Standard is implemented.
|-
|false
|Standard is not implemented.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the '''hasFeature''' method to test whether the object implements the DOM HTML standard.
|LiveURL=
|Code=
var bSupported {{=}} document.implementation.hasFeature("HTML","1.0");
}}}}
{{Notes_Section
|Notes=
===Remarks===
The ''bstrfeature'' parameter is case-insensitive.
'''hasFeature''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/implementation|implementation]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}