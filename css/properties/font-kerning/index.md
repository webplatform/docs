{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>font-kerning</code> property allows contextual adjustment of inter-glyph spacing, i.e. the spaces between the characters in text. This property  controls <bold>metric kerning</bold> - that utilizes adjustment data contained in the font. Optical Kerning is not supported as yet.}}
{{CSS Property
|Initial value=auto
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=font
|Values={{CSS Property Value
|Data Type=auto
|Description=Used to specify kerning is at the discretion of the user agent.
}}{{CSS Property Value
|Data Type=normal
|Description=Specifies kerning is applied. Fonts that do not include kerning data are unaffected by this setting.
}}{{CSS Property Value
|Data Type=none
|Description=Specifies kerning is not applied
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=*Kerning will only be visible when supported.
|Code=&lt;p class="normal"&gt;WAVAWAVAWAVAWAVA&lt;/p&gt;
&lt;p class="none"    >WAVAWAVAWAVAWAVA&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/7283111
}}{{Single Example
|Language=CSS
|Description=*Kerning will only be visible when supported.
|Code=html { font-size: 62.5%; } 
p { font-family: "Arial", serif; font-size: 3.6rem }
p.normal {font-kerning: normal;}
p.none {font-kerning: none;}
|LiveURL=http://code.webplatform.org/gist/7283111
}}
}}
{{Notes_Section
|Usage=In <code>auto</code> setting, user agents can determine whether to apply kerning or not based on a number of factors like text size, script, or other factors that influence text processing speed. Authors who what proper kerning should use <code>'normal'</code> to explicitly enable kerning. Likewise, use <code>none</code> to explicitly disable kerning. There is a performance tradeoff when enabling kerning which might not have a large impact on text rendering speed for modern implementations.
|Notes=Kerning data is a must for this property to take effect. When rendering OpenType fonts, the opentype specification states that kerning be enabled by default. When kerning is enabled, the OpenType <code>kern</code> feature is enabled. <code>vkern</code> is used for vertical text. User Agents must also support kerning via data contained in a <code>kern</code> font table, as detailed in the OpenType specification. When used in conjunction with <code>letter-spacing</code>, kerning adjustments are considered part of the default spacing and letter spacing adjustments are made <bold>after</bold> kerning has been applied.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css-fonts-3/#font-kerning-prop
|Status=W3C Candidate Recommendation
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
|Topic_clusters=CSS Font, Fonts
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}