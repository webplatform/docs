{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=evt|Data type=IDOMEvent|Description=The event object to dispatch.|Optional=}}
{{Method Parameter|Name=pfResult|Data type=VARIANT_BOOL|Description=A '''Boolean''' value that indicates whether any of the event handlers called [[dom/methods/preventDefault|'''preventDefault''']].|Optional=}}
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|NotSupportedError
|You cannot dispatch an internal event.
|}
 

Boolean

A '''Boolean''' value that indicates whether any of the event handlers called [[dom/methods/preventDefault|'''preventDefault''']].

Default. The default action is permitted.

The caller should prevent the default action.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Events that the  '''dispatchEvent'''  method dispatches are subject to the same capturing and bubbling behavior as events that  the browser dispatches.
You cannot cancel some events. For more information, see the documentation for the event.
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
*<code>Reference</code>
*<code>[[dom/methods/addEventListener|addEventListener]]</code>
*<code>[[canvas/methods/createEvent|createEvent]]</code>
*<code>[[dom/methods/initEvent|initEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}