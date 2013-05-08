{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''flex-flow''' CSS property defines the flex container's main and cross axis. It is a shorthand property for the [[css/properties/flex-direction|flex-direction]] and [[css/properties/flex-wrap|flex-wrap]] properties.}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=flex containers
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS object model property=flexFlow
|Values={{CSS Property Value
|Data Type=<flex-direction> <flex-wrap>
|Description=The shorthand value includes the values of the following properties: 
* [[css/properties/flex-direction|flex-direction]]
* [[css/properties/flex-wrap|flex-wrap]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children in a row wrapping to the next line.
|Code=.list {
  display: flex;
  flex-flow: row wrap;
}

.list div {
  flex: 1;
}
|LiveURL=http://code.webplatform.org/gist/4740728
}}{{Single Example
|Language=CSS
|Description=The Holy Grail Layout example.
|Code=-webkit-flex-flow: row;
    -moz-flex-flow: row;
            flex-flow: row;
|LiveURL=http://code.webplatform.org/gist/5506026
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#flex-flow-property
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=http://caniuse.com/#flexbox
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Flexbox
|External_links=Also, check out the following live demo sites:
* [http://demo.agektmr.com/flexbox/ Flexbox Playground]
* [http://the-echoplex.net/flexyboxes Flexy Boxes]
}}
{{Topics|Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}