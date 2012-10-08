{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=above
|Description=Decoration appears above the text.
}}{{CSS Property Value
|Data Type=below
|Description=Decoration appears below the text.
}}{{CSS Property Value
|Data Type=auto
|Description=Default. Internet Explorer 6 and later. Decoration appears above the text if the [[html/attributes/lang|'''LANG''']] attribute is set to '''ja''', which is the language code abbreviation for the Japanese language, and the [[css/properties/writing-mode|'''-ms-writing-mode''']] attribute is set to '''tb-rl''', which causes vertical inline text progression.  If not, the decoration appears below the text.
}}{{CSS Property Value
|Data Type=auto-pos
|Description=Internet Explorer 6 and later. Identical to '''auto'''.
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
|Desktop_rows=
|Mobile_rows=
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