{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses scripting to set the '''name''' property of a frame.
|LiveURL=
|Code=
parent.frames[0].name{{=}}"Left";
}}
{{Single_Example
|Description=This example shows how the '''NAME''' attribute for a window can be persisted in HTML, but only when defined in a frame within a frameset.
|LiveURL=
|Code=
&lt;FRAMESET&gt;
    &lt;FRAME NAME{{=}}"Left" SRC{{=}}"blank.htm"&gt;
    &lt;FRAME NAME{{=}}"Right" SRC{{=}}"contents.htm"&gt;
&lt;/FRAMESET&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''name''' property identifies which frame displays the content of a linked document.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frame</code>
*<code>frameSet</code>
*<code>iframe</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}