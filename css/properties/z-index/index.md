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
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. String that specifies the stacking order of the positioned objects based on the order in which the objects appear in the HTML source.
}}{{CSS Property Value
|Data Type=order
|Description=Integer that specifies the position of the object in the stacking order.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''z-index''' attribute and the '''z-index''' property to change the stacking order of objects.

This example uses an inline style sheet to set the stacking order.
|Code=&lt;img src{{=}}"cone.jpg" 
    alt{{=}}"cone"
    style{{=}}"position: absolute; 
        top: 100px; 
        left: 100px; 
        z-index: 4"&gt;
&lt;div style{{=}}"position:absolute; 
    top: 100px; 
    left: 100px;
    color: red; 
    background-color: #999966; 
    font-weight:bold; 
    z-index: 1"&gt;
...
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/z-index.htm
}}{{Single Example
|Description=This example uses inline scripting to set the stacking order.
|Code=&lt;img id{{=}}"cone" 
    alt{{=}}"cone"
    src{{=}}"cone.jpeg"
    style{{=}}"position: absolute;
        top: 10px;
        left: 10px;"
    onclick{{=}}"cone.style.zIndex{{=}}1; 
        sphere.style.zIndex{{=}}2"/&gt;
&lt;img id{{=}}"sphere" 
    alt{{=}}"sphere"
    src{{=}}"sphere.jpg"
    style{{=}}"position: absolute;
        top: 1px;
        left: 1px;"
    onclick{{=}}"cone.style.zIndex{{=}}2; 
        sphere.style.zIndex{{=}}1"/&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/zIndex.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Positive '''z-index''' values are positioned above a negative (or lesser value) '''z-index'''. Two objects with the same '''z-index''' are stacked according to source order. A positive value positions the element above text that has no defined '''z-index''', and a negative value positions it below. Set this parameter to null to remove the attribute.
The '''z-index''' property only applies to objects that have the [[css/properties/position|'''position''']] property set to '''relative''' or '''absolute'''.
The property does not apply to windowed controls, such as '''select''' objects.
Input from pointing devices, such as a mouse, does not penetrate through overlapping elements even if the elements are not visible. This is also true for positioned elements with a negative z-index unless:
*The parent is a scrolling container (that is, its [[css/properties/overflow|'''overflow''']] property is set to '''auto''' or '''scroll''').
*The parent is positioned (that is, its [[css/properties/position|'''position''']] property is set to '''absolute''', '''relative''', or '''fixed''').

As of Microsoft Internet Explorer 5.5, the '''iframe''' object is windowless and supports the '''z-index''' property.  In earlier versions of Windows Internet Explorer, the '''iframe''' object is windowed and, like all windowed controls, ignores the '''z-index''' property. If you maintain Web pages that were designed for earlier versions of Internet Explorer that do not support the '''z-index''' property, you might want to redesign the pages, especially if the pages contain '''iframe''' objects that are stacked on top of windowed controls, such as '''select''' objects. You can use the [[css/properties/visibility|'''visibility''']] attribute to hide windowed controls that you want an '''iframe''' object to overlap. You can also [[css/properties/position|'''position''']] windowed controls so that '''iframe''' objects do not overlap them.
As of Windows Internet Explorer 7, the '''select''' property is windowless and can make use of the '''z-index''' attribute and the '''z-index''' property.

Windows Internet Explorer 8 and later. When you access a property that has not been explicitly set, Internet Explorer returns the default value of the property. The default value of the '''z-index''' property for the [[css/cssom/currentStyle|'''currentStyle''']] object depends on the document compatibility mode used to display the Web page. When a page is displayed in IE8 Standards mode, the default value is <code>auto</code>. The default value is <code>0</code> in IE7 Standards mode and an empty string (<code>""</code>) in IE5 (Quirks) mode. Applications that rely on specific default values for the '''z-index''' property of the '''currentStyle''' object should be modified to take the document compatibility mode into account.
You can use the '''z-index''' property on Grid items.
While the '''z-index''' property normally only applies to objects that have the [[css/properties/position|'''position''']] property not set to '''static''', the '''z-index''' property applies to Grid items even when the '''position''' property is set to '''static'''.
|Import_Notes====Syntax===
<code>'''z-index: '''auto '''{{!}}''' ''order''</code>
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