{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Replaces the list-item marker with an image.}}
{{CSS Property
|Initial value=none
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Computed value=absolute URI or 'none'
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. No image is specified.
}}{{CSS Property Value
|Data Type=url(sURL)
|Description=Location of the image, where sURL is an absolute or relative URL.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''list-style-image''' attribute and the '''list-style-image''' property to set the image for markers.

This example uses '''ul''' as a selector in an embedded (global) style sheet to set the marker to the dot.gif image.
|Code=&lt;STYLE&gt;
    UL { list-style-image:url(dot.gif) }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-image.htm
}}{{Single Example
|Description=This example uses inline scripting to change the style of the list-item marker to an image when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;UL onmouseover{{=}}"this.style.listStyleImage{{=}}'url(dot.gif)'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyleImage.htm
}}
}}
{{Notes_Section
|Usage=The property has limited positioning options for the background image, and in some circumstances doesn’t work at all in IE. 
So it has become a far more common practice to simply set a background image on the list items.
|Notes====Remarks===
The '''list-style-image''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]: '''list-item''' property is available starting with Microsoft Internet Explorer 6.
When the image is available, it replaces the marker that is set with the [[css/properties/list-style-type|'''list-style-type''']] marker.
If the left margin of the list item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show. The margin should be set to a minimum of 30 points.
|Import_Notes====Syntax===
<code>'''list-style-image: '''url(sURL) '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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