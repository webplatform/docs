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
|Description=This example uses the '''posLeft''' property to move the first '''img''' object left by 10 units.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
document.all.tags("IMG").item(0).style.posLeft -{{=}} 10;
&lt;/SCRIPT&gt;
}}
{{Single_Example
|Description=This example uses a timer to change the value of the '''posLeft''' in increments of 10.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
function moveThis()
{
:
    if (sphere.style.posLeft&lt;900) {
        sphere.style.posTop +{{=}} 2;
        sphere.style.posLeft +{{=}} 2;
        window.setTimeout("moveThis();", 1);
        }
}
:
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property reflects the value of the Cascading Style Sheets (CSS) [[css/properties/left|'''left''']] attribute for positioned items. This property always returns zero for nonpositioned items because "left" has meaning only when the object is positioned. 
If the '''left''' attribute is not set, the '''posLeft''' property returns zero.		
Use the [[dom/properties/offsetLeft|'''offsetLeft''']] property to calculate actual positions within the document area.
Setting this property changes the value of the left position but leaves the units designator for the property unchanged.
Unlike the [[css/properties/left|'''left''']] property, the '''posLeft''' property value is a floating-point number, not a string.
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
<code>'''posLeft: '''float</code>
===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows 2000 Server
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
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/properties/pixelLeft|pixelLeft]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}