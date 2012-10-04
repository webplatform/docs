{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/traversal/NodeIterator
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example searches for [[html/elements/table|'''table''']] and [[html/elements/a|'''anchor''']] tags and reports the value of the [[html/attributes/id|'''id''']] attribute. Although the [[dom/traversal/TreeWalker|'''TreeWalker''']] preserves the hierarchical relationship of nodes, you don't need to write recursive functions to walk the nodes in a hierarchy. The '''NodeFilter''' function skips nodes rather than rejecting them, which allows the function to examine all child nodes in the hierarchy.
|LiveURL='''Note'''  Appending content to the document while the [[dom/traversal/TreeWalker|'''TreeWalker''']] is searching for nodes can cause and endless loop. To prevent this, the example collects all possible output in a temporary variable and appends it to the document after the '''TreeWalker''' is finished.
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
// This is the NodeFilter function. It receives a node, and must return a NodeFilter flag.
function filter(node)
{
    if (node.tagName {{=}}{{=}} "TABLE" {{!}}{{!}} node.tagName {{=}}{{=}} "A")
        return NodeFilter.FILTER_ACCEPT;
    return NodeFilter.FILTER_SKIP;
}
function findNodes()
{
    var tw {{=}} document.createTreeWalker(document.body, NodeFilter.SHOW_ELEMENT, filter, false);
    
    var node, results {{=}} '';
    while (node {{=}} tw.nextNode()) {
        results +{{=}} node.id + "&lt;br/&gt;";
    }
    
    document.getElementById("results").innerHTML +{{=}} results;
}
function refresh()                 
{
    window.location.reload( false );    // Reload our page.
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;!-- this is a comment node--&gt;
    &lt;table border{{=}}"1" id{{=}}"myTable"&gt;
      &lt;tbody&gt;
        &lt;tr/&gt;   
        &lt;tr&gt;
          &lt;td&gt;&lt;a href{{=}}"" id{{=}}"myLink"&gt;Text inside anchor&lt;/a&gt;&lt;/td&gt;
        &lt;/tr&gt;
      &lt;/tbody&gt;
    &lt;/table&gt;
    
    &lt;div id{{=}}"results"&gt;Results:&lt;br/&gt;&lt;/div&gt;
    
&lt;button onclick{{=}}"findNodes()"&gt;Find Nodes&lt;/button&gt;
&lt;button onclick{{=}}"refresh()"&gt;Reload&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''NodeFilter''' is a callback function that provides customized filtering for [[dom/traversal/NodeIterator|'''NodeIterator''']] and [[dom/traversal/TreeWalker|'''TreeWalker''']]. The filter function accepts a node as its only parameter, and indicates whether the node is accepted, rejected, or skipped.
 <code>function myFilter(node) {
     // NodeFilter function that returns one of the following flags:
     // NodeFilter.FILTER_ACCEPT, NodeFilter.FILTER_REJECT, NodeFilter.FILTER_SKIP
 }</code>
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TreeWalker|TreeWalker]]</code>
*<code>[[dom/traversal/NodeIterator|NodeIterator]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}