{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=text|Data type=BSTR|Description=A '''String''' that specifies the [[dom/properties/nodeValue|'''nodeValue''']] property of the text node.|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''

'''TextNode'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnChangeNode(){
   var oTextNode {{=}} document.createTextNode("New Text");
   var oReplaceNode {{=}} oSpan.childNodes(0);
   oReplaceNode.replaceNode(oTextNode);
}
&lt;/SCRIPT&gt;
&lt;SPAN ID{{=}}"oSpan" onclick{{=}}"fnChangeNode()"&gt;
Original Text
&lt;/SPAN&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This method always returns S_OK, so you must check the returned ''newTextNode'' value. If ''newTextNode'' 
is NULL, the method failed to create a new text node.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/methods/createElement|createElement]]</code>
*<code>Conceptual</code>
*<code>About the W3C Document Object Model</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}