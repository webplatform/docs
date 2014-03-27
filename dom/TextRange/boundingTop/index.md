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
|Property_applies_to=dom/TextRange
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example retrieves the value of the '''boundingTop''' property for the given text area.
|Code=&lt;SCRIPT&gt;
function boundDim(oObject)
{
    var oTextRange {{=}} oObject.createTextRange();
    if (oTextRange !{{=}} null) {
        alert("The bounding top is \n" + 
            oTextRange.boundingTop + oObject.scrollTop);
    }
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TEXTAREA COLS{{=}}100 ROWS{{=}}2 ID{{=}}oTextarea 
    onclick{{=}}"boundDim(this)"&gt; . . . &lt;/TEXTAREA&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  If the [[dom/TextRange|'''TextRange''']] is inside a '''textArea''' object, add the value of the element's [[dom/HTMLElement/scrollTop|'''scrollTop''']] property to the value of '''boundingTop'''.
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