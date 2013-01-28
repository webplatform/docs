{{Page_Title|Time units}}
{{Flags}}

{{API_Name}}
{{Summary_Section|Specify a duration}}
{{Concept_Page
|Content=

Specify either seconds ('''s''') or milliseconds ('''ms'''), which are
a thousandth of a second. Must be a numeric value greater than or
equal to zero.  Time values can be used to measure the duration of
animation effects.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.selected {
    background-color: #fff;
    transition-property: background-color;
    /* transition takes half a second to complete */
    transition-duration: 0.5s;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}