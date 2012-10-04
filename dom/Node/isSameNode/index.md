{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=otherNode|Data type=IHTMLDOMNode3|Description=The node to be compared to the node that is executing the method.|Optional=}}
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

Boolean

{| class="wikitable"
|-
!Return value
!Description
|-
|true
|The node specified in the otherNode parameter refers to the same node.
|-
|false
|The nodes are not the same node.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This determines whether or not two references refer to the same node.  If the references refer to the same node, you can use the references interchangeably, even when using a proxy.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>applet</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>audio</code>
*<code>button</code>
*<code>div</code>
*<code>[[dom/document|document]]</code>
*<code>[[dom/documentType|documentType]]</code>
*<code>[[dom/processingInstruction|ProcessingInstruction]]</code>
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
*<code>IHTMLDOMNode3</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}