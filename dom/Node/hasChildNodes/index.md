{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs some more content.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a value that indicates whether the Node has any direct Node descendant of any type.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Node
|Example_object_name=element
|Return_value_name=hasChildNodes
|Javascript_data_type=Boolean
|Return_value_description=Whether or not  the Node contains any direct Node descendant of any type
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example removes the first child node inside the element with the id "foo" if foo has child nodes.
|Code=var foo {{=}} document.getElementById("foo");

if (foo.hasChildNodes()) { 
  foo.removeChild(foo.childNodes[0]);
}
}}
}}
{{Notes_Section
|Notes=If the Node contains any [[dom/Element|Element], [dom/Text|Text] or other type of nodes, they can be accessed from the 
[[dom/Node/childNodes|'''childNodes''']] collection.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-810594187
|Status=W3C Recommendation
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.hasChildNodes Node.hasChildNodes]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536445(v=vs.85).aspx hasChildNodes() Method]
|HTML5Rocks_link=
}}