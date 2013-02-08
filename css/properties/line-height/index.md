{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|On inline elements, the line-height CSS property specifies the height that is used in the calculation of the line box height.
On block level elements, line-height specifies the minimal height of line boxes within the element.
}}
{{CSS Property
|Initial value=normal
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=for <length> and <percentage> the absolute value; otherwise as specified
|Animatable=No
|CSS percentages=refer to the font size of the element itself
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Default height. Depends on the user agent.
}}{{CSS Property Value
|Data Type=<number>
|Description=The used value of the property is this number multiplied by the element's font size. Negative values are illegal.
}}{{CSS Property Value
|Data Type=<length>
|Description=The specified length is used in the calculation of the line box height. Negative values are illegal. Note that the <length> CSS data type denotes distance measurements: a number immediately followed by a length unit - <code>px</code>, <code>em</code>, <code>pc</code>, <code>in, <code>mm</code>.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The computed value of the property is this percentage multiplied by the element's computed font size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''line-height''' attribute and the '''line-height''' property to control the height of paragraph lines.

This example uses '''p''' and '''blockquote''' as selectors in an embedded (global) style sheet to change the distance between the lines in all '''p''' and '''blockquote''' objects.
|Code=&lt;STYLE&gt;
    P { line-height:8mm}
    BLOCKQUOTE { line-height:4mm }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/line-height.htm
}}{{Single Example
|Description=This example uses inline scripting to set the distance between lines when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;DIV STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.lineHeight{{=}}'6mm'"&gt;
:
&lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/lineHeight.htm
}}{{Single Example
|Language=Other
|Description=You can get unexpected results when using a <length> value for <line-height>. This is why it is best to use unitless values.

Here is a example of what can happen when using <lenght>:

[[File:lineheight-1.png]]
|Code=&lt;style>
       .red   { font-size: 15px;  line-height: 1.1em;  border: solid red; }
      h1     { font-size: 30px; }
      div    { width: 19em;  display: inline-block; }
&lt;/style&gt

&lt;div class="red"&gt
 &lt;h1&gtAvoid unexpected results by using unitless line-height&lt;/h1&gt
  em values and percentage line-heights have poor inheritance ...
&lt;/div&gt
|LiveURL=https://developer.mozilla.org/en-US/docs/CSS/line-height#Avoid_unexpected_results.2C_use_unitless_line-height!
}}{{Single Example
|Language=Other
|Description=Here is an example of how you can re-write the same code to avoid this trap. Notice that <line-height> value is set to 1.1 instead of 1.1em in .green CSS class.

[[File:lineheight-2.png]]
|Code=&lt;style&gt
       .green   { font-size: 15px;  line-height: 1.1;  border: solid limegreen; }
      h1     { font-size: 30px; }
      div    { width: 19em;  display: inline-block; }
&lt;/style&gt

&lt;div class="green"&gt
 &lt;h1>Avoid unexpected results by using unitless line-height&lt;/h1&gt
 em values and percentage line-heights have poor inheritance ...
&lt;/div&gt
|LiveURL=https://developer.mozilla.org/en-US/docs/CSS/line-height#Avoid_unexpected_results.2C_use_unitless_line-height!
}}
}}
{{Notes_Section
|Notes====Remarks===
Line height is the distance between the descender of the font and the top of the internal leading of the font.
If a formatted line contains more than one object, the maximum line height applies. In this case, negative values are not allowed.
Microsoft Internet Explorer 3.0 supports the '''line-height''' attribute through the [[css/properties/font|'''font''']] attribute.
|Import_Notes====Syntax===
<code>'''line-height: '''normal '''{{!}}''' <number> '''{{!}}''' <length> '''{{!}}''' <percentage></code>
===Standards information===
*[http://dev.w3.org/csswg/css3-transitions/#animatable-css CSS Transitions] Defines <code>line-height</code> as animatable. The status of this document is Working Draft.
*[http://www.w3.org/TR/CSS2/visudet.html#propdef-line-height CSS 2.1]
*[http://www.w3.org/TR/CSS1/#line-height CSS 1] Initial definition.
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
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
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
|Firefox_mobile_version=1.0 (1)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/line-height
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}