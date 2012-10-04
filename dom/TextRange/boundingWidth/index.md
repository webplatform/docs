{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/traversal/TextRange
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example retrieves the value of the '''boundingWidth''' property for the given text area.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm
|Code=
&lt;SCRIPT&gt;
function boundDim(oObject)
{
    var oTextRange {{=}} oObject.createTextRange();
    if (oTextRange !{{=}} null) {
        alert("The bounding width is \n" + 
            oTextRange.boundingWidth);
    }
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TEXTAREA COLS{{=}}100 ROWS{{=}}2 ID{{=}}oTextarea 
    onclick{{=}}"boundDim(this)"&gt; . . . &lt;/TEXTAREA&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TextRange|TextRange]]</code>
*<code>Reference</code>
*<code>boundingHeight</code>
*<code>boundingLeft</code>
*<code>boundingTop</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}