{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines whether to break words when the content exceeds the boundaries of its container. The '''word-wrap''' property is an alternate name for the [[css/properties/overflow-wrap]] property.}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Content exceeds the boundaries of its container.
}}{{CSS Property Value
|Data Type=break-word
|Description=Content wraps to next line, and a word-break occurs when necessary.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The word "blonde" is not wrappable under typical English rules.  
But, when wordWrap is set to break-word, 
the word "blonde" can be split onto two lines in any way the browser chooses: 
such as "b" and "londe", or "blo" and "nde".



The following example shows how to use the '''break-word''' value of the '''-ms-word-wrap''' property to break one long word onto multiple lines. This value avoids horizontal scrolling and can be useful for printing.  The '''p''' element in this example has layout, because its width is set.
|Code=&lt;P STYLE{{=}}"word-wrap:break-word;width:100%;left:0"&gt;
LongWordLongWord...LongWordLongWord&lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wordWrap.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''word-wrap''' attribute was originally a proprietary property developed for Internet Explorer, and is used as a synonym for the standardized [[css/properties/overflow-wrap]].
This property to enables the browser to break up otherwise unbreakable strings (words).
This differs from the [[css/properties/white-space|'''white-space''']] 
property, which turns wrapping of the text on and off.  
The '''word-wrap''' property permits only whether wrapping can occur at a place in the word that is not otherwise allowed by the language rules in effect.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/css3-text/#overflow-wrap CSS Text Level 3], Section 6.2
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
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}