{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pRootNode|Data type=Node|Description=The root element or node to start traversing on.|Optional=}}
{{Method Parameter|Name=ulWhatToShow|Data type=Integer|Description=The type of nodes or elements to appear in the node list. For more information, see [[dom/traversal/properties/whatToShow|'''whatToShow''']].|Optional=}}
{{Method Parameter|Name=pFilter|Data type=VARIANT|Description=A custom NodeFilter function to use. For more information, see [[dom/traversal/properties/filter|'''filter''']]. Use null for no filter.|Optional=}}
{{Method Parameter|Name=fEntityReferenceExpansion|Data type=VARIANT_BOOL|Description=A flag that specifies whether entity reference nodes are expanded. For more information, see [[dom/traversal/properties/expandEntityReferences|'''expandEntityReferences''']].|Optional=}}
{{Method Parameter|Name=ppNodeIterator|Data type=IDOMNodeIterator|Description=Returns a [[dom/traversal/NodeIterator|'''NodeIterator''']] object.|Optional=}}
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
|-
|NotSupportedError
|pRootNode is null
|}
 

'''IDOMNodeIterator'''

Returns a [[dom/traversal/NodeIterator|'''NodeIterator''']] object.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example shows how to use [[dom/traversal/NodeIterator|'''NodeIterator''']] objects to find and remove references. The iterator returns all text nodes from the document '''body''' and searches for <code>Monday</code> in text and [[html/attributes/id|'''id''']] attributes of parent nodes. The script matches text by using the [[dom/properties/wholeText|'''wholeText''']] object of the node.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function noMondays()
{
    var ni {{=}} document.createNodeIterator(document.body, NodeFilter.SHOW_TEXT, null, false);
                
    var textNode {{=}} ni.nextNode();
    while (textNode) {
        if (textNode.wholeText.match('Monday') {{!}}{{!}} 
            textNode.parentNode.getAttribute('id') {{=}}{{=}} 'Monday')
        {
            textNode.parentNode.removeChild(textNode);
        }
        textNode {{=}} ni.nextNode();
    }
}
function refresh()                 
{
    window.location.reload( false );    // Reload our page.
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;Monday, Joe bought a turkey.&lt;/p&gt;
    &lt;p&gt;Tuesday, Bill bought a pound of nails.&lt;/p&gt;
    &lt;div&gt;Chuck called in sick Monday.&lt;/div&gt;
    &lt;p id{{=}}"Monday"&gt;CALL supplier today!&lt;/p&gt;
    &lt;p&gt;Wednesday's delivery was delayed.&lt;/p&gt;
    &lt;button onclick{{=}}"refresh()"&gt;Reload&lt;/button&gt;
    &lt;button onclick{{=}}"noMondays()"&gt;Lose Mondays&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use the '''createNodeIterator''' method when you want to focus on node content because [[dom/traversal/NodeIterator|'''NodeIterator''']] traverses a flat list of nodes in the document structure.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2


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