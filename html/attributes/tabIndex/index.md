{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''tabIndex''' property to specify the tab order for three text fields. In addition, the Submit button is removed by specifying a negative value.
|Code=&lt;input type{{=}}"text" tabindex{{=}}"1"&gt; 
&lt;input type{{=}}"text"&gt;
&lt;input type{{=}}"text" tabindex{{=}}"2"&gt; 
&lt;input type{{=}}"submit" tabindex{{=}}"-1"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex1.htm
}}{{Single Example
|Description=This example uses the '''tabIndex''' property to assign a tab order to an unordered list. To cycle through the list's tab order, the user presses the TAB key. Since the list items can have focus, the focus rectangle surrounds each item the user selects.
|Code=&lt;ul&gt;
	&lt;li&gt;Item 1 (no tab)&lt;/li&gt;
	&lt;li&gt;Item 2 (no tab)&lt;/li&gt;
	&lt;li&gt;Item 3 (no tab)&lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
	&lt;li tabindex{{=}}"1"&gt;Tab Item 1&lt;/li&gt;
	&lt;li tabindex{{=}}"2"&gt;Tab Item 2&lt;/li&gt;
	&lt;li tabindex{{=}}"3"&gt;Tab Item 3&lt;/li&gt;
	&lt;li tabindex{{=}}"4"&gt;Tab Item 4&lt;/li&gt;
	&lt;li tabindex{{=}}"5"&gt;Tab Item 5&lt;/li&gt;
&lt;/ul&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex2.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''tabIndex''' value determines the tab order as follows:
#Objects with a positive '''tabIndex''' are selected in increasing ''p'' order and in source order to resolve duplicates.
#Objects with an '''tabIndex''' of zero are selected in source order.
#Objects with a negative '''tabIndex''' are omitted from the tabbing order.

An element can have focus if the '''tabIndex''' property is set to any valid negative or positive integer.
The following elements can have focus and are tab stops by default: 
[[html/elements/a|'''a''']], '''BODY''',
'''button''', '''frame''', '''iframe''', '''img''', '''input''', '''isIndex''', '''object''', '''select''', '''textArea'''.
The following elements can have focus by default but are not tab stops. These elements can be set as tab stops by setting the '''tabIndex''' property to a positive integer.  
'''applet''', '''div''', '''frameSet''', '''span''', [[html/elements/table|'''table''']], '''td'''.
Setting the '''tHead''' and '''tFoot''' elements to participate in the tab order will not cause the focus rectangle to display when either receives focus.
Elements can become part of the  accessibility hierarchy if the '''TABINDEX''' attribute is set as follows:
*For Microsoft Internet Explorer 5.01 and later, set the '''TABINDEX''' attribute to any value.
*For Microsoft Internet Explorer 5, set the '''TABINDEX''' attribute to a positive value.

For Internet Explorer 5.01 or above, the attribute may be set to any value in the valid range of <code>-32767</code> to <code>32767</code>.
Content of elements with a closing tag can have focus by default, but are not tab stops.  As of Internet Explorer 5, you can set the '''tabIndex''' property to a valid positive integer to force the content to have a tab stop.
Elements that receive focus can fire the [[dom/events/blur|'''onblur''']] and [[dom/events/focus|'''onfocus''']] events as of Microsoft Internet Explorer 4.0, and the [[dom/events/keydown|'''onkeydown''']], [[dom/events/keypress|'''onkeypress''']], and [[dom/events/keyup|'''onkeyup''']] events as of Internet Explorer 5.
|Import_Notes====Syntax===
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
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
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>hn</code>
*<code>hr</code>
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
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>marquee</code>
*<code>menu</code>
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
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}