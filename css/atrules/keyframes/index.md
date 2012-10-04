{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_At_Rule
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The version of this rule using a vendor prefix, '''@-ms-keyframes''', has been deprecated. To ensure compatibility in the future, applications using this rule with a vendor prefix should be updated accordingly.
This rule has no default value.
This rule is used to specify property values at various points during an animation. The '''@keyframes''' rule specifies the property values during one cycle of an animation; the animation may iterate one or more times.
This rule uses keyframe selectors to specify property values at various stages of the animation. Keyframe selectors can be declared as <code>from</code> (equivalent to <code>0%</code>), <code>to</code> (equivalent to <code>100%</code>), and one or more  percentages.
Keyframe selectors use keyframe descriptors to specify the properties and values being animated. If a property cannot be animated, the specification is ignored.
'''Important'''  Because of the preliminary status of the CSS Animations Module Level 3 Working Draft, the '''@keyframes''' rule must be used with the Microsoft-specific vendor prefix, "-ms-", to work with Internet Explorer 10 and Metro style apps using JavaScript.
|Import_Notes=
===Syntax===
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
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/properties/animation-name|animationName]]</code>
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}