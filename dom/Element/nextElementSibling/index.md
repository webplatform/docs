{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to get the content of a list by using firstElementSibling, nextElementSibling, previousElementSibling, and lastElementSibling.
|LiveURL=
|Code=
 &lt;!DOCTYPE html&gt;
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
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182722 Element Traversal Specification], Section 2.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>comment</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}