{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies what parts of an element’s content are  skipped over when applying any text decoration.}}
{{CSS Property
|Initial value=objects
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=textDecorationSkip
|Values={{CSS Property Value
|Data Type=none
|Description=Will not skip anything; the text decoration will be drawn for all text content
}}{{CSS Property Value
|Data Type=object
|Description=Will skip the element (including it’s margin) if it’s atomic inline
}}{{CSS Property Value
|Data Type=spaces
|Description=Will skip white space,  including:
* regular spaces - U+0020
* tabs - U+0009
* nbsp - U+00A0
* ideographic space - U+3000
* all fixed width spaces - examples: U+2000 to U+200A, U+202F and U+205F
* any adjacent letter-spacing or word-spacing
}}{{CSS Property Value
|Data Type=ink
|Description=Will skip over where any glyphs are drawn. It will interrupt the decoration line so that the text will show through where otherwise the decoration would cross through the text. This commonly includes ascenders and descenders of glyphs. 

Note: The UA also may skip over small distances on the right or the left side of the glyph outline
}}{{CSS Property Value
|Data Type=box-decoration
|Description=Will skip over the box's margin, border, and padding areas.

Note: It is not known yet if this is a needed value
}}{{CSS Property Value
|Data Type=edges
|Description=The text decoration will be inset slightly, so that two side by side elements do not appear to have a single continuous decoration. This is important for Chinese content, where underlining is a form of punctuation.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=This property inherits so the descendent elements can have different setting.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/
|Status=Candidate Recommendation
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/gg721763(v=expression.40).aspx
|HTML5Rocks_link=
}}