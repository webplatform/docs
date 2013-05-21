{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets  list-style-type, list-style-position, list-style-image properties in one declaration.}}
{{CSS Property
|Initial value=disc outside none
|Applies to=elements with display: list-item
|Inherited=Yes
|Media=visual
|Computed value=see individual properties
|Animatable=No
|Values={{CSS Property Value
|Data Type=type
|Description=Any of the range of type values available to the [[css/properties/list-style-type|'''list-style-type''']] property.
}}{{CSS Property Value
|Data Type=position
|Description=Any of the range of position values available to the [[css/properties/list-style-position|'''list-style-position''']] property.
}}{{CSS Property Value
|Data Type=image
|Description=Any of the range of image values available to the [[css/properties/list-style-image|'''list-style-image''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example sets two different values on the [[list-style property]] of two separate lists. The first list has '''list-style''' set to <code>"outside url('bullet.png')"</code>. The second list has '''list-style''' set to <code>"inside circle"</code>. 

This example uses '''ul''' and <code>UL.compact</code> as selectors in an embedded (global) style sheet to define the styles of two different unordered lists.  For <code>UL.compact</code> to override the image that is set with the '''ul''' selector, you must explicitly set the '''image''' attribute to '''none'''.
|Code=ul {  
 list-style: outside url('http://docs.webplatform.org/w/images/3/3f/bullet.png')  
 }  
 
 ul.list2  {  
 list-style-image: none; list-style: inside circle  
 }

|LiveURL=http://code.webplatform.org/gist/5617678
}}{{Single Example
|Language=HTML
|Code=&lt;p&gt;The first list:&lt;/p&gt;
&lt;ul&gt;
  &lt;li&gt;first item of the first list&lt;/li&gt;
  &lt;li&gt;second item of the first list&lt;/li&gt; 
&lt;/ul&gt; 

&lt;p&gt;The second list.:&lt;/p&gt; 
&lt;ul class=list2&gt;  
	&lt;li&gt;first item of the second list&lt;/li&gt;  
	&lt;li&gt;second item of the second list&lt;/li&gt; 
&lt;/ul&gt;

}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style''' property is a composite property. When specifying both the '''type''' and '''image''' values, the '''image''' value takes precedence, unless the '''image''' value is set to '''none''' or the image pointed to by the URL cannot display.
The '''list-style''' property also applies to all elements on which the [[css/properties/display|'''display''']] property is set to '''list-item'''.  To make the bullet points appear, you must explicitly set the [[css/properties/margin|'''margin''']] property or set the [[css/properties/list-style-position|'''list-style-position''']] property to '''inside''' on these elements.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Lists and Counters Module Level 3
|URL=http://dev.w3.org/csswg/css3-lists/#list-style
|Status=Working Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/generate.html#propdef-list-style
|Status=Recommendation
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
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Generated and Replaced Content
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}