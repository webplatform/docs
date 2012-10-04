{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=font-style |Description=Any of the range of font-style values available to the [[css/properties/font-style|'''font-style''']] property.}}
{{CSS_Property_Value|Data Type=font-variant |Description=Any of the range of font-variant values available to the [[css/fonts/font-variant|'''font-variant''']] property.}}
{{CSS_Property_Value|Data Type=font-weight |Description=Any of the range of font-weight values available to the [[css/properties/font-weight|'''font-weight''']] property.}}
{{CSS_Property_Value|Data Type=font-size |Description=Any of the range of font-size values available to the [[css/properties/font-size|'''font-size''']] property. When this value is an integer followed by a percent (%), the value is a percentage of the parent object's font size.}}
{{CSS_Property_Value|Data Type=line-height |Description=Any of the range of line-height values available to the [[css/properties/line-height|'''line-height''']] property. When used with the '''font''' property, this attribute must include a slash (/) before the value. Line height percentage values are calculated as a percentage of the font size of the element itself, not of the parent.}}
{{CSS_Property_Value|Data Type=font-family |Description=Any of the range of font-family values available to the [[css/properties/font-family|'''font-family''']] property. This property can be set to multiple comma-separated values. Its default value depends on user settings.}}
{{CSS_Property_Value|Data Type=caption |Description=User-preference font used in objects that have captions—buttons, labels, and so on.}}
{{CSS_Property_Value|Data Type=icon |Description=User-preference font used in icon labels.}}
{{CSS_Property_Value|Data Type=menu |Description=User-preference font used in menus.}}
{{CSS_Property_Value|Data Type=message-box |Description=User-preference font used in dialog boxes.}}
{{CSS_Property_Value|Data Type=small-caption |Description=User-preference font used in small controls.}}
{{CSS_Property_Value|Data Type=status-bar |Description=User-preference font used in window status bars.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''font''' attribute and the '''font''' property to change font characteristics.

This example uses an inline style sheet to set the font attributes.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font_h.htm
|Code=
&lt;SPAN STYLE{{=}}"font:italic normal bolder 12pt Arial"&gt; 
: 
&lt;/SPAN&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the font properties.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font_s.htm
|Code=
&lt;DIV onmouseover{{=}}"this.style.font {{=}} 'italic small-caps bold 12pt serif'"&gt;
:
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This is a composite property that specifies up to six font values. The '''font-style''', 
'''font-variant''', and '''font-weight''' values may appear in any order before '''font-size'''. However, the '''font-size''', '''line-height''', and '''font-family''' properties must appear in the order listed. Setting the '''font''' property also sets the component properties. In this case, the string must be a combination of valid values for the component properties; only '''font-family''' may have more than one value. 
If the string does not contain a value for a component property, that property is set to its default, regardless of prior settings for that component property.
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, the following conditions apply to this property.
#The '''font-size''' and '''font-family''' values must be declared. If '''font-size''' and '''font-family''' are not declared, or are not in the correct order, the '''font''' property is ignored.
#All specified values must appear in the correct order. Otherwise, the '''font''' property is ignored.
#In standards-compliant mode, the default '''font-size''' is '''small''', not '''medium'''. If not explicitly set, '''font-size''' returns a point value.

For more information about standards-compliant parsing and the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration, see CSS Enhancements in Internet Explorer 6.
|Import_Notes=
===Syntax===
<code>'''font: ''''''[''' '''[''' font-style '''{{!}}{{!}}''' font-variant '''{{!}}{{!}}''' font-weight ''']''''''?''' font-size '''[''' / line-height ''']''''''?''' font-family ''']''' '''{{!}}''' caption '''{{!}}''' icon '''{{!}}''' menu '''{{!}}''' message-box '''{{!}}''' small-caption '''{{!}}''' status-bar</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Values and Units Reference</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}