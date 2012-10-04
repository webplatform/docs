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
|Description=The following example applies the '''-ms-interpolation-mode''' attribute to determine the resampling algorithm of stretched images. The sample requires Internet Explorer 7 or later to view.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/css/msInterpolation.htm
|Code=
&lt;html&gt;
&lt;head&gt;
&lt;style&gt;
img.highqual { -ms-interpolation-mode:bicubic }
img.nearestn { -ms-interpolation-mode:nearest-neighbor }
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;img src{{=}}"sphere.jpg" width{{=}}"175" height{{=}}"350" class{{=}}"nearestn"&gt;
&lt;img src{{=}}"sphere.jpg" width{{=}}"175" height{{=}}"350"&gt;
&lt;img src{{=}}"sphere.jpg" width{{=}}"175" height{{=}}"350" class{{=}}"highqual"&gt;
&lt;p&gt;Change the zoom level of the page to see the difference.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''-ms-interpolation-mode''' property is obsolete as of Windows Internet Explorer 9. Do not use. The '''-ms-interpolation-mode''' property was introduced in Windows Internet Explorer 7.
The '''-ms-interpolation-mode''' property applies to stretched images only. For example, if the natural width of the image is 200x200 but the page designer specifies that the height and width should be 400x400, then the image will be stretched to the new dimensions using the nearest-neighbor algorithm, unless otherwise specified.
If the zoom level of the page is 100%, the default interpolation is nearest-neighbor,  otherwise bicubic mode is used.
|Import_Notes=
===Syntax===
<code>'''-ms-interpolation-mode: '''nearest-neighbor '''{{!}}''' bicubic</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
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