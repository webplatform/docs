{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the color of an element's right border.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=color
|Description=A '''Variant''' that specifies or receives one of the color names or RGB values in the Color Table.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-right-color''' attribute and the '''border-right-color''' property to specify the color of the right border.

This example uses a call to an embedded (global) style sheet to change the color of the right border from <code>red</code> to <code>blue</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-right-color: red;
        border-width: 0.5cm; border-style: groove}
    .blue { border-right-color: blue }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onmouseover{{=}}"this.className{{=}}'blue'"
        onmouseout{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-right-color.htm
}}{{Single Example
|Description=This example uses inline scripting to change the color of the right border to <code>blue</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;TD onmouseover{{=}}"this.style.borderWidth{{=}}'0.5cm';
    this.style.borderRightColor{{=}}'blue';"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderRightColor.htm
}}{{Single Example
|Language=CSS
|Description=The following example demonstrates the use of <code>border-right-color</code> by creating a set of 7 boxes with the rainbow colors, each box using a different way of color code representation. (Some style rules omitted for brevity.)
|Code=.named-value {
  border-right-color: red;
}

.hex-value {
  border-right-color: #FD6C02;
}

.rgb-value {
  border-right-color: rgb(255, 255, 0);
}

.rgb-percentage-value {
  border-right-color: rgb(0%, 100%, 0%);
}

.hsl-value {
  border-right-color: hsl(240, 100%, 50%);
}

.rgba-value {
  border-right-color: rgba(75, 0, 130, 0.8);
}

.hsla-value {
  border-right-color: hsla(282, 100%, 41%, 0.8);
}
|LiveURL=http://dabblet.com/gist/5530809
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
|Notes====Remarks===
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Some browsers do not recognize color names, but all browsers should recognize RGB color values and display them correctly.
|Import_Notes====Syntax===
<code>'''border-right-color: '''''
&lt;color&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 8.5.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
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