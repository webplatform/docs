{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to determine the position of a '''td''' object. Although the '''td''' object appears to the far right in the document, its position is close to the x-axis and y-axis, because its offset parent is a [[html/elements/table|'''table''']] object rather than the document body.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
  &lt;TITLE&gt;Elements: Positions&lt;/TITLE&gt;
  &lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;

  function showPosition()
  {
    var oElement {{=}} document.all.oCell;
    
    alert("The TD element is at (" + oElement.offsetLeft + 
          "," + oElement.offsetTop + ")\n" + "The offset parent is " 
          + oElement.offsetParent.tagName );
  }
  &lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"showPosition()"&gt;
&lt;P&gt;This document contains a right-aligned table.
&lt;TABLE BORDER{{=}}1 ALIGN{{=}}right&gt;
  &lt;TR&gt;
    &lt;TD ID{{=}}oCell&gt;This is a small table.&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL='''Note'''  For Internet Explorer 4.0, this same example returns a position of 0,0 because the offset parent is the table row.
}}
}}
{{Notes_Section
|Notes====Remarks===
Most of the time the '''offsetParent''' property returns the '''body''' object.
'''Note'''  In Microsoft Internet Explorer 5, the '''offsetParent''' property returns the [[html/elements/table|'''table''']] object for the '''td''' object; in Microsoft Internet Explorer 4.0 it returns the '''tr''' object. You can use the [[dom/Element/parentElement|'''parentElement''']] property to retrieve the immediate container of the table cell.
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