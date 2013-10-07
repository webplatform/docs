{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the treatment of all consecutive white space characters (with no exception for line feed characters).}}
{{CSS Property
|Initial value=collapse
|Applies to=All elements and generated content.
|Inherited=Yes
|Computed value=As specified (except for initial and inherit).
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=collapse
|Description=The white space characters are collapsed according to the rules described in [http://www.w3.org/TR/2003/CR-css3-text-20030514/#white-space-processing white space processing].
}}{{CSS Property Value
|Data Type=preserve
|Description=All white space characters are rendered as they are.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* preserve */
p.asis {
    all-space-treatment: preserve;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Text Module
|URL=http://www.w3.org/TR/2003/CR-css3-text-20030514
|Status=W3C Candidate Recommendation
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
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}