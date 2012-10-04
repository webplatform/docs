{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''label''' object and the '''accessKey''' attribute to set focus on a text box. The '''label''' object makes it possible to underline the designated '''accessKey'''. You may also use the [[css/media queries/accelerator|'''-ms-accelerator''']] attribute to hide the underline until the ALT key is pressed.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accessKeyEX.htm
|Code=
&lt;label for{{=}}"fp1" accesskey{{=}}"1"&gt;#&lt;span style{{=}}"text-decoration: underline;"&gt;1&lt;/span&gt;: 
Press ALT+1 to set focus to textbox&lt;/label&gt;
&lt;input type{{=}}"text" name{{=}}"T1" value{{=}}"text1" size{{=}}"20" tabindex{{=}}"1" id{{=}}"fp1"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
By default, pressing an access key sets focus to an object. The object receives focus when the user simultaneously presses the ALT key and the access key assigned to an object. Some controls perform an action after receiving focus. For example, using '''accessKey''' on an '''input type{{=}}button''' causes the [[dom/events/click|'''onclick''']] event to fire. By comparison, applying the '''accessKey''' on a radio button causes the '''onclick''' event to fire and toggles the [[html/attributes/checked|'''checked''']] property, visibly selecting or deselecting the control.
'''Note'''  For elements that are not tab stops by default, such as a '''SPAN''', the [[html/attributes/tabIndex|'''tabIndex''']] property must be set on the element for the '''accessKey''' property to function.
In Windows Internet Explorer 7 and greater, ALT+D selects text in the Address bar, making D unavailable as a keyboard shortcut on a webpage.
As of Microsoft Internet Explorer 5, some scoped elements do not implicitly support the '''accessKey''' property. Instead, they support the property by setting the [[html/attributes/tabIndex|'''TABINDEX''']] attribute to any valid negative or positive integer.
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
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
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
*<code>header</code>
*<code>hgroup</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
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
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
*<code>object</code>
*<code>ol</code>
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
*<code>Reference</code>
*<code>[[css/media queries/accelerator|accelerator]]</code>
*<code>[[html/attributes/tabIndex|tabIndex]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}