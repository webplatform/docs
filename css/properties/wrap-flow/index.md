{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies how exclusions impact inline content within block-level elements}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Media=visual
|Computed value=as specified except for element's whose ‘float’ computed value is not none, in which case the computed value is ‘auto’.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=No exclusion is created. Inline flow content interacts with the element as usual. 
}}{{CSS Property Value
|Data Type=both
|Description=Inline flow content can flow on all sides of the exclusion.
}}{{CSS Property Value
|Data Type=start
|Description=Inline flow content can flow around the start edge of the exclusion area but must leave the area next to the end edge of the exclusion empty.
}}{{CSS Property Value
|Data Type=end
|Description=Inline flow content can flow around the end edge of the exclusion area but must leave the area next to the start edge of the exclusion empty.
}}{{CSS Property Value
|Data Type=minimum
|Description=Inline flow content can flow around the edge of the exclusion with the smallest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.
}}{{CSS Property Value
|Data Type=maximum
|Description=Inline flow content can flow around the edge of the exclusion with the largest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.
}}{{CSS Property Value
|Data Type=clear
|Description=Inline flow content can only flow before and after the exclusion in the flow content's block direction and must leave the areas next to the start and end edges of the exclusion empty.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=If the property's computed value is ‘auto’, the element does not become an exclusion.

An exclusion affects the inline flow content descended from the exclusion's containing block and that of all descendant elements of the same containing block. All inline flow content inside the containing block of the exclusions is affected. To stop the effect of exclusions defined outside an element, the ‘wrap-through’ property can be used.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh772045(v=vs.85).aspx
|HTML5Rocks_link=
}}