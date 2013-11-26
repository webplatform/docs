{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a [[dom/traversal/NodeIterator|'''NodeIterator''']] object that you can use to traverse filtered lists of nodes or elements in a document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=rootNode
|Data type=DOM Node
|Description=The root element or node to start traversing on.
|Optional=No
}}{{Method Parameter
|Name=whatToShow
|Data type=Number
|Description=The type of nodes or elements to appear in the node list. For more information, see [[dom/traversal/properties/whatToShow|'''whatToShow''']].
|Optional=No
}}{{Method Parameter
|Name=filter
|Data type=DOM Node
|Description=A custom NodeFilter function to use. For more information, see [[dom/traversal/properties/filter|'''filter''']]. Use null for no filter.
|Optional=No
}}{{Method Parameter
|Name=expandEntityReference
|Data type=Boolean
|Description=Whether entity reference nodes are expanded. For more information, see [[dom/traversal/properties/expandEntityReferences|'''expandEntityReferences''']].
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=nodeIterator
|Javascript_data_type=DOM Node
|Return_value_description=A [[dom/traversal/NodeIterator|'''NodeIterator''']] instance object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example shows how to use [[dom/traversal/NodeIterator|'''NodeIterator''']] objects to find and remove references. The iterator returns all text nodes from the document '''body''' and searches for <code>Monday</code> in text and [[html/attributes/id|'''id''']] attributes of parent nodes. The script matches text by using the [[dom/properties/wholeText|'''wholeText''']] object of the node.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
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
}}
}}
{{Notes_Section
|Notes=Use the '''createNodeIterator''' method when you want to focus on node content because [[dom/traversal/NodeIterator|'''NodeIterator''']] traverses a flat list of nodes in the document structure.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}