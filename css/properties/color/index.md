{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Merge Candidate, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=This article should be kept, and the data from http://docs.webplatform.org/wiki/css/Properties/color merged with it as appropriate.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=color
|Description=A '''String''' that specifies or receives one of the color names or RGB values in the Color Table.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''color''' attribute and the '''color''' property to change the text color of an object.

This example uses a call to an embedded (global) style sheet to change the text color to <code>red</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;STYLE&gt;
    .color1 { color:red }
    .color2 { color: }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SPAN STYLE{{=}}"font-size:14" onmouseover{{=}}"this.className{{=}}'color1'"
    onmouseout{{=}}"this.className{{=}}'color2'"&gt; . . .
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/color_h.htm
}}{{Single Example
|Code=&lt;SPAN STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.color{{=}}'red'"&gt;
:
&lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/color_s.htm
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}