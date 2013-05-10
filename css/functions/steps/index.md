{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status}}
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
}}{{Single Example
|Language=Other
|Description=Modify the timing function for a sequence of two transitions                                                                    
|LiveURL=http://letmespellitoutforyou.com/samples/transit_timing.html
}}
}}
{{Notes_Section}}
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
{{See_Also_Section
|Topic_clusters=Animation, Transistions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}