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
|Description=This example shows how to determine the position of a '''td''' object. Although the '''td''' object appears to the far right in the document, its position is close to the x-axis and y-axis, because its offset parent is a [[html/elements/table|'''table''']] object rather than the document body.
|LiveURL='''Note'''  For Internet Explorer 4.0, this same example returns a position of 0,0 because the offset parent is the table row.
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
  &lt;TITLE&gt;Elements: Positions&lt;/TITLE&gt;
  &lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;

  function showPosition()
  {
    var oElement {{=}} document.all.oCell;
    
    alert("The TD element is at (" + oElement.offsetLeft + 
          "," + oElement.offsetTop + ")\n" + "The offset parent is " 
          + oElement.offsetParent.tagName );
  }
  &lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"showPosition()"&gt;
&lt;P&gt;This document contains a right-aligned table.
&lt;TABLE BORDER{{=}}1 ALIGN{{=}}right&gt;
  &lt;TR&gt;
    &lt;TD ID{{=}}oCell&gt;This is a small table.&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Most of the time the '''offsetParent''' property returns the '''body''' object.
'''Note'''  In Microsoft Internet Explorer 5, the '''offsetParent''' property returns the [[html/elements/table|'''table''']] object for the '''td''' object; in Microsoft Internet Explorer 4.0 it returns the '''tr''' object. You can use the [[dom/traversal/properties/parentElement|'''parentElement''']] property to retrieve the immediate container of the table cell.
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
*<code>Measuring Element Dimension and Location with CSSOM in Internet Explorer 9</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}