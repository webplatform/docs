{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/KeyboardEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/KeyboardEvent
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to retrieve information from the '''shiftKey''''''shiftKey''' property of the event object. When the user simultaneously presses the shift key and types a character in the first text field, the value "true" appears in the second text field.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onkeypressEX.htm
|Code=
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function checkKey()
{
if (window.event.shiftKey)  // checks whether the SHIFT key 
						    // is pressed
   {
   txtOutput.value {{=}} "true"; // returns TRUE if SHIFT is pressed 
						     // when the event fires
   }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Press the SHIFT key while pressing another key.&lt;br&gt;
    &lt;input type{{=}}"text" name{{=}}"txtEnterValue" onkeypress{{=}}"checkKey()"&gt; &lt;/p&gt;
&lt;p&gt;Indicates &amp;quot;true&amp;quot; if the shift key is used.&lt;br&gt;
    &lt;input type{{=}}"text" name{{=}}"txtOutput"&gt; &lt;/p&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
As of Microsoft Internet Explorer 4.0, the '''onkeypress''' event fires and can be canceled for the following keys:
*Letters: A - Z (uppercase and lowercase)
*Numerals: 0 - 9
*Symbols: ! @ # $ % ^ &amp; * ( ) _ - + {{=}} &lt; [ ] { } , . / ? \ {{!}} ' ` " ~
*System: ESC, SPACEBAR, ENTER

Returns a number specifying the Unicode value of the key that was pressed.
To invoke this event, do one of the following:
*Press any alphanumeric keyboard key.

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

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
*<code>audio</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/document|document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
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
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
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
*<code>source</code>
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
*<code>video</code>
*<code>window</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/events/change|onchange]]</code>
*<code>[[dom/events/keydown|onkeydown]]</code>
*<code>[[dom/events/keyup|onkeyup]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}