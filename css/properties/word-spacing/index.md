{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Remove topic cluster flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>word-spacing</code> CSS property specifies the spacing behavior between "words".}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=an optimum, minimum, and maximum value, each consisting of either an absolute length, a percentage, or the keyword ‘normal’
|Animatable=No
|CSS object model property=wordSpacing
|CSS percentages=refers to width of the affected glyph
|Values={{CSS Property Value
|Data Type=normal
|Description=The spacing is the normal spacing for the current font.
}}{{CSS Property Value
|Data Type=length
|Description=Indicates inter-word space in addition to the default space between words, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). Values may be negative, but there may be implementation-specific limits.
}}{{CSS Property Value
|Data Type=percentage
|Description=Specifies the additional spacing as a percentage of the affected word's advance measure.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''word-spacing''' attribute and the '''word-spacing''' property to increase the amount of space between words in a <code>p</code> element.
|Code=&lt;p&gt;This is a simple paragraph with the default value for word-spacing.&lt;/p&gt;

&lt;p class="pos"&gt;This is a simple paragraph with a altered word-spacing value by 0.3em.&lt;/p&gt;

&lt;p class="neg"&gt;This is a simple paragraph withe a altered word-spacing value by -0.1em&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5671391
}}{{Single Example
|Language=CSS
|Code=p {
    word-spacing: normal;
}

p.pos {
    word-spacing: .3em;
}

p.neg {
    word-spacing: -.1em;
}
}}
}}
{{Notes_Section
|Usage=* Up to three different values can be specified, in the following order: optimum, minimum, maximum
* If one value is specified, it is used for all spacing. If two values are specified, the first is used for the optimum and minimum spacings, and the second is used for maximum.
|Notes=When specified as a positive <code>length</code> value, the <code>word-spacing</code> attribute adds the specified value to the default spacing between words within an element. A negative <code>length</code> value decreases the space between words. Word spacing can be influenced by justification.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#word-spacing
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}