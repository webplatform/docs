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
|Description=The underline is positioned relative to the alphabetic baseline. In this case the underline is likely to cross some descenders. Decoration appears below the text.
}}{{CSS Property Value
|Data Type=under
|Description=The underline is positioned under the element's text content. In this case the underline usually does not cross the descenders. (This is sometimes called "accounting" underline.) This value can be combined with ‘left’ or ‘right’ if a particular side is preferred in vertical writing modes.
}}{{CSS Property Value
|Data Type=left
|Description=In vertical writing modes, the underline is aligned as for ‘under’, except it is always aligned to the left edge of the text. If this causes the underline to be drawn on the "over" side of the text, then an overline also switches sides and is drawn on the "under" side.
}}{{CSS Property Value
|Data Type=right
|Description=In vertical writing modes, the underline is aligned as for ‘under’, except it is always aligned to the right edge of the text. If this causes the underline to be drawn on the "over" side of the text, then an overline also switches sides and is drawn on the "under" side.
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
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/#text-underline-position-property
|Status=Working Draft
}}
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