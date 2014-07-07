{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN content
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=BSTR
|Description=A '''String''' that specifies the [[html/attributes/name|'''name''']] or [[html/attributes/id|'''id''']] property of the object to retrieve.  A collection is returned if more than one match is made.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''namedItem''' method to retrieve a '''div''' and change its [[dom/HTMLElement/innerText|'''innerText''']] property.
|Code=&lt;div id{{=}}"oDIV1"&gt;This text will not change.&lt;/div&gt;
&lt;div id{{=}}"oDIV2"&gt;This text will change.&lt;/div&gt;
&lt;button onclick{{=}}"document.all.namedItem('oDIV2').innerHTML{{=}}'Changed!';"&gt;
   Change Option
&lt;/button&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''namedItem''' method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched Defining Document Compatibility.
The '''namedItem''' method was introduced in Microsoft Internet Explorer 6.
The '''namedItem''' method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched '''element'''.
This method first searches for an object with a matching [[html/attributes/id|'''id''']] attribute. If a match is not found, the method searches for an object with a matching [[html/attributes/name|'''name''']] attribute, but only on those elements that are allowed a name attribute.
|Import_Notes====Standards information===
There are no standards that apply here.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}