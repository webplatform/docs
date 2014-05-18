{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the position an element in relation to the right side of the containing element.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, 'auto'.
|Animatable=Yes
|CSS object model property=right
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Position is determined by the regular HTML layout of the page.
}}{{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=We demonstrate the `right` property by positioning the elements.
|Code=.container {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
}

.absolutely-positioned-within-container {
  /**
   * Object is positioned relative to nearest positioned ancestor—or
   * to the initial containing block if no positioned ancestor exists.
   * Here, the nearest positioned ancestor is the `div.container`.
   */
  position: absolute;
  /**
   * Offsets this element 50px to the left of the container's right edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  right: 50px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned anscestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `body`.
   */
  position: absolute;
  /**
   * Offsets this element 150px to the left of the initial containing
   * block's right edge i.e. the `body`'s right edge.
   */
  right: 150px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 30px towards the left from where it would have been in
   * the normal flow.
   */
  right: 30px;
}
|LiveURL=http://code.webplatform.org/gist/6181880
}}{{Single Example
|Language=HTML
|Description=The HTML for the above example.
|Code=<syntaxhighlight>
<article>
  <div class="container">
    <p class="box absolutely-positioned-within-container">Absolutely positioned within <code>div.container</code> at 50px left from the container's right edge.</p>
    <p class="box relatively-positioned">This is relatively positioned at 30px from the right.</p>
  </div>
  
  <p class="box absolutely-positioned-within-body">This is absolutely positioned within the <code>body</code> at 150px to the left of the body's right edge.</p>
</article>
</syntaxhighlight>
}}
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
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=5.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/right
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}