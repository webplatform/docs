{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines all the properties of an element's border in a single declaration. It can be used to set one or more values (of those: [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']], [[css/properties/border-color|'''border-color''']]).}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=border
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<width> <style> <color>
|Description=The <tt>border</tt> property is a shorthand property for setting the same width, color, and style for all four borders of a box.
* Width - Any of the range of width values available to the [[css/properties/border-width|'''border-width''']] property. Default value is <tt>medium</tt>.
* Style - Any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property. Default value is <tt>none</tt>.
* Color - Any of the range of color values available to the [[css/properties/border-color|'''border-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border''' attribute and the '''border''' property to specify the composite border properties.

This example uses a call to an embedded (global) style sheet to modify the '''border''' attribute.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    .applyBorder { border:0.2cm groove orange }
    .removeBorder { border:none }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt; 
    &lt;TD onmouseover{{=}}"this.className{{=}}'applyBorder'"
        onmouseout{{=}}"this.className{{=}}'removeBorder'"&gt;
    &lt;IMG src{{=}}"sphere.jpg"&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border_h.htm
}}{{Single Example
|Description=This example uses inline scripting to modify the '''border''' property.
|Code=&lt;TD onmouseover{{=}}"this.style.border{{=}}'0.2cm groove pink'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border''' property is a shorthand property that sets the '''width''', '''style''', and '''color''' values for all four sides of an object. All individual border properties, that are not set by the composite border property are set to their default values. 

The default value for the [[css/properties/border-color|'''border-color''']] is the same as the text color, for [[css/properties/border-width|'''border-width''']] is <tt>medium</tt> and for [[css/properties/border-style|'''border-style''']] is <tt>none</tt>. Therefor you must specify a style when specifying a width or color; otherwise, the border will be invisible.

By setting '''border''', all other border properties are set to their default values; e.g. the value of [[css/properties/border-image|'''border-image''']]  is reset to default value <tt>none</tt>.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=under revision by DougMay 2012-11-03
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0(1.9.2)
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}