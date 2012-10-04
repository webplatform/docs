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
|Description=When the [[css/properties/overflow|'''overflow''']] property is set to '''auto''', the content can exceed the dimensions of an element, and scroll bars appear. You can use the '''scrollWidth''' property to retrieve the width of the content within the element.

This example uses the '''scrollWidth''' property to compare the viewable width of the content to the actual width of a '''div''' element. The width of the element is exposed through the [[dom/properties/offsetWidth|'''offsetWidth''']] property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollWidth.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
function fnCheckScroll() {
   var iScrollWidth {{=}} oDiv.scrollWidth;
   var iOffsetWidth {{=}} oDiv.offsetWidth;
   var iDifference {{=}} iScrollWidth - iOffsetWidth;
   alert("Width: " + iOffsetWidth
      + "\nscrollWidth: " + iScrollWidth
      + "\nDifference: " + iDifference); 
}
&lt;/script&gt;
...
&lt;div id{{=}}"oDiv" style{{=}}"overflow: scroll; height{{=}} 50px; width{{=}} 400px; text-align: left" nowrap&gt;
	... 
&lt;/div&gt;
&lt;button onclick{{=}}"fnCheckScroll()"&gt;Check scrollWidth&lt;/button&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The width is the distance between the left and right edges of the object's visible content.
This property is read-only on HTML documents, and read-write on fixed regions.
For more information about how to access the dimension and location of objects on the page through the Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>applet</code>
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
*<code>custom</code>
*<code>dd</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>head</code>
*<code>hn</code>
*<code>html</code>
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
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>menu</code>
*<code>meta</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
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
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/properties/scrollHeight|scrollHeight]]</code>
*<code>[[dom/properties/scrollLeft|scrollLeft]]</code>
*<code>[[dom/properties/scrollTop|scrollTop]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}