{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Interface=dom/objects/KeyboardEvent
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
As of Microsoft Internet Explorer 5, the event also fires for the following keys:
*Editing: BACKSPACE
*Navigation: PAGE UP, PAGE DOWN
*System: SHIFT+TAB

As of Microsoft Internet Explorer 4.0, the '''onkeyup''' event fires for the following keys:
*Editing: DELETE, INSERT
*Function: F1 - F12
*Letters: A - Z (uppercase and lowercase)
*Navigation: HOME, END, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
*Numerals: 0 - 9
*Symbols: ! @ # $ % ^ &amp; * ( ) _ - + {{=}} &lt; [ ] { } , . / ? \ {{!}} ' ` " ~
*System: ESC, SPACEBAR, SHIFT, TAB

Returns a number specifying the '''keyCode''' of the key that was released.
To invoke this event, do one of the following:
*Release any keyboard key.
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages===
*<code>[[dom/events/keydown|onkeydown]]</code>
*<code>[[dom/events/keypress|onkeypress]]</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}