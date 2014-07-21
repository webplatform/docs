{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Retrieves the width of the rectangle that bounds the TextRange object}}
{{API_Object_Property
|Property_applies_to=dom/TextRange
|Read_only=Yes
|Example_object_name=textRange
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=the width of the bounding rectangle, in pixels.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example retrieves the value of the '''boundingWidth''' property for the given text area.
|Code=&lt;script type{{=}}"text/html"&gt;
function boundDim(oObject)
{
    var oTextRange {{=}} oObject.createTextRange();
    if (oTextRange !{{=}} null) {
        alert("The bounding width is \n" + 
            oTextRange.boundingWidth);
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;textarea cols{{=}}"100" rows{{=}}"2" id{{=}}"oTextarea" 
    onclick{{=}}"boundDim(this)"&gt;  &lt;/textarea&gt;

|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm
}}
}}
{{Notes_Section
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533541(v=vs.85).aspx boundingWidth Property]
|HTML5Rocks_link=
}}