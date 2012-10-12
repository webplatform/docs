{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic
|Content=Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Defines the line style of the border bottom of a box}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Border is not drawn, regardless of any [[css/properties/border-width|'''border-width''']].
}}{{CSS Property Value
|Data Type=dotted
|Description=Border is a dotted line.
}}{{CSS Property Value
|Data Type=dashed
|Description=Border is a dashed line. 
}}{{CSS Property Value
|Data Type=solid
|Description=Border is a solid line.
}}{{CSS Property Value
|Data Type=double
|Description=Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/border-width|'''border-width''']] value. The border width must be at least 3 pixels wide to draw a double border.
}}{{CSS Property Value
|Data Type=groove
|Description=3-D groove is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=ridge
|Description=3-D ridge is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=inset
|Description=3-D inset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=outset
|Description=3-D outset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=window-inset
|Description=Same as <code>inset</code> with a thin outside border.
}}{{CSS Property Value
|Data Type=hidden
|Description=Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example use the '''border-bottom-style''' property to specify the border style.

This example uses a call to an embedded style sheet to change the style of the bottom border to '''groove'''.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-bottom-style:solid;
        border-width:0.3cm }
    .change { border-bottom-style:groove}
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
  &lt;TD onmouseover{{=}}"this.className{{=}}'change'" 
      onmouseout{{=}}"this.className{{=}}''"&gt;
    &lt;IMG src{{=}}"sphere.jpg"&gt;
  &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-bottom-style.htm
}}
}}
{{Notes_Section
|Notes=An [[css/properties/border-width|'''border-width''']] greater than zero must be set for the '''border-bottom-style'''attribute to render.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/box.html#propdef-border-bottom-style
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=Mac < 4, Win < 5.5
|Note="dotted", "dashed" are supported on the Macintosh platform, as of Internet Explorer 4.01, and on the Windows platform, as of Internet Explorer 5.5. It renders as a solid line on UNIX platforms, and on Windows systems running earlier versions of Internet Explorer.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6+
|Note="window-inset" is supported from Internet Explorer 6 and later
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8+
|Note="hidden" supported as of Internet Explorer 8
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 5.5
|Note=As of Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}