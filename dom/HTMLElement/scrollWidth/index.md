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
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=When the [[css/properties/overflow|'''overflow''']] property is set to '''auto''', the content can exceed the dimensions of an element, and scroll bars appear. You can use the '''scrollWidth''' property to retrieve the width of the content within the element.

This example uses the '''scrollWidth''' property to compare the viewable width of the content to the actual width of a '''div''' element. The width of the element is exposed through the [[dom/HTMLElement/offsetWidth|'''offsetWidth''']] property.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnCheckScroll() {
   var iScrollWidth {{=}} oDiv.scrollWidth;
   var iOffsetWidth {{=}} oDiv.offsetWidth;
   var iDifference {{=}} iScrollWidth - iOffsetWidth;
   alert("Width: " + iOffsetWidth
      + "\nscrollWidth: " + iScrollWidth
      + "\nDifference: " + iDifference); 
}
&lt;/script&gt;
...
&lt;div id{{=}}"oDiv" style{{=}}"overflow: scroll; height{{=}} 50px; width{{=}} 400px; text-align: left" nowrap&gt;
	... 
&lt;/div&gt;
&lt;button onclick{{=}}"fnCheckScroll()"&gt;Check scrollWidth&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollWidth.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The width is the distance between the left and right edges of the object's visible content.
This property is read-only on HTML documents, and read-write on fixed regions.
For more information about how to access the dimension and location of objects on the page through the Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
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