{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=newChild|Data type=IHTMLDOMNode|Description='''Object''' that specifies the new element to be inserted into the document.|Optional=}}
{{Method Parameter|Name=oldChild|Data type=IHTMLDOMNode|Description='''Object''' that specifies the existing element to be replaced.|Optional=}}
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''

Returns a reference to the object that is replaced.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''replaceChild''' method to replace a bold element from a '''div''' with an italic element.
|LiveURL=
|Code=
&lt;head&gt;
&lt;script&gt;
function replaceElement()
{
        //The first child of the div is the bold element.   
    var oChild{{=}}Div1.children(0);	
    var sInnerHTML {{=}} oChild.innerHTML;
    if (oChild.tagName{{=}}{{=}}"B")
    {
        oNewChild{{=}}document.createElement("I");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML{{=}}sInnerHTML
    }
    else
    {
        oNewChild{{=}}document.createElement("B");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML{{=}}sInnerHTML		
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id{{=}}"Div1" onclick{{=}}"replaceElement()"&gt;
Click anywhere in this sentence to toggle this &lt;strong&gt;word&lt;/strong&gt;
between bold and italic.&lt;/div&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The node to be replaced must be an immediate child of the parent object. The new node must be created using the [[dom/methods/createElement|'''createElement''']] method.
This property is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
Windows Internet Explorer 9. Exceptions are only supported when webpages are displayed in IE9 Standards mode.
In Microsoft Internet Explorer 6, This method now applies to the [[dom/attributes|'''attribute''']] object.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>b</code>
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
*<code>[[dom/documentType|documentType]]</code>
*<code>dt</code>
*<code>em</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
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
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
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
*<code>[[dom/processingInstruction|ProcessingInstruction]]</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
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