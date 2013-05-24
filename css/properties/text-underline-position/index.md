{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Decoration appears above the text.
}}{{CSS Property Value
|Data Type=alphabetic
|Description=Decoration appears below the text.
}}{{CSS Property Value
|Data Type=under
|Description=Default. Internet Explorer 6 and later. Decoration appears above the text if the [[html/attributes/lang|'''LANG''']] attribute is set to '''ja''', which is the language code abbreviation for the Japanese language, and the [[css/properties/writing-mode|'''-ms-writing-mode''']] attribute is set to '''tb-rl''', which causes vertical inline text progression.  If not, the decoration appears below the text.
}}{{CSS Property Value
|Data Type=left
|Description=Internet Explorer 6 and later. Identical to '''auto'''.
}}{{CSS Property Value
|Data Type=right
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how all of the elements in a document inherit the '''-ms-text-underline-position''' style rule from the parent '''HTML''' element. 
Underline decorations throughout the document are positioned above the text, relative to the layout of the text.
|Code=&lt;HTML STYLE{{=}}"text-underline-position:above"&gt;
&lt;HEAD&gt;&lt;TITLE&gt;&lt;/TITLE&gt;&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;&lt;SPAN&gt;This horizontal SPAN element is not underlined.&lt;/SPAN&gt;  
&lt;SPAN STYLE{{=}}"text-decoration:underline"&gt;This horizontal SPAN 
element is underlined above the text.&lt;/SPAN&gt;&lt;/P&gt;
&lt;P STYLE{{=}}"writing-mode:tb-rl"&gt;&lt;SPAN&gt;This vertical SPAN element is 
not underlined.&lt;/SPAN&gt;  
&lt;SPAN STYLE{{=}}"text-decoration:underline"&gt;This vertical SPAN element 
is underlined above the text.&lt;/SPAN&gt;&lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textUnderlinePosition.htm
}}{{Single Example
|Description=The following example demonstrates the effect of the '''auto''' value of the '''-ms-text-underline-position''' property when the [[html/attributes/lang|'''LANG''']] attribute of an object containing vertical inline text is set to '''ja'''.
|Code=&lt;div style{{=}}"writing-mode:tb-rl; text-decoration:underline; 
  text-underline-position:auto"&gt;     
    &lt;p&gt;This element contains underlined vertical text.  
      The LANG attribute of this element is not explicitly set.
      The underline decoration appears below, or after, 
      the text when text-underline-position is set to auto.&lt;/p&gt;
    
    &lt;p lang{{=}}"ja"&gt;This element also contains underlined vertical text.  
      The LANG attribute of this element is set to ja.
      The underline decoration in this element appears above, 
      or before the text.&lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textUnderlinePositionAuto.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-text-underline-position''' attribute is an extension to CSS, and can be used as a synonym for '''text-underline-position''' in IE8 Standards mode.
This property specifies the position of the underline decoration. To turn the decoration on or off, use the [[css/properties/text-decoration|'''text-decoration''']] property.
The position of the underline decoration is relative to the layout of the text in the object.
With vertical text, it is more accurate to say that the '''above''' value causes the underline decoration to be laid out before the text or that the decoration appears before the text. With the '''below''' value, then, the decoration appears after the text.
In Internet Explorer 6, The '''auto''' and '''auto-pos''' values apply to this property as of Internet Explorer 6.  The default value of this property is '''auto''' as of Internet Explorer 6. With Microsoft Internet Explorer 5.5, the default value of this property is '''below'''.
|Import_Notes====Syntax===
<code>'''-ms-text-underline-position: '''above '''{{!}}''' below '''{{!}}''' auto '''{{!}}''' auto-pos</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}