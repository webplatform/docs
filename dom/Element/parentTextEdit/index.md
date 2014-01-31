{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example retrieves the parent object, if needed, creates the text range, moves to the original object, and selects the first word in the object.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
function selectWord()
{
    var oSource {{=}} window.event.srcElement ;
    if (!oSource.isTextEdit) 
        oSource {{=}} oSource.parentTextEdit;
    if (oSource !{{=}} null) {
        var oTextRange {{=}} oSource.createTextRange();
        oTextRange.moveToElementText(window.event.srcElement);
        oTextRange.collapse();
        oTextRange.expand("word");
        oTextRange.select();
    }
}
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The property is an object if the parent exists; otherwise, it is <code>null</code>. For example, the '''parentTextEdit''' property of the '''body''' is <code>null</code>.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}