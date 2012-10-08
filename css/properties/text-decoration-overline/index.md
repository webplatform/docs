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
|Data Type=VARIANT_TRUE
|Description=A line is drawn over the text.
}}{{CSS Property Value
|Data Type=VARIANT_FALSE
|Description=A line is not drawn over the text.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''textDecorationOverline''' property to draw a line over the text when the user moves the mouse over the text.
|Code=&lt;P onmouseover{{=}}"this.style.textDecorationOverline{{=}}true;"&gt;
Mouse over this text for an overline.
&lt;/P&gt;
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''textDecorationOverline: '''VARIANT_TRUE '''{{!}}''' VARIANT_FALSE</code>
===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows Server 2003
|-
!Header
|<dl>
<dt>Mshtml.h</dt>
</dl>
|-
!IDL
|<dl>
<dt>Mshtml.idl</dt>
</dl>
|-
!DLL
|<dl>
<dt>Mshtml.dll</dt>
</dl>
|}
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
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/text-decoration|textDecoration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}