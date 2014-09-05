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
{{Summary_Section|Reflects the value of the Cascading Style Sheets (CSS) '''height''' attribute for positioned items.}}
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
|Description=This example uses the '''posHeight''' property to increase the height of the first '''img''' element by 10 units.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
document.all.tags("IMG").item(0).style.posHeight +{{=}} 10;
&lt;/SCRIPT&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
This property reflects the value of the Cascading Style Sheets (CSS) [[css/properties/height|'''height''']] attribute for positioned items. This property always returns zero for nonpositioned items because "height" has meaning only when the object is positioned.  If the '''height''' attribute is not set, the '''posHeight''' property returns zero.
Unlike the [[css/properties/height|'''height''']] property, the '''posHeight''' property value is a floating-point number, not a string. Setting the '''posHeight''' property changes the value of the height but leaves the units designator for the property unchanged.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
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
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/properties/pixelHeight|pixelHeight]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}