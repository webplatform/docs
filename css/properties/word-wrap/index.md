{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Remove topic cluster flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|An alias of [[css/properties/overflow-wrap]], word-wrap defines whether to break words when the content exceeds the boundaries of its container.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=wordWrap
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Lines can only be broken at normal break points (spaces, non-alphanumeric characters, etc.).
}}{{CSS Property Value
|Data Type=break-word
|Description=Words that exceed the width of the container will be arbitrarily broken to fit within the container's bounds.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This is the style rule that applies to the example.
|Code=.NormalValue		{ word-wrap:normal;     background-color:lightgray; }
.WithBreaks 		{ word-wrap:break-word; background-color:lightgray; }
.NormalValueNarrow	{ word-wrap:normal;     background-color:lightgray; width:10px }
.WithBreaksNarrow 	{ word-wrap:break-word; background-color:lightgray; width:10px }
.WithBreaksNoWrap  	 { word-wrap:break-word; background-color:lightgray; width:10px; white-space:nowrap; }
.clsLiteral        	 { font-family: Courier New, Courier, monospace; }
|LiveURL=http://code.webplatform.org/gist/5888667
}}{{Single Example
|Language=HTML
|Description=The following examples show how the [[css/properties/word-wrap]] property can be used to break one long word into multiple words on multiple lines. The ''break-word'' value avoids horizontal scrolling and can be useful for printing.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;wordWrap property&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;div class="body"&gt;

&lt;h1&gt;wordWrap property&lt;/h1&gt; 
&lt;p&gt;
&lt;strong&gt;Note&lt;/strong&gt; that the &lt;strong&gt;"p"&lt;/strong&gt; elements in the examples have layout because their widths are set.
&lt;/p&gt;

&lt;hr /&gt;

&lt;p&gt;
These examples shows the &lt;span class="clsLiteral"&gt;break-word&lt;/span&gt; value of the &lt;strong&gt;wordWrap&lt;/strong&gt; property.
&lt;/p&gt;

&lt;p class="WithBreaks"&gt;
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
&lt;/p&gt;

&lt;p class="WithBreaksNarrow"&gt;
blonde
&lt;/p&gt;

&lt;hr /&gt;
&lt;p&gt;
These examples show the &lt;span class="clsLiteral"&gt;normal&lt;/span&gt; value of the &lt;strong&gt;wordWrap&lt;/strong&gt; property. 
In quirks mode (transitional DOCTYPE), the field width is extended to fit the word.
&lt;/p&gt;

&lt;p class="NormalValue"&gt;
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
&lt;/p&gt;

&lt;p class="NormalValueNarrow"&gt;
blonde
&lt;/p&gt;

&lt;hr /&gt;

&lt;p&gt;
These examples show the &lt;span class="clsLiteral"&gt;break-word&lt;/span&gt; value of the 
&lt;strong&gt;wordWrap&lt;/strong&gt; property with &lt;span class="clsLiteral"&gt;white-space:nowrap&lt;/span&gt;.
&lt;/p&gt;

&lt;p class="WithBreaksNoWrap"&gt;
Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word 
&lt;/p&gt;

&lt;p class="WithBreaksNoWrap"&gt;
blonde
&lt;/p&gt;

&lt;hr /&gt;

&lt;p&gt;
To clip unwrapped text to the space provided, you can use &lt;span class="clsLiteral"&gt;overflow:hidden&lt;/span&gt; 
and &lt;span class="clsLiteral"&gt;text-overflow:ellipsis&lt;/span&gt;. 
&lt;/p&gt;

&lt;p class="NormalValue" style="overflow:hidden"&gt;
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
&lt;/p&gt;

&lt;p class="NormalValue" style="overflow:hidden;text-overflow:ellipsis"&gt;
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
&lt;/p&gt;

&lt;hr/&gt;
&lt;/div&gt; 

&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://code.webplatform.org/gist/5888667
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''word-wrap''' property was originally a proprietary property developed for Internet Explorer, and is used as a synonym for the standardized [[css/properties/overflow-wrap|'''overflow-wrap''']] property.
This property to enables the browser to break up otherwise unbreakable strings (words).
This differs from the [[css/properties/white-space|'''white-space''']] 
property, which turns wrapping of the text on and off.  
The '''word-wrap''' property specifies only whether wrapping can occur at a place in the word that is not otherwise allowed by the language rules in effect.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/css3-text/#overflow-wrap CSS Text Level 3], Section 6.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#overflow-wrap
|Status=W3C Recommendation
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