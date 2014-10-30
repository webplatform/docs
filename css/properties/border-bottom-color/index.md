{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
Shorten the article. The various ways of color encoding needn't be included in the example, as they are not specific to border-bottom-color. The link to the color article is sufficient.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the color of the bottom border. This page explains the border-bottom-color value, but often you will find it more convenient to fix the border's bottom color as part of a shorthand set, either [[css/properties/border-bottom|border-bottom]] or [[css/properties/border-color|border-color]].

[[css/data_types/color|Colors]] can be defined several ways. For more information, see [[css/properties/border-bottom-color#Usage|Usage]].
}}
{{CSS Property
|Initial value=color - The value of the 'color' property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=when taken from the 'color' property, the computed value of 'color'; otherwise, as specified
|Animatable=Yes
|CSS object model property=borderTopColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<color>
|Description=The computed value of the ‘color’ property. This value can be a basic color keyword, such as red or lavenderblush, a numerical value, an RGB or RGBA value, or an HSL or HSLA value. For more information, see [[css/properties/border-bottom-color#Usage|Usage]].
}}{{CSS Property Value
|Data Type=inherit
|Description=currentColor, the color value inherited from parent object.
}}{{CSS Property Value
|Data Type=currentColor
|Description=The same as ‘color: inherit’, the color value inherited from parent object.
}}{{CSS Property Value
|Data Type=transparent
|Description=Fully transparent. This keyword can be considered a shorthand for transparent black, rgba(0,0,0,0), which is its computed value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example demonstrates the use of <code>border-bottom-color</code> by creating a set of 7 boxes with the rainbow colors, each box using a different way of color code representation. (Some style rules omitted for brevity.)
|Code=.box {
  border: 5px solid #efefef;
}

.named-value {
  border-bottom-color: red;
}

.hex-value {
  border-bottom-color: #FD6C02;
}

.rgb-value {
  border-bottom-color: rgb(255, 255, 0);
}

.rgb-percentage-value {
  border-bottom-color: rgb(0%, 100%, 0%);
}

.hsl-value {
  border-bottom-color: hsl(240, 100%, 50%);
}

.rgba-value {
  border-bottom-color: rgba(75, 0, 130, 0.8);
}

.hsla-value {
  border-bottom-color: hsla(282, 100%, 41%, 0.8);
}
|LiveURL=http://code.webplatform.org/gist/5535432
}}{{Single Example
|Language=HTML
|Description=
|Code=&lt;div class="box named-value"&gt;
  &lt;h1&gt;Named color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;red&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box hex-value"&gt;
  &lt;h1&gt;Hexadecimal color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;#FD6C02&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box rgb-value"&gt;
  &lt;h1&gt;RGB color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;rgb(255, 255, 0)&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box rgb-percentage-value"&gt;
  &lt;h1&gt;RGB percentage color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;rgb(0%, 100%, 0%)&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box hsl-value"&gt;
  &lt;h1&gt;HSL color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;hsl(240, 100%, 50%)&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box rgba-value"&gt;
  &lt;h1&gt;RGB with alpha color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;rgba(75, 0, 130, 0.8)&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;

&lt;div class="box hsla-value"&gt;
  &lt;h1&gt;HSL with alpha color&lt;/h1&gt;
  &lt;p&gt;&lt;code&gt;hsla(282, 100%, 41%, 0.8)&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The color value can be a property keyword, an extended keyword, or a numerical value. The two property keywords are currentColor and transparent. currentColor is the ‘color’ property value from the parent object. transparent is shorthand for transparent black, rgba(0,0,0,0).

The color value can also be a numerical value, such as one of the following:

* a basic color keyword, such as "red"
* a hex value, such as #ff0000
* an red-green-blue (RGB) value, such as rgb(255,0,0)
* an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
* a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
* HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [http://www.w3.org/TR/css3-color/#svg-color CSS Color Module Level 3 spec], which is the consolidation of various specifications.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Backgrounds and Borders Module
|URL=http://www.w3.org/TR/css3-background/#the-border-color
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/box.html#border-color-properties
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Level 3 - Color Module
|URL=http://www.w3.org/TR/css3-color
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultsSelected]]</code>
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}