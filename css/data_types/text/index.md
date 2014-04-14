{{Page_Title|Text values in CSS properties}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Various CSS data types are expressed using character text, however the meaning and syntax of each type differs.}}
{{Concept_Page
|Content=Text-like [[css/data_types|CSS data-types]] include:

* [[css/data_types/string|<code>&lt;string></code>s]]

* [[css/data_types/custom_ident|<code>&lt;custom-ident></code> (custom identifier) values]]

* [[css/data_types/keyword|keywords]]

In addition, various [[css/functions| CSS functions]] can be used to generate values of these or other data types.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=a[href$=".pdf"]::after {
    /* literal string marks links to PDF files */
    content: " (PDF)";
}
}}{{Single Example
|Language=CSS
|Code=.pulse {
    /* identifier for keyframe animation defined below */
    animation-name: pulse
    animation-duration: 1s;
    /* property values are built-in keywords */
    animation-direction: alternate;
    animation-iteration-count: infinite;
    /* The url() function accepts a string value */
    background-image: url(img/icon.png);
}

/* "pulse" is referenced above by animation-name property */
@keyframes pulse {
    from { opacity: 1   }
    to   { opacity: 0.5 }
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