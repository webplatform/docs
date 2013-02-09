{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Elements which get <code>float</code> applied with a value other than <code>none</code> are taken from the normal flow and get wrapped on the left or right side of the parent element. Other elements get wrapped around it.}}
{{CSS Property
|Initial value=none
|Applies to=all elements; but absolutely positioned, replaced elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=<code>none</code> indicates that the element does not contain any float at all. This is the initial value of the <code>float</code> property.
}}{{CSS Property Value
|Data Type=left
|Description=The <code>left</code> value indicates that the element must float to the left side of its containing block.
}}{{CSS Property Value
|Data Type=right
|Description=The <code>left</code> value indicates that the element must float to the right side of its containing block.

}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how the '''float''' attribute affects the flow of the text. The sphere image floats to the left of the text, and the cone floats to the right.
|Code=&lt;img src{{=}}"sphere.jpg" style{{=}}"float:left"&gt;
&lt;img src{{=}}"cone.jpg" style{{=}}"float:right"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/float_h.htm
}}{{Single Example
|Description=This example uses inline scripting and the '''float'''property to swap images when the mouse moves over the button.
|Code=&lt;IMG ID{{=}}oSphere SRC{{=}}"sphere.jpeg" STYLE{{=}}"float:left"&gt;
&lt;IMG ID{{=}}oCone SRC{{=}}"cone.jpeg" STYLE{{=}}"float:right"&gt;
:
&lt;BUTTON onmouseover{{=}}"oSphere.style.styleFloat{{=}}'right'; 
    oCone.style.styleFloat{{=}}'left'"
    onmouseout{{=}}"oSphere.style.styleFloat{{=}}'left'; 
    oCone.style.styleFloat{{=}}'right'"&gt;
    Flip-flop images.
&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/styleFloat.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
With a value of '''left''' or '''right''', the object is treated as block-level—that is, the [[css/properties/display|'''display''']] property is ignored. For example, floating paragraphs allow the paragraphs to appear side-by-side.
Objects following a floating object move in relation to the position of the floating object.
The floating object is moved left or right until it reaches the border, padding, or margin of another block-level object.
The '''div''' and '''span''' objects must have a width set for the '''float''' attribute to render. In Microsoft Internet Explorer 5, '''div''' and '''span''' objects are assigned a width by default and will render if a width is not specified.
|Import_Notes====Syntax===
<code>'''float: '''left '''{{!}}''' right '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.25
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
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