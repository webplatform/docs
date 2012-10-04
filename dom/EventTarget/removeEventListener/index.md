{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=type|Data type=BSTR|Description=The event [[dom/properties/type (event)|'''type''']] that the event handler is registered for.|Optional=}}
{{Method Parameter|Name=listener|Data type=IDispatch|Description=The event handler function to remove.|Optional=}}
{{Method Parameter|Name=useCapture|Data type=VARIANT_BOOL|Description=A '''Boolean''' value that specifies the event phase to remove the event handler from:|Optional=}}
|Method_applies_to=dom/document,dom/Node
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
|E_FAIL
|The operation failed.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|E_FAIL
|The operation failed.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
If you register multiple identical event handlers for the same event type, the duplicate event handlers are discarded. You can remove only the first instance.
If the arguments for '''removeEventListener'''  do not identify a  registered event handler, the call to  '''removeEventListener''' has no effect.
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
*<code>[[dom/methods/addEventListener|addEventListener]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}