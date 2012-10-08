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
|Description=The following examples use the list-style attribute and the '''list-style''' property to set the list style.

This example uses '''ul''' and <code>UL.compact</code> as selectors in an embedded (global) style sheet to define the styles of two different unordered lists.  For <code>UL.compact</code> to override the image that is set with the '''ul''' selector, you must explicitly set the '''image''' attribute to '''none'''.
|Code=&lt;STYLE&gt;
    UL { list-style: outside url(dot.gif) }
    UL.compact { list-style-image:none; list-style: inside circle }
&lt;/STYLE&gt; 
&lt;/HEAD&gt;
&lt;BODY&gt; 
&lt;UL&gt;
    &lt;LI&gt;...
    &lt;LI&gt;...
&lt;/UL&gt;
&lt;UL CLASS{{=}}compact&gt;
    &lt;LI&gt;...
    &lt;LI&gt;...
&lt;/UL&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style.htm
}}{{Single Example
|Description=This example uses inline scripting to change the style of the list. If the default image cannot be located, a hollow circle is used.
|Code=&lt;UL onmouseover{{=}}"this.style.listStyle{{=}}'url(dot.gif) circle'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyle.htm
}}{{Single Example
|Description=The following example sets the [[css/properties/display|'''display''']] property to '''list-item''', a new possible value as of Internet Explorer 6, to demonstrate that the '''list-style''' property can also apply to elements on which the '''display''' property is set.
|Code=&lt;SPAN onmouseover{{=}}"this.style.display{{=}}'list-item'"&gt;A line of text...&lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyle_2.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style''' property is a composite property. When specifying both the '''type''' and '''image''' values, the '''image''' value takes precedence, unless the '''image''' value is set to '''none''' or the image pointed to by the URL cannot display.
The '''list-style''' property also applies to all elements on which the [[css/properties/display|'''display''']] property is set to '''list-item'''.  To make the bullet points appear, you must explicitly set the [[css/properties/margin|'''margin''']] property or set the [[css/properties/list-style-position|'''list-style-position''']] property to '''inside''' on these elements.
|Import_Notes====Syntax===
<code>'''list-style: ''''''[''' type '''{{!}}{{!}}''' position '''{{!}}{{!}}''' image ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.6
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