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
|Description=This example uses the '''scrollLeft''' property to determine the amount scrolled by the object.
|Code=&lt;DIV ID{{=}}oDiv STYLE{{=}}"position:absolute; width:200px; 
    height:100px; overflow:scroll"                   
    onclick{{=}}alert(this.scrollLeft)&gt;
&lt;SPAN STYLE{{=}}"width:250px"&gt; . . . &lt;/SPAN&gt;&lt;/DIV&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This property's value equals the current horizontal offset of the content within the scrollable range. Although you can set this property to any value, if you assign a value less than 0, the property is set to 0. If you assign a value greater than the maximum value, the property is set to the maximum value.
You can set this property inline, but the results might be inconsistent while the document loads.
This property is always 0 for objects that do not have scroll bars. For these objects, setting the property has no effect.
When a '''marquee''' object scrolls vertically, its '''scrollLeft''' property is set to 0, overriding any script setting.
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
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