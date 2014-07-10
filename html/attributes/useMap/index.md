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
|Description=The following example defines the map. Clicking within the rectangular areas of the map loads a new page into a target window named <code>frame1</code>.
|Code=&lt;MAP NAME{{=}}"map1"&gt;
   &lt;AREA NAME{{=}}"area1" COORDS{{=}}"4,20,20,40" href{{=}}"left_arrow.htm" target{{=}}"frame1"/&gt;
   &lt;AREA NAME{{=}}"area2" COORDS{{=}}"116,20,100,40" href{{=}}"right_arrow.htm" target{{=}}"frame1"/&gt;
&lt;/MAP&gt;
}}{{Single Example
|Description=The following example shows '''USEMAP''' with an image.
|Code=&lt;IMG USEMAP{{=}}"#map1" BORDER{{=}}"0" SRC{{=}}"double_pointed_arrow.png"&gt;
}}{{Single Example
|Description=The following example shows '''USEMAP''' with an '''object'''. This technique requires Internet Explorer 8 and later.
|Code=&lt;OBJECT data{{=}}"double_pointed_arrow.png" border{{=}}"0" type{{=}}"image/gif" usemap{{=}}"#map1"&gt;
&lt;/OBJECT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''useMap''' property identifies the image as a client-side image map by associating a '''map''' object with the image. This '''map''' object contains '''area''' objects that define regions within the image. The user can click these regions to navigate to a designated URL.
You can dynamically assign the maps to the image through the '''useMap''' property.
In Microsoft Internet Explorer 6 and greater, this property applies to the '''object''' and '''input''' objects.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 13.6.1
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
*<code>img</code>
*<code>object</code>
*<code>input</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}