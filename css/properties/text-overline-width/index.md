{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the line width for the overline text decoration.}}
{{CSS Property
|Initial value=auto
|Applies to=all elements with and generated content with textual content
|Inherited=No
|Media=visual
|Computed value=see prose
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=The user agent may use any algorithm to determine the text decoration width. The computed value is 'auto'.
}}{{CSS Property Value
|Data Type=normal
|Description=The text decoration width is the normal text decoration width for the nominal font. The computed value is 'normal'.
}}{{CSS Property Value
|Data Type=<number>
|Description=The text decoration width is the product of the <number> and the computed 'font-size'. The computed value is '<number>'.
}}{{CSS Property Value
|Data Type=<length>
|Description=The text decoration width is the length. The computed value is the corresponding absolute <length>.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The text decoration width is the product of the <percentage> and the computed 'font-size'. The computed value is the absolute <length>.
}}{{CSS Property Value
|Data Type=thin
|Description=Generates a thin line. The computed value is 'thin'.
}}{{CSS Property Value
|Data Type=medium
|Description=Generates a medium line. The computed value is 'medium'.
}}{{CSS Property Value
|Data Type=thick
|Description=Generates a thick line. The computed value is 'thick'.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Example incomplete because no browser implementation exists.
|Code=p {
  text-overline-width: thick;
}
|LiveURL=http://code.webplatform.org/gist/7284054
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Text Module
|URL=http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-style
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