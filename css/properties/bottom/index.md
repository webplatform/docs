{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the position of the bottom edge of an element.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Default position, according to the regular HTML layout of the page.
}}{{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). The value is a percentage of the height of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=We demonstrate the `bottom` property by positioning these elements.
|Code=.container {
  /**
   * Object is positioned according to the normal flow, and then offset.
   * @see http://docs.webplatform.org/wiki/css/properties/position
   */
  position: relative;
}

.absolutely-positioned-within-container {
  /**
   * Object is positioned relative to nearest positioned ancestor—or
   * to the initial containing block if no positioned ancestor exists.
   * Here, the nearest positioned ancestor is the `<div class="container">`.
   * @see .container (above)
   * @see http://docs.webplatform.org/wiki/css/properties/position
   */
  position: absolute;
  /**
   * Offsets this element 50px above the container's bottom edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  bottom: 50px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned anscestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `<body>`.
   */
  position: absolute;
  /**
   * Offsets this element 100px above the initial containing
   * block's bottom edge i.e. the `<body>`'s bottom edge.
   */
  bottom: 100px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   * @see http://docs.webplatform.org/wiki/css/properties/position
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 20px towards the left from where it would have been in
   * the normal flow.
   */
  bottom: 20px;
}

|LiveURL=http://code.webplatform.org/gist/6181867
}}{{Single Example
|Language=HTML
|Description=The HTML for the above style rules.
|Code=&lt;article&gt;
  &lt;h1&gt;&lt;code&gt;bottom&lt;/code&gt; example&lt;/h1&gt;
  &lt;p&gt;The following example demostrates the various uses of the &lt;code&gt;bottom&lt;/code&gt; property. Learn more about it at the &lt;a href="http://docs.webplatform.org/wiki/css/properties/bottom"&gt;&lt;code&gt;bottom&lt;/code&gt;&lt;/a&gt; CSS properties page on Web Platform Docs!&lt;/p&gt;
  &lt;div class="container"&gt;
    &lt;p class="box absolutely-positioned-within-container"&gt;Absolutely positioned within &lt;code&gt;div.container&lt;/code&gt; at 50px above the bottom edge.&lt;/p&gt;
    &lt;p class="box relatively-positioned"&gt;This is relatively positioned at 20px from the bottom.&lt;/p&gt;
  &lt;/div&gt;
  
  &lt;p class="box absolutely-positioned-within-body"&gt;This is absolutely positioned within the &lt;code&gt;body&lt;/code&gt; at 50px above the bottom edge.&lt;/p&gt;
&lt;/article&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''bottom''' attribute should be used only when the [[css/properties/position|'''position''']]
attribute is set; otherwise, the value of the '''bottom''' attribute is ignored.
Because the value of the '''bottom''' property is a string, the property cannot be used  in script to calculate the position of the object in the document; instead, the [[css/cssom/properties/pixelBottom|'''pixelBottom''']] property or the [[css/cssom/properties/posBottom|'''posBottom''']] property should be used.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) object model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
<code>'''bottom: '''length '''{{!}}''' percentage '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.3.2
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
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/properties/pixelTop|pixelTop]]</code>
*<code>[[css/cssom/properties/posTop|posTop]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}