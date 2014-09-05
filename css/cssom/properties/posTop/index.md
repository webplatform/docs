{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Reflects the value of the Cascading Style Sheets (CSS) '''top''' attribute for positioned items.}}
{{API_Object_Property
|Property_applies_to=css/cssom/properties
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses the '''posTop''' property to move the first '''img''' object up by 10 units.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
document.all.tags("IMG").item(0).style.posTop -{{=}} 10;
&lt;/SCRIPT&gt;
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=This example uses a timer to change the value of the '''posTop''' in increments of 10.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
This property reflects the value of the Cascading Style Sheets (CSS) [[css/properties/top|'''top''']] attribute for positioned items. This property always returns zero for nonpositioned items because "top" has meaning only when the object is positioned.
If the '''top''' attribute is not set, the '''posTop''' property returns zero.		
Use the [[dom/HTMLElement/offsetTop|'''offsetTop''']] property to calculate actual positions within the document area.
Setting this property changes the value of the top position but leaves the units designator for the property unchanged.
Unlike the [[css/properties/top|'''top''']] property, the '''posTop''' property value is a floating-point number, not a string.

|Import_Notes=
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
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/properties/pixelTop|pixelTop]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}