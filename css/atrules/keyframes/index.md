{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=/* defining the animation */
@keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-moz-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-ms-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-webkit-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-o-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

/* applying the animation */
div {
    animation: fadeInAnimation linear;
    -moz-animation: fadeInAnimation linear;
    -ms-animation: fadeInAnimation linear;
    -webkit-animation: fadeInAnimation linear;
    -o-animation: fadeInAnimation linear;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The version of this rule using a vendor prefix, '''@-ms-keyframes''', has been deprecated. To ensure compatibility in the future, applications using this rule with a vendor prefix should be updated accordingly.
This rule has no default value.
This rule is used to specify property values at various points during an animation. The '''@keyframes''' rule specifies the property values during one cycle of an animation; the animation may iterate one or more times.
This rule uses keyframe selectors to specify property values at various stages of the animation. Keyframe selectors can be declared as <code>from</code> (equivalent to <code>0%</code>), <code>to</code> (equivalent to <code>100%</code>), and one or more  percentages.
Keyframe selectors use keyframe descriptors to specify the properties and values being animated. If a property cannot be animated, the specification is ignored.
'''Important'''  Because of the preliminary status of the CSS Animations Module Level 3 Working Draft, the '''@keyframes''' rule must be used with the Microsoft-specific vendor prefix, "-ms-", to work with Internet Explorer 10 and Metro style apps using JavaScript.
|Import_Notes====Syntax===
<code>'''@keyframes '''''
&lt;identifier&gt;
'' { ''
&lt;keyframes_blocks&gt;
'' };</code>
===Parameters===
;''identifier'':The name of the animation.
;''keyframes_blocks'':A set of keyframes blocks, each of which is composed of keyframe selectors.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Syntax
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/animation-name|animationName]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}