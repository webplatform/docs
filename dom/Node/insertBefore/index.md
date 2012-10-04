{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=newChild|Data type=IHTMLDOMNode|Description='''IHTMLDOMNode''' that specifies the new object to be inserted.|Optional=}}
{{Method Parameter|Name=refChild|Data type=VARIANT|Description='''Variant''' that specifies the placement of the new element.  If this parameter is specified, the new element will be inserted immediately before this existing child element.|Optional=}}
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''insertBefore''' method to insert a new item into an existing list.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertBefore.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
    function insertElement()
    {
        var nod{{=}}document.createElement("li");
        oUL1.insertBefore(nod, oLIYellow);
        nod.innerText{{=}}"Orange";
    }
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p onclick{{=}}"insertElement()"&gt;Click &lt;strong&gt;HERE&lt;/strong&gt; to add an item to the following list.&lt;/p&gt;
    &lt;ul id{{=}}"oUL1"&gt;
        &lt;li id{{=}}"oLIRed"&gt;Red&lt;/li&gt;
        &lt;li id{{=}}"oLIYellow"&gt;Yellow&lt;/li&gt;
        &lt;li id{{=}}"oLIBlue"&gt;Blue&lt;/li&gt;
    &lt;/ul&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Do not specify the ''refChild'' parameter when inserting the first child node. If children already exist and you do not specify the ''refChild'' parameter, the ''newChild'' becomes the last child of the parent object.
This method is accessible at run time. If elements are removed at run time, before the closing tag has been parsed, areas of the document might not render.
Windows Internet Explorer 9. Exceptions are only supported when webpages are displayed in IE9 Standards mode.
Microsoft Internet Explorer 6 and later.  The [[dom/attributes|'''attribute''']] object supports this method.
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
*<code>object</code>
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
*<code>About the W3C Document Object Model</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}