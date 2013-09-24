{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate
|Checked_Out=No
|Editorial notes='''Obsolete; not in current W3C spec.'''
}}
{{Standardization_Status|N/A}}
{{API_Name|wrap-option (Obsolete)}}
{{Summary_Section|Obsolete and unsupported. Do not use.

This CSS property controls the text when it reaches the end of the block in which it is enclosed.
}}
{{CSS Property
|Initial value=wrap
|Applies to=all elements and generated content
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=wrap
|Description=The text is wrapped at the best line-breaking opportunity (if required) within the available block inline-progression dimension
}}{{CSS Property Value
|Data Type=no-wrap
|Description=The text is only wrapped where explicitly specified by preserved line feed characters. In the case when lines are longer than the available block width, the overflow will be treated in accordance with the 'overflow' property specified in the element.
}}{{CSS Property Value
|Data Type=soft-wrap
|Description=The text is wrapped after the last character which can fit before the ending-edge of the line and where explicitly specified by preserved line feed characters. No line-breaking algorithm is invoked. The intended usage is the rendering of a character terminal emulation.
}}{{CSS Property Value
|Data Type=emergency
|Description=The text is wrapped like for the 'wrap' case, except that the line-breaking algorithm will allow as a last resort option a text wrap after the last character which can fit before the ending edge of the line box, independently of 'line-break', 'word-break-cjk' and 'word-break-inside' properties. For example, this addresses the situation of very long words constrained in a fixed-width container with no scrolling allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Text Module
|URL=http://www.w3.org/TR/2003/CR-css3-text-20030514
|Status=Obsolete (previously a Candidate Recommendation)
|Relevant_changes=Section 7.1
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
|Manual_links=See also: [[css/properties/wrap-flow|wrap-flow]] property
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}