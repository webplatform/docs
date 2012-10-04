{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=type|Data type=BSTR|Description=The type of event [[dom/properties/type (event)|'''type''']] to register.|Optional=}}
{{Method Parameter|Name=useCapture|Data type=VARIANT_BOOL|Description=A '''Boolean''' value that specifies the event phase to add the event handler for:|Optional=}}
|Method_applies_to=dom/Node
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
Events are handled in two phases: capturing and bubbling. During the capturing phase, events are dispatched to parent objects before they are dispatched to event targets that are lower in the object hierarchy. During the bubbling phase, events are dispatched to target elements first and then to parent elements. You can register event handlers for either event phase. For more information, see [[dom/properties/eventPhase|'''eventPhase''']].
'''Note'''   Some events, such as [[dom/events/focus|'''onfocus''']], do not bubble. However, you can capture all events. You cannot capture events by elements that are not parents of the target element.
If you register multiple identical event handlers on the same event target, the duplicate event handlers are discarded.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 4.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/TextNode|TextNode]]</code>
*<code>window</code>
*<code>XMLHttpRequest</code>
*<code>[[apis/audio-video/AudioTrackList|AudioTrackList]]</code>
*<code>[[dom/methods/removeEventListener|removeEventListener]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}