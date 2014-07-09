{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a value that indicates whether the object has children.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=bResult
|Javascript_data_type=Boolean
|Return_value_description=Boolean

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}The object contains HTML Elements or TextNode objects.
{{!}}-
{{!}}false
{{!}}The object does not contain HTML Elements or TextNodes.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example removes the first child node inside the element with the id "foo" if foo has child nodes.
|Code=var foo {{=}} document.getElementById("foo");

if ( foo.hasChildNodes() ) { 
  foo.removeChild( foo.childNodes[0] );
}
}}
}}
{{Notes_Section
|Notes====Remarks===
If the object contains HTML Elements or [[dom/TextNode|'''TextNodes''']], they can be accessed from the 
[[dom/Node/childNodes|'''childNodes''']] collection.
|Import_Notes====Syntax===
object.hasChildNodes() 
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.hasChildNodes Node.hasChildNodes]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536445(v=vs.85).aspx hasChildNodes() Method]
|HTML5Rocks_link=
}}