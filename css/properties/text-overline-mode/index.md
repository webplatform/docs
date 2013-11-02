{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the mode for the overline text decoration, determining whether the text decoration affects the space characters or not.}}
{{CSS Property
|Initial value=continuous
|Applies to=all elements with and generated content with textual content
|Inherited=No
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=No
|Values={{CSS Property Value
|Data Type=continuous
|Description=This value means that the line is continuous.
}}{{CSS Property Value
|Data Type=skip-white-space
|Description=This means that space characters will not be lined.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Currently not implemented in any browser, so example is incomplete.
|Code=p {
  text-overline-mode: skip-white-space;
}
|LiveURL=http://code.webplatform.org/gist/7283851
}}
}}
{{Notes_Section
|Notes=Not implemented in any browser, but Chrome has a placeholder property for it (which may fool any feature detectors into thinking it works).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Text Module
|URL=http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-mode
|Status=Candidate Recommendation
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