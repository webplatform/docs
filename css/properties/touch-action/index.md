{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Determines whether touch input may trigger default behavior supplied by the user agent, such as panning or zooming.}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements, SVG elements
|Inherited=No
|Media=visual
|Computed value=Same as specified value
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=The user agent determines the permitted touch behaviors, such as panning and zooming manipulations of the viewport, for touches that begin on the element.
}}{{CSS Property Value
|Data Type=none
|Description=Touches that begin on the element do not trigger default touch behaviors.
}}{{CSS Property Value
|Data Type=inherit
|Description=The property takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=You might find the following example within a fingerpainting application to ensure that its canvas doesn't move when a user touches and manipulates it. When a user touches this canvas and moves his or her finger, no manipulation will occur. DOM events will be sent instead.
|Code=canvas#fingerpainter {
  touch-action: none;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=Section 6.1
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Supported as [http://msdn.microsoft.com/en-us/library/ie/hh772044(v=vs.85).aspx -ms-touch-action] with the following additional values:
;pan-x
: The element permits touch-driven panning on the horizontal axis. The touch pan is performed on the nearest ancestor with horizontally scrollable content.
;pan-y
: The element permits touch-driven panning on the vertical axis. The touch pan is performed on the nearest ancestor with vertically scrollable content.
;pinch-zoom
: The element permits pinch-zooming. The pinch-zoom is performed on the nearest ancestor with zoomable content.
;manipulation
: The element permits touch-driven panning and pinch-zooming. This is the shorthand equivalent of "pan-x pan-y pinch-zoom".
;double-tap-zoom
: The element permits double-tap-zooming. The double-tap-zoom is performed on the full page.
}}
}}
{{See_Also_Section
|Manual_sections=Feature Detection
* [[dom/navigator/pointerEnabled|pointerEnabled]]
* [[dom/navigator/maxTouchPoints|maxTouchPoints]]

Events
* [[dom/events/gotpointercapture|gotpointercapture]]
* [[dom/events/lostpointercapture|lostpointercapture]]
* [[dom/events/pointercancel|pointercancel]]
* [[dom/events/pointerdown|pointerdown]]
* [[dom/events/pointerenter|pointerenter]]
* [[dom/events/pointerleave|pointerleave]]
* [[dom/events/pointermove|pointermove]]
* [[dom/events/pointerout|pointerout]]
* [[dom/events/pointerover|pointerover]]
* [[dom/events/pointerup|pointerup]]

Objects
* [[dom/objects/PointerEvent|PointerEvent]]

Methods
* [[dom/methods/setPointerCapture|setPointerCapture]]
* [[dom/methods/releasePointerCapture|releasePointerCapture]]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/library/ie/hh772044.aspx
|HTML5Rocks_link=
}}