{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the color of an element's top border. This page explains the border-top-color value, but often you will find it more convenient to fix the border's top color as part of a shorthand set, either [[css/properties/border-top|border-top]] or [[css/properties/border-color|border-color]].

[[css/units/color|Colors]] can be defined several ways. For more information, see [[css/properties/border-top-color#Usage|Usage]].
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
|Data Type=inherit
|Description=currentColor, the color value inherited from parent object.
}}{{CSS Property Value
|Data Type=currentColor
|Description=The same as ‘color: inherit’, the color value inherited from parent object.
}}{{CSS Property Value
|Data Type=transparent
|Description=Fully transparent. This keyword can be considered a shorthand for transparent black, rgba(0,0,0,0), which is its computed value.
}}{{CSS Property Value
|Data Type=color
|Description=The computed value of the ‘color’ property. This value can be a basic color keyword, such as red or lavenderblush, a numerical value, an RGB or RGBA value, or an HSL or HSLA value. For more information, see [[css/properties/border-top-color#Usage|Usage]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the '''border-top-color''' attribute and the '''border-top-color''' property to specify the color of the top border.

This example uses a call to an embedded (global) style sheet to change the color of the top border to <code>blue</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-top-color: red;
        border-width: 0.5cm; border-style: groove }
    .blue { border-top-color: blue }  
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onmouseover{{=}}"this.className{{=}}'blue'"
        onmouseout{{=}}"this.className{{=}}''"&gt;
    &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-top-color.htm
}}{{Single Example
|Language=HTML
|Description=This example uses inline scripting to change the color of the top border to <code>blue</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;TD onmouseover{{=}}"this.style.borderWidth{{=}}'0.5cm';
    this.style.borderTopColor{{=}}'blue'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderTopColor.htm
}}{{Single Example
|Language=CSS
|Description=The following example demonstrates the use of <code>border-top-color</code> by creating a set of 7 boxes with the rainbow colors, each box using a different way of color code representation. (Some style rules omitted for brevity.)
|Code=.box {
  border: 5px solid #efefef;
}

.named-value {
  border-top-color: red;
}

.hex-value {
  border-top-color: #FD6C02;
}

.rgb-value {
  border-top-color: rgb(255, 255, 0);
}

.rgb-percentage-value {
  border-top-color: rgb(0%, 100%, 0%);
}

.hsl-value {
  border-top-color: hsl(240, 100%, 50%);
}

.rgba-value {
  border-top-color: rgba(75, 0, 130, 0.8);
}

.hsla-value {
  border-top-color: hsla(282, 100%, 41%, 0.8);
}
|LiveURL=http://code.webplatform.org/gist/5535354
}}{{Single Example
|Language=HTML
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
}}
}}
{{Notes_Section
|Usage=The color value can be a property keyword, an extended keyword, or a numerical value. The two property keywords are currentColor and transparent. currentColor is the ‘color’ property value from the parent object. transparent is shorthand for transparent black, rgba(0,0,0,0).

The color value can also be a numerical value, such as one of the following:

* a basic color keyword, such as "red"
* a numerical value, such as #ff0000
* an red-green-blue (RGB) value, such as rgb(255,0,0)
* an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
* a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
* HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [http://www.w3.org/TR/css3-color/#svg-color|CSS Color Module Level 3 spec], which is the consolidation of various specifications.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3, 4.1. Line Colors: the ‘border-color’ properties
|URL=http://www.w3.org/TR/css3-background/#the-border-color
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification, 8 Box model
|URL=http://www.w3.org/TR/CSS2/box.html#border-color-properties
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSSOM, 6.5.1 The CSSStyleDeclaration Interface,
|URL=http://www.w3.org/TR/cssom/#the-cssstyledeclaration-interface
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS Color Module Level 3
|URL=http://www.w3.org/TR/css3-color
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Microsoft Internet Explorer
|Version=5.5
|Note=This property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}{{Compatibility Notes Row}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections=*<code>[[css/properties/border-top|border-top]]</code>
*<code>[[css/properties/border-color|border-color]]</code>
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