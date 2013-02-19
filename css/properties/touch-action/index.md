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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/library/ie/hh772044.aspx
|HTML5Rocks_link=
}}