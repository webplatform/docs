{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=summary needed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
|Read_only=No
|Example_object_name=declaration
|Javascript_data_type=String
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example demonstrates how to read the '''clipTop''' property from the [[css/cssom/currentStyle|'''currentStyle''']] object of an image.
|Code=&lt;SCRIPT&gt;
function setClip(sOptionValue) {
    oImage.style.clip{{=}}"rect("+sOptionValue+",100,100,0)";
    if (oImage.currentStyle.clipTop {{=}}{{=}} "60px") {
        alert("The image has been clipped to 60px.");
        }
:
}	 
&lt;/SCRIPT&gt;
:
&lt;IMG ID{{=}}oImage SRC{{=}}"/workshop/graphics/sphere.png"&gt;
:
Pick an amount to clip the top: 
    // the option value is sent as an argument:
&lt;SELECT onchange{{=}}"setClip(value)"&gt;
&lt;OPTION VALUE{{=}}100&gt;reset &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}40&gt;40px &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}50&gt;50px &lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}60&gt;60px &lt;/OPTION&gt;
&lt;/SELECT&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipTop.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/clip|clip]]</code>
*<code>[[css/cssom/properties/clipBottom|clipBottom]]</code>
*<code>[[css/cssom/properties/clipLeft|clipLeft]]</code>
*<code>[[css/cssom/properties/clipRight|clipRight]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}