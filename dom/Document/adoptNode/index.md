{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pNodeSource|Data type=IHTMLDOMNode|Description=A reference to the
'''element''' object   that  refers to the node to  move.|Optional=}}
{{Method Parameter|Name=ppNodeDest|Data type=IHTMLDOMNode3|Description=A reference to the
'''element''' object   that  refers to the node that has been moved, or a null value if the node cannot be moved.|Optional=}}
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
 

'''IHTMLDOMNode3'''

A reference to the
'''element''' object   that  refers to the node that has been moved, or a null value if the node cannot be moved.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example illustrates the '''adoptNode''' method and  shows one way to handle cases where the method fails.
|LiveURL=
|Code=
var oNode {{=}} document.adoptNode( oXHTMLNode );
if ( oNode {{=}}{{=}} null )
   oNode {{=}} document.importNode( oXHTMLNode );
parent.appendChild( oNode );
}}}}
{{Notes_Section
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