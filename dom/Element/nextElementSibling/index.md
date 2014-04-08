{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Retrieves the element node that is a sibling to this element node (a direct child of the same parent) and is immediately after it in the DOM tree, ignoring text nodes, comment nodes and any other non-element nodes. If there is no next element sibling, the property value is null. Read-only.}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=Yes
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to get the content of a list using firstElementChild, nextElementSibling, previousElementSibling, and lastElementChild to traverse the document tree.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;IElementTraversal Example&lt;/title&gt;
    &lt;script&gt;
        function GetListItems () {
            var list {{=}} document.getElementById ("girls");       // find our list 
            var results {{=}} document.getElementById("results");   // get our results line element
            var oChild {{=}} list.lastElementChild;                 // start with the last item in list
            while (oChild) {                                    // get and display each item in list
               results.innerHTML +{{=}} "&lt;br/&gt;" + oChild.innerHTML;  
                oChild {{=}} oChild.previousElementSibling;         // get previous element in list
                }
        }        
        function GetListItems2 () {
            var list {{=}} document.getElementById ("girls");       // find our list
            var results {{=}} document.getElementById("results");   // get our results line element
            var oChild {{=}} list.firstElementChild;                // start with the first item in list 
            while (oChild) {                                    // get and display each item in list 
                results.innerHTML +{{=}} "&lt;br /&gt;" + oChild.innerHTML;   
                oChild {{=}} oChild.nextElementSibling;             // get next element in list 
                }
        }
        function refresh()                 
           {
             window.location.reload( false );           //reload our page
           }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;ol id{{=}}"girls"&gt;
        &lt;li&gt;Sugar&lt;/li&gt;
        &lt;li&gt;Spice&lt;/li&gt;
        &lt;li&gt;Everything nice&lt;/li&gt;
    &lt;/ol&gt;
    &lt;p id{{=}}"results"&gt;Girls have: &lt;/p&gt;
    &lt;p&gt;
    &lt;button onclick{{=}}"GetListItems ();"&gt;Get list backwards&lt;/button&gt;
    &lt;/p&gt;
   &lt;p&gt;
    &lt;button onclick{{=}}"GetListItems2 ();"&gt;Get list forwards&lt;/button&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;input type{{=}}"button" value{{=}}"Refresh page" onclick{{=}}"refresh()"   /&gt;   
    &lt;/p&gt;  
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182722 Element Traversal Specification], Section 2.4
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}