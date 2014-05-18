{{Page_Title|font-variant}}
{{Flags
|High-level issues=Merge Candidate
|Checked_Out=No
|Editorial notes={{Editorial/Merge_Candidate|Other=/css/properties/font-variant}}

Double Entry (/css/properties/font-variant)

}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Selects a normal, or small-caps face from a font family. Also possible by using the font shorthand.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=yes
|Media=visual
|Computed value=As specified
|Animatable=no
|CSS object model property=N/A
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Specifies a normal font face.
}}{{CSS Property Value
|Data Type=small-caps
|Description=Specifies a small-caps labeled font. If no small-case font is available, some browser (e.g. Firefox) simulate a small-case font by replacing the lowercase characters by scaled uppercase letters.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherit to the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example to show the effect achieved when small-caps are applied to a text paragraph.
|Code=<p>I think WebPlatform rocks.</p>
|LiveURL=http://code.webplatform.org/gist/5716625
}}{{Single Example
|Language=CSS
|Description=The CSS applied to the HTML above.
|Code=p {
  font-variant: small-caps;	
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 3
|URL=http://www.w3.org/TR/css3-fonts/#font-variant-prop
|Status=W3C Candidate Recommendation
|Relevant_changes=Extends the property (not yet in this entry)
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/fonts.html#small-caps
|Status=W3C Recommendation
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
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS, Design}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}