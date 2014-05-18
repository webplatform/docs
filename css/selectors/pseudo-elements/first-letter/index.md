{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The ::first-letter pseudo-element may be used for "initial caps" and "drop caps", which are common typographical effects.}}
{{CSS_Selector
|Content=The ::first-letter pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.

The following properties apply to the ::first-letter pseudo-element.
- background
- border
- border-bottom
- border-bottom-color
- border-bottom-style
- border-bottom-width
- border-collapse
- border-color
- border-left
- border-left-color
- border-left-style, border-left-width
- border-right
- border-right-color
- border-right-style
- border-right-width
- border-style
- border-top
- border-top-color
- border-top-style
- border-top-width
- border-width
- clear
- color
- float
- font
- font-family
- font-size
- font-style
- font-variant
- font-weight
- line-height
- margin
- padding
- text-decoration
- text-transform
- vertical-align
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following CSS will create "initial caps" by doubling the size of the first letter of any paragraph.
|Code=p::first-letter {
   font-size: 200%;
}
}}{{Single Example
|Language=CSS
|Description=The following CSS will create a drop capital spanning about two lines.
|Code=p::first-letter {
   font-size: 2.5em;
   float: left;
}
}}{{Single Example
|Language=HTML
|Code=<article>
<p>Text text text text text. Text text text text text text text . Text text text text. </p>
<p>Text text text text text. Text text text text text text text . Text text text text. </p>
<p>Text text text text text. Text text text text text text text . Text text text text. </p>
</article>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 Selectors
|URL=http://www.w3.org/TR/CSS2/selector.html#first-letter
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS 3 Selectors
|URL=http://www.w3.org/TR/css3-selectors/#first-letter
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=> 9
|Note=Only the one-colon form of this pseudo-element is recognized (:first-letter). Beginning with Internet Explorer 9, the first-letter pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form.
}}
}}
{{See_Also_Section
|Topic_clusters=Fonts, Pseudo-Elements, Selectors, Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}