{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the event phase that is being evaluated.}}
{{API_Object_Property
|Property_applies_to=dom/Event
|Read_only=Yes
|Example_object_name=event
|Return_value_name=eventPhase
|Javascript_data_type=Number
|Return_value_description=0 is the initial and final phase (NONE), which means an event has not been dispatched, or the event is done dispatching.
1 is the capturing phase (CAPTURING_PHASE), which means it is currently running the capturing event handlers.
2 is the at target phase (AT_TARGET), which means it is currently running the event handlers that were added to the same element the event on which was dispatched.
3 is the bubbling phase (BUBBLING_PHASE), which means it is currently running event handlers of parent nodes of the original target element.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=During the capturing phase, events are dispatched to parent elements before objects that are lower in the hierarchy. Next, during the bubbling phase, events are dispatched to target elements followed by parent objects. The event phase is <code>AT_TARGET</code> when the element that receives the event ([[dom/Event/target|'''target''']]) is the same element as the element that is processing the event ([[dom/Event/currentTarget|'''currentTarget''']]). The target element receives both capture and bubble events if both are registered.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 4.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/CustomEvent|CustomEvent]]</code>
*<code>[[dom/Event|Event]]</code>
*<code>[[dom/DragEvent|DragEvent]]</code>
*<code>[[dom/FocusEvent|FocusEvent]]</code>
*<code>[[dom/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/MessageEvent|MessageEvent]]</code>
*<code>[[dom/MouseEvent|MouseEvent]]</code>
*<code>[[dom/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/MutationEvent|MutationEvent]]</code>
*<code>[[dom/StorageEvent|StorageEvent]]</code>
*<code>[[dom/TextEvent|TextEvent]]</code>
*<code>[[dom/UIEvent|UIEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}