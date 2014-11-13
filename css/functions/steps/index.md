{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|A timing function that specifies a progression of discrete intervals over the course of a transition or animation keyframe.}}
{{CSS_Function
|Content=The function's mandatory first argument specifies the number of discrete, equal steps in the progression.  An optional second argument accepts keywords '''start''' or '''end''' (the default), specifying whether the change should take place at the beginning or end of each new step.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Apply an un-smoothed ratchet effect to any font-size transitions:
|Code=p {
    transition: font-size 1s;
    transition-timing-function: steps(5);
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transitions
|URL=http://www.w3.org/TR/2013/WD-css3-transitions-20131119/
|Status=Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}