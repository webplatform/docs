{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=fDeep|Data type=VARIANT_BOOL|Description='''Boolean''' that specifies one of the following values:|Optional=}}
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
|Description=
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnClone(){
   /* the 'true' possible value specifies to clone
      the childNodes as well.
   */
   var oCloneNode {{=}} oList.cloneNode(true);
   /* When the cloned node is added,
   'oList' becomes a collection.
   */
   document.body.insertBefore(oCloneNode);
}
&lt;/SCRIPT&gt;
&lt;UL ID{{=}}"oList"&gt;
&lt;LI&gt;List node 1
&lt;LI&gt;List node 2
&lt;LI&gt;List node 3
&lt;LI&gt;List node 4
&lt;/UL&gt;
&lt;INPUT type{{=}}"button" value{{=}}"Clone List" onclick{{=}}"fnClone()"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''cloneNode''' method copies an object, attributes, and, if specified, 
the [[dom/properties/childNodes|'''childNodes''']].
When you refer to the [[html/attributes/id|'''ID''']] 
of a cloned element, a collection is returned.
'''cloneNode'''does not work on an '''IFRAME''' directly. You must call '''cloneNode'''through the [[dom/properties/all|'''all''']] collection. The following example demonstrates how to call '''cloneNode''' on an '''IFRAME'''.
 <code>&lt;HTML&gt;
 &lt;SCRIPT&gt;
 function fnBegin(){
     var fr {{=}} document.all.oFrame.cloneNode();
     console.log(document.body.innerHTML);
 }    
 &lt;/SCRIPT&gt;
 &lt;BODY onload{{=}}"fnBegin()"&gt;
     &lt;IFRAME id{{=}}"oFrame" src{{=}}"about:blank" 
         style{{=}}"border:1px solid black; position:absolute; top:20px; left:30px;
             width:350px; height:300px;"&gt;&lt;/IFRAME&gt;
 &lt;/BODY&gt;    
 &lt;/HTML&gt;</code>
If the object being cloned is an element and that element has expandos defined on it, the expandos are copied to the clone when '''cloneNode''' is called.  Other browsers might handle this differently.
In Microsoft Internet Explorer 6, this method applies to the [[dom/attributes|'''attribute''']] object.
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
*<code>applet</code>
*<code>area</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>article</code>
*<code>aside</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
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
*<code>embed</code>
*<code>fieldSet</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>font</code>
*<code>footer</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>header</code>
*<code>hgroup</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
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
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
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
*<code>script</code>
*<code>section</code>
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
*<code>Reference</code>
*<code>[[dom/methods/appendChild|appendChild]]</code>
*<code>[[dom/methods/removeNode|removeNode]]</code>
*<code>[[dom/methods/replaceNode|replaceNode]]</code>
*<code>[[dom/methods/swapNode|swapNode]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}