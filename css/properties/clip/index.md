{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
|Editorial notes=Deprecated; replaced by clip-path.
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|'''Deprecated; see [[css/properties/clip-path|clip-path]].'''

Lets you specify the dimensions of an absolutely positioned element that should be visible, and the element is clipped into this shape, and displayed.
}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Clip to expose entire object.
}}{{CSS Property Value
|Data Type=rect(top, right, bottom, left)
|Description=Top, right, bottom, and left specify length values, any of which can be replaced by '''auto''', leaving that side not clipped. The value of top specifies that everything above this value on the Y axis (with 0 at the top) is clipped. The value of right specifies that everything above this value on the X axis (with 0 at the left) is clipped. The value of bottom specifies that everything below this value on the Y axis (with 0 at the top) is clipped. The value of left specifies that everything to the left of this value on the X axis (with 0 at the left) is clipped.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This example takes the Web Platform Docs logo and clips it in two ways: one shows the icon and the other shows the text.
|Code=img.clippable {
  /**
   * The `clip` property applies only to absolutely positioned elements only.
   * @see http://www.w3.org/TR/css-masking/#clip-property
   */
  position: absolute;
  top: 100px;
}

img.clipped-icon {
  left: 215px;
  /**
   * The rectangle clips the image leaving only the icon visible.
   * For Internet Explorer 4-7, use `clip: rect(10px 68px 63px 3px);`
   */
  clip: rect(10px, 68px, 63px, 3px);
}

img.clipped-text {
  left: 300px;
  /**
   * The rectangle clips the image leaving only the text visible.
   * For Internet Explorer 4-7, use `clip: rect(10px 190px 63px 53px);`
   */
  clip: rect(10px, 190px, 63px, 53px);
}
|LiveURL=http://code.webplatform.org/gist/6338197
}}{{Single Example
|Language=HTML
|Description=The HTML for the above example.
|Code=<syntaxhighlight>
  <img class="clippable original" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo" />
  <img class="clippable clipped-icon" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (icon only)" title="Web Platform Docs logo (icon only)" />
  <img class="clippable clipped-text" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (text only)" title="Web Platform Docs logo (text only)" />
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Windows Internet Explorer 8, the required syntax of the '''clip''' attribute is identical to that specified in the Cascading Style Sheets, Level 2 Revision 1 (CSS2.1) specification; that is, commas are now required between the parameters of the <code>rect()</code> value. This behavior requires Windows Internet Explorer to be in IE8 Standards mode (or EmulateIE8 mode with an Internet Explorer 8 [[html/elements/!DOCTYPE|!DOCTYPE]] directive). For more information on document compatibility modes, see Defining Document Compatibility.
In Windows Internet Explorer 7 and earlier (and in Internet Explorer 8 or later in IE7 Standards mode, EmulateIE7 mode, or IE5 (Quirks) mode), the commas should be omitted. For example: '''clip''':<code>rect(0 50 50 0)</code>
The required syntax of the '''clip''' attribute is identical to that specified in the CSS2.1 specification; that is, commas are now required between the parameters of the <code>rect()</code> value.
This property defines the shape and size of the positioned object that is visible. The [[css/properties/position|'''position''']] must be set to '''absolute'''. Any part of the object that is outside the clipping region is transparent. Any coordinate can be replaced by the value '''auto''', which exposes the respective side (that is, the side is not clipped).
The order of the values '''clip''':<code>rect(0, 0, 50, 50)</code> renders the object invisible because it sets the top and right positions of the clipping region to 0. To achieve a 50-by-50 view port, use '''clip''':<code>rect(0, 50, 50, 0)</code>.
The '''clip''' attribute and the '''clip''' property are available on the Macintosh platform, as of Microsoft Internet Explorer 5.
|Import_Notes====Syntax===
<code>'''clip: '''auto '''{{!}}''' rect(top, right, bottom, left)</code>
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
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/properties/clipBottom|clipBottom]]</code>
*<code>[[css/cssom/properties/clipLeft|clipLeft]]</code>
*<code>[[css/cssom/properties/clipRight|clipRight]]</code>
*<code>[[css/cssom/properties/clipTop|clipTop]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}