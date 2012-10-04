{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=inherit |Description=Default. Object inherits the visibility of the next parent object.}}
{{CSS_Property_Value|Data Type=visible |Description=Object is visible.}}
{{CSS_Property_Value|Data Type=hidden |Description=Object is hidden.}}
{{CSS_Property_Value|Data Type=collapse |Description=Internet Explorer 8. Used in tables to remove '''tr''' and '''col'''; for all other elements, same as '''hidden'''.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''visibility'''  attribute and the '''visibility''' property to determine whether the object is visible.

This example uses two calls to an embedded (global) style sheet to hide and then show the image when the user moves the mouse over and off the text.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/visibility_h.htm
|Code=
&lt;head&gt;
&lt;style&gt;
.vis1 {
    visibility: visible;
}
.vis2 {
    visibility: hidden;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;img id{{=}}"oSphere" src{{=}}"sphere.jpg" alt{{=}}"sphere"&gt;
&lt;p onmouseover{{=}}"oSphere.className{{=}}'vis2'" 
    onmouseout{{=}}"oSphere.className{{=}}'vis1'"&gt;
Mouseover this text to make the sphere disappear.&lt;/p&gt;
&lt;/body&gt;
}}
{{Single_Example
|Description=This example uses a call to a function to hide the image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/visibility_s.htm
|Code=
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function disappear()
{
    oSphere.style.visibility{{=}}"hidden"; 
    }
function reappear()
{
    oSphere.style.visibility{{=}}"visible"; 
    }
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;img src{{=}}"sphere.jpeg" id{{=}}"oSphere"&gt;
&lt;p id{{=}}"oTxt" onmouseover{{=}}"disappear()" onmouseout{{=}}"reappear()"&gt;Move the mouse 
over this text to make the sphere disappear.&lt;/p&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Unlike [[css/properties/display|'''display''']], objects that are not visible still reserve the same physical space in the content layout as they would if they were visible. You can change the visibility through scripting to show and hide overlapping content based on user interaction. For document style scripting information, see Introduction to Dynamic Styles.
As of Microsoft Internet Explorer 5, a child object can be '''visible''' when its parent is '''hidden'''.  With Microsoft Internet Explorer 4.0, the parent object must be '''visible''' for a child object to be '''visible'''.
|Import_Notes=
===Syntax===
<code>'''visibility: '''visible '''{{!}}''' hidden '''{{!}}''' collapse '''{{!}}''' inherit</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Background, Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}