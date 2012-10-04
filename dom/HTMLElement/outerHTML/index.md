{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''outerHTML''' property to copy an object, accompanying attributes, and children to a list when a user clicks one of the objects.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnCopyHTML(){
   var oWorkItem {{=}} event.srcElement;
   if((oWorkItem.tagName !{{=}} "UL") &amp;&amp; (oWorkItem.tagName !{{=}} "LI")){
      alert("Adding " + oWorkItem.outerHTML + " to the list.");
      oScratch.innerHTML +{{=}} oWorkItem.outerHTML + "&lt;BR&gt;";
   }
}	
&lt;/SCRIPT&gt;

&lt;UL onclick {{=}} "fnCopyHTML()"&gt;
&lt;LI&gt;&lt;B&gt;Bold text&lt;/B&gt;
&lt;LI&gt;&lt;I&gt;Italic text&lt;/I&gt;
&lt;LI&gt;&lt;U&gt;Underlined text&lt;/U&gt;
&lt;LI&gt;&lt;STRIKE&gt;Strikeout text&lt;/STRIKE&gt;
&lt;/UL&gt;
&lt;P&gt;
&lt;DIV ID {{=}} "oScratch" &gt;
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''outerHTML''' property is read-only on the '''caption''', '''col''', '''colGroup''', '''html''', '''head''', '''body''', '''frameSet''', '''tBody''', '''td''', '''tFoot''', '''th''', '''tHead''', and '''tr''' objects.
The property can be any valid string containing a combination of text and tags.
When the property is set, the given string completely replaces the object, including its start and end tags. If the string contains HTML tags, the string is parsed and formatted as it is placed into the document.
You can set this property only after the [[dom/events/load|'''onload''']] event fires on the '''window'''. When dynamically creating a tag using [[dom/traversal/TextRange|'''TextRange''']], [[dom/properties/innerdom/innerHTML|'''innerHTML''']], or '''outerHTML''', use Microsoft JScript to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported.
You can change the value of the '''title''' element using the [[dom/document|'''document''']].'''TITLE''' property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model. For example, use the [[dom/properties/rowIndex|'''rowIndex''']] property or the [[dom/properties/rows (table)|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/methods/insertRow|'''insertRow''']] and [[dom/methods/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/properties/cellIndex|'''cellIndex''']] property or the [[dom/properties/cellSpacing|'''cells''']] collection. You can add or delete rows using the [[dom/methods/insertCell|'''insertCell''']] and [[dom/methods/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/properties/innerdom/innerHTML|'''innerHTML''']] property.
This property is accessible at run time as of Microsoft Internet Explorer 5. Removing elements at run time, before the closing tag has been parsed, can prevent other areas of the document from rendering.
|Import_Notes=
===Syntax===
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
*<code>article</code>
*<code>aside</code>
*<code>b</code>
*<code>bdo</code>
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
*<code>custom</code>
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
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
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
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>[[dom/methods/insertAdjacentHTML|insertAdjacentHTML]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}