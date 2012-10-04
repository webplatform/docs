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
|Description=This example uses the '''className''' attribute to apply one or more styles to an HTML element.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/className.htm
|Code=
&lt;HEAD&gt;
    &lt;STYLE TYPE{{=}}"text/css"&gt;
        P {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    &lt;/STYLE&gt;
&lt;/HEAD&gt;

&lt;BODY&gt;
    &lt;P&gt;
        Large text, no class specified, one implied.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"redText"&gt;
        Large text, .redText class specified.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"blueText italicText"&gt;
        Large text, .blueText and .italicText classes specified.
    &lt;/P&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The class is typically used to associate a particular style rule in a style sheet with the element.
You can apply multiple styles to an element by specifying more than one style for the '''CLASS''' attribute. To apply multiple styles to a single element, use the following syntax:
 <code>&lt;ELEMENT CLASS {{=}} "sClass [ sClass2 [ sClass3 ... ] ]" ... &gt;</code>
By default, the property is equal to the string assigned to the '''className''' property of the given object, or null if the attribute is not explicitly assigned.
When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:
#Element
#'''CLASS'''
#[[html/attributes/id|'''ID''']]
#Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see [http://msdn.microsoft.com/en-us/library/240ww6sz(VS.71).aspx Introduction to Cascading Style Sheets].
Multiple styles are supported as of Microsoft Internet Explorer 5.
In Windows Internet Explorer 8, class names, such as <code>hslice</code> and <code>entry-title</code>, are used to identify portions of a webpage that can be monitored for updates (Web Slices). For more information, see Subscribing to Content with Web Slices.
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
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}