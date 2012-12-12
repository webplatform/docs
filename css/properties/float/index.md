{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies whether or not a box (an element) should float.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Object displays where it appears in the text.
}}{{CSS Property Value
|Data Type=left
|Description=Text flows to the right of the object.
}}{{CSS Property Value
|Data Type=right
|Description=Text flows to the left of the object.
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
|Desktop_rows=
|Mobile_rows=
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