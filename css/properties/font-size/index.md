{{Page_Title|font-size}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|<code>font-size</code> sets the font size of the text inside the element to which it is applied, and that of its descendants. You can size text using absolute measurements, or measurements relative to the affected element's parent or root elements. [[guides/css_text_styling_fundamentals|CSS Text Styling Fundamentals]] provides an overview.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified, but with relative lengths converted into absolute pixel values. 
|Animatable=Yes
|CSS object model property=fontSize
|Values={{CSS Property Value
|Data Type=absolute keywords
|Description=A set of keywords indicating predefined font sizes that scale according to font setting preferences or each browser's default values. From small to large, possible values are '''xx-small''', '''x-small''', '''small''', '''medium''', '''large''', '''x-large''', and '''xx-large'''.
}}{{CSS Property Value
|Data Type=relative keywords
|Description=A set of keywords interpreted relative to the parent element's '''font-size''' — either '''smaller''' or '''larger'''.
}}{{CSS Property Value
|Data Type=length
|Description=An absolute or relative unit value: any of the standard [[css/data_types/length|css length units]] are allowed.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage value, indicating a percentage of the parent element's '''font-size'''.
}}{{CSS Property Value
|Data Type=inherit
|Description=the <code>inherit</code> keyword causes the element to adopt its parent element's font size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A selection of examples showing some typical uses of the font-size property.
|Code=&lt;p class="example-one"&gt;Example One: We ♥ WebPlatform Docs!&lt;/p&gt;
&lt;p class="example-two"&gt;Example Two: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis, eos, dicta nihil aliquid quia dolores labore nesciunt unde consectetur blanditiis ex eius consequatur qui incidunt voluptatem inventore fugit quos amet!&lt;/p&gt;
&lt;p class="example-three"&gt;Example Three: Eius, earum unde eum distinctio ex accusamus rem eligendi optio mollitia deleniti? Iure, accusamus, fuga ipsa quas doloremque enim velit sed est earum pariatur ab optio quia molestiae repellendus non.&lt;/p&gt;
}}{{Single Example
|Language=CSS
|Code=.example-one {
	font-size: 1.2em;
}		

.example-two {
	font-size: small;
}

.example-three {
	font-size: 28px;
}
|LiveURL=http://code.webplatform.org/gist/5628042
}}{{Single Example
|Language=CSS
|Description=A redefinition of the typical '''16px''' browser default font size '''medium''' value as '''10px''', followed by a resizing of the text that follows proportionate to that.
|Code=html { font-size: 62.5%; } 
/* 
16 * 62.5% == 10 
*/

.example-one { font-size: 3.6rem }   /* 36px */
.example-two { font-size: 2.4rem }   /* 24px */
.example-three  { font-size: 1.4rem }   /* 14px */
|LiveURL=http://code.webplatform.org/gist/5628240
}}
}}
{{Notes_Section
|Usage=Keywords such as '''large''' and '''medium''', or relative '''em''' or percentage units, are generally safer to use than pixel measurements, especially for mobile web browsers that adjust their set of default font sizes for legibility. Otherwise, pixels offer the safest way to specify measurements, since [[css/concepts/CSS_pixels|CSS pixels]] are adjusted for variations in display pixel density.

While the initial '''medium''' size applies widely, browsers apply a default style sheet that modifies it for various semantic elements, boosting the size of headings, for example. Browsers also automatically resize fonts when zooming the page, stepping by values that may not correspond exactly to the zoom factor. Unless disabled using [[css/properties/text-size-adjust|'''text-size-adjust''']], fonts also resize when tipping between portrait and landscape orientations on mobile browsers. For an overview of the issue, see [[tutorials/mobile_viewport|The Mobile Viewport and Orientation]].

The value of '''font-size''' also affects the value of [[css/properties/line-height|'''line-height''']] when using its default or relative measurements.

Along with many other CSS properties, '''font-size''' can also be applied directly as an SVG attribute:

<syntaxhighlight lang="xml">
<text x="12px" y="12px" font-family="sans-serif" font-size="120%"/>
</syntaxhighlight>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#font-size-prop
|Status=Working Draft
}}{{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}{{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification
|URL=http://www.w3.org/TR/CSS2/
|Status=W3C Recommendation
}}
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
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=1.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=IE
|Version=≤ 6.0
|Note=Requires a [[html/elements/!DOCTYPE|'''!DOCTYPE''']] declaration that triggers [[concepts/standards_mode|standards mode]], otherwise the initial value is '''small''' rather than '''medium'''.
}}{{Compatibility Notes Row
|Browser=IE
|Version=≤ 7.0
|Note=Does not support '''inherit''' as a value.
}}{{Compatibility Notes Row
|Browser=IE
|Version=≤ 8.0
|Note=Does not resize text specified with absolute pixel measurements when using the browser's ''text-resize'' feature, but does resize correctly when zooming the page.
}}{{Compatibility Notes Row
|Browser=IE
|Version=≤ 8.0
|Note=Does not support [[css/data_types/length|'''rem''']] values; specify other supported values as fallback properties.
}}{{Compatibility Notes Row
|Browser=All
|Note=Check compatibility for more recent [[css/data_types/length|viewport unit values]].
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts, Text
|Manual_links=* [[guides/css_text_styling_fundamentals|CSS text styling fundamentals]]
|External_links=* Smashing: [http://www.smashingmagazine.com/2011/10/07/16-pixels-body-copy-anything-less-costly-mistake 16 Pixels: For Body Copy. Anything Less Is a Costly Mistake]
* HTML5 Boilerplate: [https://github.com/h5bp/html5-boilerplate/issues/724 Reasoning behind default font-size and line-height]
* A List Apart: [http://www.alistapart.com/articles/howtosizetextincss How to Size Text in CSS]
* Mozilla: [http://mxr.mozilla.org/mozilla/source/layout/style/html.css default style sheet]
* WebKit: [http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css default style sheet]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}