{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example is an ID selector that demonstrates the use of both the '''transform'''
and the [[css/properties/transform-origin|'''transform-origin''']] properties. In this case, the '''transform-origin''' property
has been set to "60% 100%", which sets the transform's origin point to 60% of the length and 100% of the height of the element to be transformed.
The '''transform''' property first uses the '''translate''' function to move the element 200 pixels in the ''x'' direction
and 100 pixels in the ''y'' direction. It then uses the '''scale''' function to scale the element by 75%. Finally, it uses the '''rotate''' function to rotate the element 40 degrees clockwise around the
origin point set by the '''transform-origin''' property.
|LiveURL=
|Code=
#mytransform {
  transform: translate(200px, 100px) scale(.75, .75) rotate(40deg);
  transform-origin: 60% 100%;
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
The version of this property using a vendor prefix, '''-ms-transform''', has been deprecated in Internet Explorer 10 and later. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly. However, be aware that '''-ms-transform''' is the only form of this property that is recognized by Windows Internet Explorer 9, which supports 2-D Cascading Style Sheets (CSS) transforms.
3-D transforms are only supported in Internet Explorer 10 and later.
For information about the transformation functions that are supported for use with the '''transform''' property, see Transform Functions.
|Import_Notes=
===Syntax===
<code>'''transform: '''none '''{{!}}''' ''
&lt;transform-function&gt;
'' '''[''' ''
&lt;transform-function&gt;
'' ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/transform-origin|transform-origin]]</code>
|Topic_clusters=Transforms
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}