{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Determines whether two nodes are equal in their type, name and namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=otherNode
|Data type=DOM Node
|Description=The node to be compared to the node that is executing the method.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=isEqual
|Javascript_data_type=Boolean
|Return_value_description=Whether the node specified in the ''otherNode'' parameter is equal to the current node.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This method determines whether or not two nodes are equal.  Nodes are considered equal when the values of the following attributes are equal:
*[[dom/properties/nodeType|'''nodeType''']]
*[[dom/properties/nodeName|'''nodeName''']]
*[[dom/properties/localName|'''localName''']]
*[[dom/properties/namespaceURI|'''namespaceURI''']]
|Notes=Nodes can be equal without being the same.  Use [[dom/methods/isSameNode|'''isSameNode''']] to determine if two nodes are the same.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>applet</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>audio</code>
*<code>button</code>
*<code>div</code>
*<code>[[dom/Document|Document]]</code>
*<code>[[dom/documentType|documentType]]</code>
*<code>frame</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>label</code>
*<code>legend</code>
*<code>marquee</code>
*<code>[[html/elements/media|media]]</code>
*<code>object</code>
*<code>optGroup</code>
*<code>option</code>
*<code>select</code>
*<code>source</code>
*<code>span</code>
*<code>[[html/elements/table|table]]</code>
*<code>textArea</code>
*<code>[[dom/TextNode|TextNode]]</code>
*<code>video</code>
*<code>[[dom/methods/isSameNode|isSameNode]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}