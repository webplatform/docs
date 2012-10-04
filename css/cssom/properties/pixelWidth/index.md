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
|Description=This example uses a timer to increment the '''pixelWidth''' property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm
|Code=
&lt;SCRIPT&gt;
function scaleThis()
{
    if (sphere.style.pixelWidth &lt;900) {
        sphere.style.pixelWidth +{{=}} 4;
        sphere.style.pixelHeight +{{=}}4;
        window.setTimeout("scaleThis();", 1);
    }
}
:
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Setting this property changes the value of the width without changing the units designator. Unlike the [[css/properties/width|'''width''']] property, the '''pixelWidth''' value is an integer, not a string, and is always interpreted in pixels.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
<code>'''pixelWidth: '''''
&lt;integer&gt;
''</code>
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
*<code>[[css/cssom/properties/posWidth|posWidth]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}