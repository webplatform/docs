{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example provides the full code for an image map of the solar system. When you click the sun or any planet, you will link to the image associated with the x,y coordinate. You can click the Back button from the image to return to the solar system image map.
|Code=&lt;P&gt;&lt;IMG SRC{{=}}"solarsys.png" WIDTH{{=}}504 HEIGHT{{=}}126 
    BORDER{{=}}0 ALT{{=}}"Solar System" USEMAP{{=}}"#SystemMap"&gt;

&lt;MAP NAME{{=}}"SystemMap"&gt;
    &lt;AREA SHAPE{{=}}"rect" COORDS{{=}}"0,0,82,126" 
        HREF{{=}}"/workshop/graphics/sun.png"&gt;
    &lt;AREA SHAPE{{=}}"circle" COORDS{{=}}"90,58,3" 
        HREF{{=}}"/workshop/graphics/merglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"circle" COORDS{{=}}"124,58,8" 
        HREF{{=}}"/workshop/graphics/venglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"circle" COORDS{{=}}"162,58,10" 
        HREF{{=}}"/workshop/graphics/earglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"circle" COORDS{{=}}"203,58,8" 
        HREF{{=}}"/workshop/graphics/marglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"poly" COORDS{{=}}"221,34,238,37,257,32,278,
        44,284,60,281,75,288,91,267,87,253,89,237,81,229,
        64,228,54" HREF{{=}}"/workshop/graphics/jupglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"poly" COORDS{{=}}"288,19,316,39,330,37,348,
        47,351,66,349,74,367,105,337,85,324,85,307,77,303,
        60,307,50" HREF{{=}}"/workshop/graphics/satglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"poly" COORDS{{=}}"405,39,408,50,411,57,410,
        71,404,78,393,80,383,86,381,75,376,69,376,56,380,
        48,393,44" HREF{{=}}"/workshop/graphics/uraglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"poly" COORDS{{=}}"445,38,434,49,431,53,427,62,
        430,72,435,77,445,92,456,77,463,72,463,62,462,53,
        455,47" HREF{{=}}"/workshop/graphics/nepglobe.png"&gt;
    &lt;AREA SHAPE{{=}}"circle" COORDS{{=}}"479,66,3" 
        HREF{{=}}"/workshop/graphics/pluglobe.png"&gt;
&lt;/MAP&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
In Microsoft Internet Explorer 6 and greater this property applies to the [[html/elements/a|'''a''']] object.
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
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>area</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}