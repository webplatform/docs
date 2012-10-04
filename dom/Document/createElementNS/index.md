{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pvarNS|Data type=VARIANT|Description=A '''String''' value that specifies the URI of the desired namespace.|Optional=}}
{{Method Parameter|Name=bstrTag|Data type=BSTR|Description=A '''String''' value  that contains  the name of the desired element.|Optional=}}
{{Method Parameter|Name=newElem|Data type=IHTMLElement|Description=A reference to the
'''element''' object   that  contains the new element.|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|}
 

'''IHTMLElement'''

A reference to the
'''element''' object   that  contains the new element.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example creates a circle element from the SVG namespace.
|LiveURL=
|Code=
var sNamespace {{=}} "http://www.w3.org/2000/svg";
var oCircle {{=}} document.createElementNS( sNamespace, "circle" );
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''createElementNS''' method is supported only for XML namespaces.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}