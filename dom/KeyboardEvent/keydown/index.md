{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/KeyboardEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''onkeydown''' event to cancel input from the keyboard.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onkeydown.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
function fnTrapKD(){
   if(oTrap.checked){
      oOutput.innerText+{{=}}"[trap {{=}} " + event.keyCode + "]";
      event.returnValue{{=}}false;
   }
   else{
      oOutput.innerText+{{=}}String.fromCharCode(event.keyCode);
   }
}
&lt;/script&gt;
&lt;input type{{=}}"checkbox" id{{=}}"oTrap"&gt;
&lt;input id{{=}}"oExample" type{{=}}"text" onkeydown{{=}}"fnTrapKD()"&gt;
&lt;textarea id{{=}}"oOutput" rows{{=}}"10" cols{{=}}"50"&gt;
&lt;/textarea&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can cancel all keys that fire the '''onkeydown''' event in HTML Applications, including most accelerator keys, such as ALT+F4.
As of Microsoft Internet Explorer 5, the event also fires for the following keys:
*Editing: BACKSPACE
*Navigation: PAGE UP, PAGE DOWN
*System: SHIFT+TAB

As of Internet Explorer 5, this event can be canceled for the following keys and key combinations by specifying '''event.returnValue{{=}}false''':
*Editing: BACKSPACE, DELETE
*Letters: A - Z (uppercase and lowercase)
*Navigation: PAGE UP, PAGE DOWN, END, HOME, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
*Numerals: 0 - 9
*Symbols: ! @ # $ % ^ &amp; * ( ) _ - + {{=}} &lt; [ ] { } , . / ? \ {{!}} ' ` " ~
*System: SPACEBAR, ESC, TAB, SHIFT+TAB

As of Microsoft Internet Explorer 4.0, the '''onkeydown''' event fires for the following keys:
*Editing: DELETE, INSERT
*Function: F1 - F12
*Letters: A - Z (uppercase and lowercase)
*Navigation: HOME, END, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
*Numerals: 0 - 9
*Symbols: ! @ # $ % ^ &amp; * ( ) _ - + {{=}} &lt; [ ] { } , . / ? \ {{!}} ' ` " ~
*System: ESC, SPACEBAR, SHIFT, TAB

In Internet Explorer 4.0, you cannot cancel the '''onkeydown''' event, but you can use the [[dom/events/keypress|'''onkeypress''']] event to cancel keyboard events.
Returns a number specifying the '''keyCode''' of the key that was pressed.
To invoke this event, do one of the following:
*Press any keyboard key.

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
*<code>[[dom/events/keyup|onkeyup]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}