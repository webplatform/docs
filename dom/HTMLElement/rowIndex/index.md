{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example function shows how to use the '''rowIndex''' attribute to format a [[html/elements/table|'''table''']].  The function sets the background color of the rows in the '''table''' to black or white, alternating row by row.
|LiveURL=
|Code=
function formatTable(oTable)
{
  var rows{{=}}oTable.rows;
  for(var i{{=}}0;i&lt;rows.length;i++)
  {
    if(i%2{{=}}{{=}}0) {
      rows[i].style.backgroundColor {{=}} "black";
      rows[i].style.color {{=}} "white";
    } else {
      rows[i].style.backgroundColor {{=}} "white";
      rows[i].style.color {{=}} "black";
    }
  }
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property is different from [[dom/properties/sectionRowIndex|'''sectionRowIndex''']], which indicates the object's position in the '''tBody''', '''tHead''', or '''tFoot''' [[dom/properties/rows (table)|'''rows''']] collection. These sections are mutually exclusive, so the '''tr''' is always contained in one of these sections and in the [[html/elements/table|'''table''']]. You can determine the '''rowIndex''' property of an object by the order in which the object appears in the HTML source.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>tr</code>
*<code>Reference</code>
*<code>[[dom/properties/cellIndex|cellIndex]]</code>
*<code>[[dom/properties/sourceIndex|sourceIndex]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}