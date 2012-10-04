{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/KeyboardEvent
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''charCode''' property represents the character code during the [[dom/events/keypress|'''onkeypress''']] event and the unmodified scan code of the key during [[dom/events/keydown|'''onkeydown''']] and [[dom/events/keyup|'''onkeyup''']] events. To detect whether the Alt, Ctrl, Meta, or Shift key is also pressed, see the [[dom/properties/altKey|'''altKey''']], [[dom/properties/ctrlKey|'''ctrlKey''']], [[dom/properties/metaKey|'''metaKey''']], or [[dom/properties/shiftKey|'''shiftKey''']] property of the event.
The '''charCode''' property  is provided for compatibility only. The latest version of the Document Object Model (DOM) Events specification defines a [[dom/properties/key|'''key''']] property instead.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/char|char]]</code>
*<code>[[dom/properties/key|key]]</code>
*<code>[[dom/properties/keyCode|keyCode]]</code>
*<code>[[dom/properties/which (keyboard)|which]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}