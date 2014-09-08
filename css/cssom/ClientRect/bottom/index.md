{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/cssom/ClientRect
|Read_only=Yes
|Example_object_name=clientRect
|Return_value_name=pixelsFromBottom
|Javascript_data_type=Number
|Return_value_description=The number of pixels.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[dom/HTMLElement/getBoundingClientRect|'''getBoundingClientRect''']] method to retrieve the coordinates of the bounds of the text rectangles within the element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;&lt;title&gt;
  &lt;script&gt;
function getCoords() {
  oBndRct{{=}}this.getBoundingClientRect();
  console.log("Bounding rectangle {{=}} \nUpper left coordinates: " +
    oBndRct.left + " " + oBndRct.top +
    "\nLower right coordinates: " +
    oBndRct.right + " " + oBndRct.bottom);
}
window.addEventListener("load", getCoords, false);
  &lt;/script&gt;
 &lt;/head&gt;	
 &lt;body&gt;
  &lt;p &gt;&lt;/p&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm
}}
}}
{{Notes_Section
|Usage=
|Notes=This syntax shows how to access the bottom coordinate of the second text rectangle of a [[dom/TextRange|'''TextRange''']] oTextRange object.
 <code>oRct {{=}} oTextRange.getClientRects();
 oRct[1].bottom;</code>
Note that the collection index starts at 0, so the second item index is 1.
This syntax shows how to access the bottom coordinate of the bounding rectangle of an oElement element object.
 <code>oBndRct {{=}} oElement.getBoundingClientRect();
 oBndRct.bottom;</code>
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
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}