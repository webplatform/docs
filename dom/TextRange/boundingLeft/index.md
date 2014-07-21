{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.}}
{{API_Object_Property
|Property_applies_to=dom/TextRange
|Read_only=Yes
|Example_object_name=textRange
|Javascript_data_type=Number
|Return_value_description=the left coordinate of the bounding rectangle, in pixels.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example retrieves the value of the '''boundingLeft''' property for the given text area.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function boundDim(oObject)
{
    var oTextRange {{=}} oObject.createTextRange();
    if (oTextRange !{{=}} null) {
        alert("The bounding left is \n" + 
            oTextRange.boundingLeft);
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;textarea cols{{=}}"100" rows{{=}}"2" id{{=}}"oTextarea"
    onclick{{=}}"boundDim(this)"&gt; . . . &lt;/textarea&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
result = textRange.boundingLeft;

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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533539(v=vs.85).aspx boundingLeft Property]
|HTML5Rocks_link=
}}