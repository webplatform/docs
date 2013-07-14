{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>text-align</code> CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements itself, only their inline content.}}
{{CSS Property
|Initial value=start, or a nameless value that acts as left if direction is ltr, right if direction is rtl, if start is not supported by the browser.
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Computed value=as specified, except for the match-parent value which is calculated against its parent's direction value and results in a computed value of either left or right
|Animatable=No
|CSS object model property=textAlign
|Values={{CSS Property Value
|Data Type=start
|Description=The same as ''<code>left</code>'' if direction is left-to-right and ''<code>right</code>'' if direction is right-to-left.
}}{{CSS Property Value
|Data Type=end
|Description=The same as ''<code>right</code>'' if direction is left-to-right and ''<code>left</code>'' if direction is right-to-left.
}}{{CSS Property Value
|Data Type=left
|Description=The inline contents are aligned to the left edge of the line box.
}}{{CSS Property Value
|Data Type=right
|Description=The inline contents are aligned to the right edge of the line box.
}}{{CSS Property Value
|Data Type=center
|Description=The inline contents are centered within the line box.
}}{{CSS Property Value
|Data Type=<string>
|Description=The first occurrence of the one-char string is the element used for alignment. the keyword that follows or precedes it indicates how it is aligned. This allows to align numeric values on the decimal point, for instance.
}}{{CSS Property Value
|Data Type=justify
|Description=The text is justified. Text should line up their left and right edges to the left and right content edges of the paragraph.
}}{{CSS Property Value
|Data Type=match-parent
|Description=Similar to inherit with the difference that the value ''<code>start</code>'' and ''<code>end</code>'' are calculated according the parent's direction and are replaced by the adequate ''<code>left</code>'' or ''<code>right</code>'' value.
}}{{CSS Property Value
|Data Type=start end
|Description=Specifies ''<code>start</code>'' alignment of the first line and any line immediately after a forced line break; and ''<code>end</code>'' alignment of any remaining lines not affected by [[css/properties/text-align-last|'''text-align-last''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This just shows the four possible types of text-alignment.
|Code=&lt;p class="left"&gt; This paragraph is aligned to the left. &lt;/p&gt;

&lt;p class="centered"&gt; This paragraph is centered. &lt;/p&gt;

&lt;p class="right"&gt; This paragraph is aligned to the right. &lt;/p&gt;

&lt;p class="justified"&gt;This paragraph needs to be really long in order to show how to justify text. It only works because we set a width for this paragraph though.&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5664679
}}{{Single Example
|Language=CSS
|Code=.left { text-align: left;}
.cenetered{ text-align: center;}
.right { text-align: right;}
.justified { width: 200px; text-align: justify;}
}}
}}
{{Notes_Section
|Notes=The standard-compatible way to center a block itself without centering its inline content is setting the left and right <code>margin</code> to auto, e.g.:
<code>margin:auto;</code> or <code>margin:0 auto;</code> or  <code>margin-left:auto; margin-right:auto;</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Level 3
|URL=http://dev.w3.org/csswg/css3-text/#text-align
|Status=Working Draft
|Relevant_changes=Added the <code>start</code> and <code>end</code> keyword. Changed the unnamed initial value to <code>start</code> (which it was). Added the <code><string></code> value, the <code>match-parent</code> value and the <code>start end</code> double value.
}}
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
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Yes
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Text
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/text-align
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ms531162(v=vs.85).aspx
|HTML5Rocks_link=
}}