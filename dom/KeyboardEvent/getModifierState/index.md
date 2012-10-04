{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=keyArg|Data type=BSTR|Description='''Alt'''



The left or right Alt key. 


'''AltGraph'''



The Ctrl and Alt keys. 


'''CapsLock'''



The Caps Lock toggle. 


'''Control'''



The left or right Ctrl key. 


'''Meta'''



The Meta/Control key. 


'''NumLock'''



The Num Lock toggle. 


'''Scroll'''



The Scroll Lock toggle. 


'''Shift'''



The left or right Shift key. 


'''Win'''



The left or right Windows logo key. 

|Optional=}}
{{Method Parameter|Name=state|Data type=VARIANT_BOOL|Description=true if the modifier key is active; otherwise, false.|Optional=}}
|Method_applies_to=dom/objects/KeyboardEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Boolean

true if the modifier key is active; otherwise, false.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Some keyboard configurations contain a left and right modifier key. To determine whether the left or right key is pressed, use the  [[dom/properties/location|'''location''']] property.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/altKey|altKey]]</code>
*<code>[[dom/properties/ctrlKey|ctrlKey]]</code>
*<code>[[dom/properties/metaKey|metaKey]]</code>
*<code>[[dom/properties/shiftKey|shiftKey]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}