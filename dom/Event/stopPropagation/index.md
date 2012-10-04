{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/objects/Event
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
You can stop event propagation in the capturing or bubbling event phase by calling the '''stopPropagation''' method. However, the event dispatchs to all event listeners on the current target (regardless of capturing or bubbling) before the event flow stops. To completely prevent any remaining handlers from running, use the [[dom/methods/stopImmediatePropagation|'''stopImmediatePropagation''']] method instead.
The  '''stopPropagation'''  method is similar to the [[dom/properties/cancelBubble|'''cancelBubble''']] event property of Windows Internet Explorer 8 and earlier versions.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/objects/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/objects/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/objects/CustomEvent|CustomEvent]]</code>
*<code>[[dom/objects/Event|Event]]</code>
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/FocusEvent|FocusEvent]]</code>
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/objects/MessageEvent|MessageEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/MutationEvent|MutationEvent]]</code>
*<code>[[dom/objects/MSSiteModeEvent|MSSiteModeEvent]]</code>
*<code>[[dom/objects/StorageEvent|StorageEvent]]</code>
*<code>[[dom/objects/TextEvent|TextEvent]]</code>
*<code>[[dom/objects/UIEvent|UIEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/eventPhase|eventPhase]]</code>
*<code>[[dom/methods/stopImmediatePropagation|stopImmediatePropagation]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}