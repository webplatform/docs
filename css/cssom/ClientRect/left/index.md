{{Page_Title}}
{{Flags
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
|Return_value_name=pixelsFromLeft
|Javascript_data_type=Number
|Return_value_description=The number of pixels.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']] method to retrieve the coordinates of the bounds of the text rectangles within the element.
|Code=&lt;SCRIPT&gt;
function getCoords(oObject) {
    oBndRct{{=}}oObject.getBoundingClientRect();
    alert("Bounding rectangle {{=}} \nUpperleft coordinates: "
        + oBndRct.left + " " + oBndRct.top +
        "\nLowerright coordinates: "
        + oBndRct.right + " " + oBndRct.bottom);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;	
&lt;BODY&gt;
&lt;P ID{{=}}oPara onclick{{=}}"getCoords(this)"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm
}}
}}
{{Notes_Section
|Notes=To access the left coordinate of the second text rectangle of a [[dom/traversal/TextRange|'''TextRange''']] object, use this syntax:
 <code>oRct {{=}} oTextRange.getClientRects();
 oRct[1].left;</code>
Note that because the collection index starts at 0, the second item index is 1.
To access the left coordinate of the bounding rectangle of an element object, use this syntax:
 <code>oBndRct {{=}} oElement.getBoundingClientRect();
 oBndRct.left;</code>
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
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/properties/bottom|bottom]]</code>
*<code>[[dom/traversal/properties/right|right]]</code>
*<code>[[dom/traversal/properties/top|top]]</code>
*<code>[[dom/TextRectangle|TextRectangle]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}