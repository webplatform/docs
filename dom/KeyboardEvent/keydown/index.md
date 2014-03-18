{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/KeyboardEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/KeyboardEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onkeydown''' event to cancel input from the keyboard.
|Code=&lt;script type{{=}}"text/javascript"&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onkeydown.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
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

In Internet Explorer 4.0, you cannot cancel the '''onkeydown''' event, but you can use the [[dom/KeyboardEvent/keypress|'''onkeypress''']] event to cancel keyboard events.
Returns a number specifying the '''keyCode''' of the key that was pressed.
To invoke this event, do one of the following:
*Press any keyboard key.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}