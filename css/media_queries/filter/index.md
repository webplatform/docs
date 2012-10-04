{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''-ms-filter''' attribute in Internet Explorer 8.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_8.htm
|Code=
-ms-filter: 'progid:DXImageTransform.Microsoft.MotionBlur(strength{{=}}50), progid:DXImageTransform.Microsoft.BasicImage(mirror{{=}}1)';

}}
{{Single_Example
|Description=The following example shows how to use an inline style sheet to set the filter on an image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_h.htm
|Code=
&lt;img style{{=}}"filter:progid:DXImageTransform.Microsoft.MotionBlur(strength{{=}}50)
    progid:DXImageTransform.Microsoft.BasicImage(mirror{{=}}1)"
    src{{=}}"/workshop/samples/author/dhtml/graphics/cone.jpg"
    height{{=}}"80px" width{{=}}"80px" alt{{=}}"cone"&gt;
}}
{{Single_Example
|Description=The following example shows how to use inline scripting to set the filter on an image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_s.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
function doFilter ()
{ 
    filterFrom.filters.item(0).Apply();
    // 12 is the dissolve filter.  
    filterFrom.filters.item(0).Transition{{=}}12;
    imageFrom.style.visibility {{=}} "hidden";
    filterTo.style.visibility {{=}} ""; 
    filterFrom.filters.item(0).play(14); 
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Click the image to start the filter.&lt;/p&gt;
// Call the function.
&lt;div id{{=}}"filterFrom" onclick{{=}}"doFilter()" 
    style{{=}}"position: absolute; 
        width: 200px; 
        height: 250px; 
        background-color: white; 
        filter: revealTrans()"&gt;
&lt;img id{{=}}"imageFrom" 
    style{{=}}"position: absolute; 
        top: 20px; 
        left: 20px;" 
    src{{=}}"sphere.jpg" 
    alt{{=}}"sphere"&gt;
&lt;div id{{=}}"filterTo" 
    style{{=}}"position: absolute; 
        width: 200px; 
        height: 250px; 
        top: 20px; 
        left: 20px; 
        background: white; 
        visibility: hidden;"&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-filter''' attribute is an extension to CSS, and can  be used as a synonym for '''filter''' in IE8 Standards mode. When you use '''-ms-filter''', enclose the progid in single quotes (') or double quotes ("). Use commas (,) to separate multiple values, as shown in the Examples section.
An object must have layout for the filter to render. A simple way to accomplish this is to give the element a specified [[css/properties/height|'''height''']] and [[css/cssom/properties/hasLayout|'''hasLayout''']]  property.
The shadow filter can be applied to the '''img''' object by setting the filter on the image's parent container.
The filter mechanism is extensible and enables you to develop and add  filters later. For more information about filters, see Introduction to Filters and Transitions.
Not available on the Macintosh platform.
|Import_Notes=
===Syntax===
<code>'''-ms-filter: '''filtertype1 (parameter1, parameter2,...) '''{{!}}''' filtertype2 (parameter1, parameter2,...)</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Media Queries
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}