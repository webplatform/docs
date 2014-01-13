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
|Description=This example uses the '''innerText''' property to replace an object's contents. The object surrounding the text is not replaced.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerText.htm
|Code=
&lt;P ID{{=}}oPara&gt;Here's the text that will change.&lt;/P&gt;
:
&lt;BUTTON onclick{{=}}"oPara.innerText{{=}}'WOW! It changed!'"&gt;Change text&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oPara.innerText{{=}}'And back again'"&gt;Reset&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''innerText''' property is valid for block elements only. By definition, elements that do not have both an opening and closing tag cannot have an '''innerText''' property.
The '''innerText''' property is read-only on the '''html''', [[html/elements/table|'''table''']], '''tBody''', '''tFoot''', '''tHead''', and '''tr''' objects.
When the '''innerText''' property is set, the given string completely replaces the existing content of the object.
You can set this property only after the [[dom/events/load|'''onload''']] event fires on the '''window'''. When dynamically creating a tag using [[dom/traversal/TextRange|'''TextRange''']], [[dom/properties/innerdom/innerHTML|'''innerHTML''']], or [[dom/properties/outerdom/outerHTML|'''outerHTML''']], use Microsoft JScript to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported.
You can change the value of the '''title''' element using the [[dom/Document|'''Document''']].title property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model. For example, use the [[dom/properties/rowIndex|'''rowIndex''']] property or the [[dom/properties/rows (table)|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/methods/insertRow|'''insertRow''']] and [[dom/methods/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/properties/cellIndex|'''cellIndex''']] property or the [[dom/properties/cellSpacing|'''cells''']] collection. You can add or delete rows using the [[dom/methods/insertCell|'''insertCell''']] and [[dom/methods/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/properties/innerdom/innerHTML|'''innerHTML''']] property.
'''Security Warning:  ''' The '''innerText''' property can be used to safely add dynamic text to a webpage if the target element type is not a <code>script</code> element. With the exception of the <code>script</code> element, '''innerText''' does not execute script when inserting text into the Document Object Model (DOM) of a webpage.
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
*<code>[[dom/methods/insertAdjacentText|insertAdjacentText]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}