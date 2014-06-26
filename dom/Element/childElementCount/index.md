{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the number of direct children of this node that are elements.  Read-only.}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=Yes
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to use '''childElementCount''' to get the number of ''immediate'' children of a div tag. Descendent children of the the div tag "divWithChildren" are ignored.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
        &lt;title&gt;childElementCount example&lt;/title&gt;
    &lt;script&gt;
        function GetCount () {
            var testArea {{=}} document.getElementById ("testArea");
            var childCount {{=}} 0;
                childCount {{=}} testArea.childElementCount;
            alert ("The number of child elements is " + childCount);
        }
    &lt;/script&gt; 
&lt;/head&gt;
&lt;body&gt;
    &lt;div id{{=}}"testArea" &gt;
    &lt;p&gt;This is the test area, which contains several children.&lt;/p&gt;
        &lt;div id{{=}}"divWithChildren"&gt;
            &lt;div&gt;a descendant child of a div&lt;/div&gt;
            &lt;div&gt;also a descendent child of a div&lt;/div&gt;
        &lt;/div&gt;
        &lt;p&gt;A paragraph tag to consider.&lt;/p&gt;
        &lt;input type{{=}}"text" size{{=}}"80" value{{=}}"And a text box as well"/&gt; 
    &lt;/div&gt;
    &lt;p&gt;&lt;input type{{=}}"button" value{{=}}"Get the number child elements in our test" name{{=}}"abutton"  onclick{{=}}"GetCount ();" /&gt; &lt;/p&gt;
    
&lt;/body&gt; 
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''childElementCount''' property only returns immediate children of the current node. It does not count descendent children of the immediate children.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182722 Element Traversal Specification], Section 2.5
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