{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Assigns a specified pointer to an element. This method is used to ensure that an element continues to receive pointer events even if the contact moves off the element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=pointerID
|Data type=Number
|Description=The pointer to assign to the element.
|Optional=No
}}
|Method_applies_to=dom/Element
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Capturing the current pointer can improve usability by reducing the touch precision required when interacting with an element. For example, if a button is touched and held, and the user's finger slides off the button before raising it (breaking the contact), the button might not receive the [[dom/objects/PointerEvent/pointerup|pointerup]] event. This could cause the button to stay depressed forever. By assigning the pointer to the button element with ''setPointerCapture'', the button receives pointer events, including the ''pointerup'' event that signals the button to return to its initial state.

The capture will be released when the pointer is removed (onpointerup) or explicitly released by calling the [[dom/methods/releasePointerCapture|releasePointerCapture]] method. There are cases the element could lose the capture. For example, if the touch moves outside the window or some other element captures the touch, then the element that had the capture will lose the capture. The element that lost the capture will receive a [[dom/PointerEvent/lostpointercapture|lostpointercapture]] event.
|Notes=When a pointer is captured to an element, the parent and ancestor elements receive a [[dom/objects/PointerEvent/gotpointercapture|gotpointercapture]] event during capture and bubble phase.

If the specified pointerId does not match any existing pointers, a [[dom/DOMException|DOMException]] is thrown with the name ''InvalidPointerId''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=Sections 4 and 7
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=IE10
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Pointer Events
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/library/ie/hh771882.aspx
|HTML5Rocks_link=
}}