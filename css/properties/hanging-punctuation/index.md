{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|If a punctuation mark is present, this property determines if the punctuation mark hangs and whether it can be placed outside the line box and the start or at the end of a line of text.}}
{{CSS Property
|Initial value=none
|Applies to=inline elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=Not available
|Values={{CSS Property Value
|Data Type=none
|Description=No character hangs
}}{{CSS Property Value
|Data Type=first
|Description=This is an opening bracket or quote that is at the start of the first formatted line of an element that hangs. Any characters in the Unicode categories Ps, Pf, Pi are applied.
}}{{CSS Property Value
|Data Type=last
|Description=This is a closing bracket or quote of an element at the end of the last formatted line. The element hangs and this applies to any characters in the Unicode categories Pe, Pf, and Pi.
}}{{CSS Property Value
|Data Type=force-end
|Description=A stop or comma at the end of a line hangs
}}{{CSS Property Value
|Data Type=allow-end
|Description=A stop or comma at the end of a line hangs if it does not otherwise fit prior to justification.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=When measuring the line's contents for fit, alignment, or justification, the punctuation mark is not considered when it hangs. The mark may be placed outside the line box depending on the line's alignment.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#hanging-punctuation0
|Status=Working Draft
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
|Topic_clusters=Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}