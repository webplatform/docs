{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{CSS_Property
|Applies to=flexbox elements
|Media=visual
|Inherited=No
|Initial value=stretch
|Values={{CSS_Property_Value|Data Type=start |Description=If the parent element has a computed value for [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] of <code>row</code> or <code>column</code>, the leading edge (or baseline) of each child element is aligned with the leading edge of the object. Any remaining space, perpendicular to the layout axis, is placed after the trailing edge of each child element.

If the parent element has a computed value for [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] of <code>row-reverse</code> or <code>column-reverse</code>, the trailing edge (or baseline) of each child element is aligned with the trailing edge of the object. Any remaining space, perpendicular to the layout axis, is placed before the leading edge of each child element.}}
{{CSS_Property_Value|Data Type=end |Description=If the parent element has a computed value for [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] of <code>row</code> or <code>column</code>, the trailing edge of each child element is aligned with the trailing edge of the object. Any remaining space, perpendicular to the layout axis, is placed before the leading edge of each child element.

If the parent element has a computed value for [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] of <code>row-reverse</code> or <code>column-reverse</code>, the leading edge of each child element is aligned with the leading edge of the object. Any remaining space, perpendicular to the layout axis, is placed after the trailing edge of each child element.}}
{{CSS_Property_Value|Data Type=center |Description=Each child element is centered between the leading and trailing edges of the object. Any remaining space, perpendicular to the layout axis, is evenly distributed before and after each child.}}
{{CSS_Property_Value|Data Type=stretch |Description=Initial value. Each child element is stretched to completely fill the space that is available perpendicular to the layout axis. If set, the [[css/properties/max-width|'''max-width''']] or [[css/properties/max-height|'''max-height''']] property for a child element takes precedence and layout follows the  <code>start</code> rule.}}
{{CSS_Property_Value|Data Type=baseline |Description=The baselines (leading edge or trailing edge depending on the [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] property)  of all child elements are aligned with each other. 

The child element that occupies the most space, perpendicular to the layout axis, follows the <code>start</code> rule; the baselines of all remaining elements are then aligned with the baseline of this element.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''-ms-flex-align: '''start '''{{!}}''' end '''{{!}}''' center '''{{!}}''' baseline '''{{!}}''' stretch</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 8.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
|Topic_clusters=Flexbox
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}