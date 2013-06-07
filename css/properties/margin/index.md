{{Page_Title|margin}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>margin</code> property is shorthand to allow you to set all four margins of an element at once. Its equivalent longhand properties are <code>margin-top</code>, <code>margin-right</code>, <code>margin-bottom</code> and <code>margin-left</code>. Negative values are also allowed.}}
{{CSS Property
|Initial value=Depends on the particular element. Different elements have different default margins.
|Applies to=All elements except elements with table display types other than table-caption, table, and inline-table
|Inherited=No
|Media=visual
|Computed value=As specified, but with relative lengths converted into absolute pixel values.
|Animatable=Yes
|CSS object model property=margin
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed length, using any standard  [http://docs.webplatform.org/wiki/css/units/length CSS length units] . Negative Values are allowed.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage relative to the width of the containing block. Negative values are allowed.
}}{{CSS Property Value
|Data Type=auto
|Description=<code>auto</code> is replaced by some suitable value by the browser. For example, it can be used for centering of blocks.

<code>div { width:50%;  margin:0 auto; }</code> centers the <code>&lt;div&gt;</code> container horizontally.
}}{{CSS Property Value
|Data Type=inherit
|Description=Causes the element it is applied to to take on the same margin values as its parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing different combinations of margin values applied to three identically sized elements.
* The first one has a margin of 50 pixels on all sides.
* The second one has no margin on the top and bottom, but <code>auto</code> set on the left and right, causing it to center in the parent container.
* The third one has four individual values, including a negative top margin, causing it to move up, above the level of the second container, and a large left margin, causing it to be shunted over to the right.
|Code=&lt;div class="one"&gt;&lt;/div&gt;
&lt;div class="two"&gt;&lt;/div&gt;
&lt;div class="three"&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5727296
}}{{Single Example
|Language=CSS
|Description=The CSS applied to the above HTML.
|Code=/**
 * margin examples
 */
 
 * {
   margin: 0;
 }

div {
  width: 200px;
  height: 100px;
  background: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0));
  border-radius: 10px;
}

.one {
  background-color: red;
  margin: 50px
}

.two {
  background-color: blue;
  margin: 0px auto;
}

.three {
  background-color: green;
  margin: -11em 0px 0px 210px;
}
|LiveURL=http://code.webplatform.org/gist/5727296
}}
}}
{{Notes_Section
|Usage=* <code>margin</code> can take 1-4 values for its value, including CSS length units, percentage values, or the keywords '''auto''' or '''inherit''':
** If one value is given, it applies to all four sides.
** If two values are given, the first applies to the top and bottom, the second applies to the right and left.
** If three values are given, the first applies to the top, the second applies to the right and left sides, and the third applies to the bottom.
** If four values are given, they are applied in clockwise order, starting from the top (top, right, bottom, left).
* Negative margins are supported except for top and bottom margins on inline objects.
* When two margins collide, for example when one block level element has a bottom margin set, immediately followed by another block level element with a top margin, the larger of the two margins remains, and the smaller one collapses and disappears.
* Margins are always transparent.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 (Section 8.3)
|URL=http://www.w3.org/TR/CSS2/box.html#margin-properties
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=All
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=All
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=All
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=All
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=All
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=All
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=All
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=All
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=All
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=All
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=All
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=All
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=All
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
*<code>Conceptual</code>
*<code>CSS Values and Units Reference</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}