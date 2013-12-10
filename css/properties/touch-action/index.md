{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete
|Checked_Out=No
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
|Description=The user agent MAY determine any permitted touch behaviors, such as panning and zooming manipulations of the viewport, for touches that begin on the element.
}}{{CSS Property Value
|Data Type=none
|Description=Touches that begin on the element MUST NOT trigger default touch behaviors.
}}{{CSS Property Value
|Data Type=pan-x
|Description=The user agent MAY consider touches that begin on the element only for the purposes of horizontally scrolling the element's nearest ancestor with horizontally scrollable content.
}}{{CSS Property Value
|Data Type=pan-y
|Description=The user agent MAY consider touches that begin on the element only for the purposes of vertically scrolling the element's nearest ancestor with vertically scrollable content.
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
}}{{Single Example
|Language=HTML
|Description=The application has content that extends horizontally beyond the viewport and the desired behavior is to allow the user to scroll content left and right as desired without the browser moving the entire page.
|Code=<div style="touch-action: pan-x;">
    This element receives pointer events when not panning in the horizontal direction.
</div>
|LiveURL=http://www.love2dev.com/
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=https://dvcs.w3.org/hg/pointerevents/raw-file/tip/pointerEvents.html#the-touch-action-css-property
|Status=Editor's Draft
|Relevant_changes=Section 9.1
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
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE11
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
|Note=Supported as [http://msdn.microsoft.com/en-us/library/ie/hh772044(v=vs.85).aspx -ms-touch-action] with the following additional values:;pan-x: The element permits touch-driven panning on the horizontal axis. The touch pan is performed on the nearest ancestor with horizontally scrollable content.;pan-y: The element permits touch-driven panning on the vertical axis. The touch pan is performed on the nearest ancestor with vertically scrollable content.;pinch-zoom: The element permits pinch-zooming. The pinch-zoom is performed on the nearest ancestor with zoomable content.;manipulation: The element permits touch-driven panning and pinch-zooming. This is the shorthand equivalent of "pan-x pan-y pinch-zoom".;double-tap-zoom: The element permits double-tap-zooming. The double-tap-zoom is performed on the full page.
}}
}}
{{See_Also_Section
|Topic_clusters=Pointer Events
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/library/ie/hh772044.aspx
|HTML5Rocks_link=
}}