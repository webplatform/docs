{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example reads the '''clipBottom''' property from the [[css/cssom/currentStyle|'''currentStyle''']] object of an image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipBottom.htm
|Code=
&lt;SCRIPT&gt;
function setClip(sOptionValue) {
    oImage.style.clip{{=}}"rect(0,100,"+sOptionValue+",0)";
    if (oImage.currentStyle.clipBottom {{=}}{{=}} "60px") {
        alert("The image has been clipped to 60px.");
        }
:
}	 
&lt;/SCRIPT&gt;
:
&lt;IMG ID{{=}}oImage SRC{{=}}"/workshop/graphics/sphere.png"&gt;
:
Pick an amount to clip the bottom: 
    // the option value is sent as an argument:
&lt;SELECT onchange{{=}}"setClip(value)"&gt;
&lt;OPTION VALUE{{=}}100&gt;reset &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}40&gt;40px &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}50&gt;50px &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}60&gt;60px &lt;/OPTION&gt;
&lt;/SELECT&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/clip|clip]]</code>
*<code>[[css/cssom/properties/clipLeft|clipLeft]]</code>
*<code>[[css/cssom/properties/clipRight|clipRight]]</code>
*<code>[[css/cssom/properties/clipTop|clipTop]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}