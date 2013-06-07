{{Page_Title|Text values}}
{{Flags}}
{{API_Name}}
{{Summary_Section|Specify strings, identifiers, keywords, and functions}}
{{Concept_Page
|Content=Properties accept string values in various ways:

* A literal ''string'' value to display on the web page. Literal strings need to be single- or double-quoted. Single quotes nested within double-quoted strings are interpreted literally, and vice versa.

* An ''identifier'' referring to an object defined elsewhere, such as a [[tutorials/css_animation|keyframe animation]] or a [[tutorials/css-regions|named flow]].

* A ''keyword'' value recognized by individual CSS properties. For example, the [[css/properties/text-align|'''text-align''']] property recognizes '''justify''' as a valid value. (All CSS properties accept the built-in '''inherit''' value for the parent element's value, and '''initial''' for the default value.)

* A ''function'' accepts strings and measurements as values. For example, the [[css/functions/url|'''url()''']] function specifies a path to a file or web page.  See [[css/data_types/color|color units]] for information about various '''rgba()''' and '''hsla()''' functions, otherwise see [[css/functions|CSS functions]] for others.
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