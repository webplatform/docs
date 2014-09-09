{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Compatibility table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a [[dom/TreeWalker|'''TreeWalker''']] object that you can use to traverse filtered lists of nodes or elements in a document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=rootNode
|Data type=DOM Node
|Description=The root element or node to start traversing on.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=whatToShow
|Data type=unsigned long
|Description=The type of nodes or elements to appear in the node list. For more information, see [[dom/NodeIterator/whatToShow|'''whatToShow''']].
|Optional=No
}}{{Method Parameter
|Index=2
|Name=filter
|Data type=DOM Node
|Description=A custom '''NodeFilter''' function to use. For more information, see [[dom/NodeIterator/filter|'''filter''']], or null for none.
|Optional=No
}}{{Method Parameter
|Index=3
|Name=entityReferenceExpansion
|Data type=Boolean
|Description=Whether entity reference nodes are expanded. For more information, see [[dom/NodeIterator/expandEntityReferences|'''expandEntityReferences''']].
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=treeWalker
|Javascript_data_type=DOM Node
|Return_value_description=A [[dom/TreeWalker|'''TreeWalker''']] instance object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example shows how to use [[dom/TreeWalker|'''TreeWalker''']] objects to find and remove references. The iterator returns all text nodes from the document '''body''' and searches for <code>Monday</code> in text and [[html/attributes/id|'''id''']] attributes of parent nodes. The script matches text by using the [[dom/Text/wholeText|'''wholeText''']] property of the node.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function noMondays()
{
    var tw {{=}} document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT, null, false);
                
    var textNode {{=}} tw.nextNode();
    while (textNode) {
        if (textNode.wholeText.match('Monday') {{!}}{{!}} 
            textNode.parentNode.getAttribute('id') {{=}}{{=}} 'Monday')
        {
            textNode.parentNode.removeChild(textNode);
        }
        textNode {{=}} tw.nextNode();
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
|LiveURL=
}}
}}
{{Notes_Section
|Usage=Use the '''createTreeWalker''' method when you want to navigate a representation of the document's hierarchical structure. If you would rather traverse a sequence of nodes without regard to document structure, use [[dom/Document/createNodeIterator|'''createNodeIterator''']].
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/traversal.html#Traversal-Document
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Document/createNodeIterator|createNodeIterator]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}