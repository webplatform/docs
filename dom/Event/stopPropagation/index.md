{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Prevents propagation of an event beyond the current target.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Event
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this method to stop event propagation in the capturing or bubbling event phase.
|Notes=The event dispatches to all event listeners on the current target (regardless of capturing or bubbling) before the event flow stops. To completely prevent any remaining handlers from running, use the [[dom/Event/stopImmediatePropagation|'''stopImmediatePropagation''']] method instead.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and earlier
|Note=A proprietary alternative for this method is the [[dom/properties/cancelBubble|cancelBubble]] property.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/CustomEvent|CustomEvent]]</code>
*<code>[[dom/DragEvent|DragEvent]]</code>
*<code>[[dom/Event|Event]]</code>
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