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
|Description=This example uses the '''scrollTop''' property to determine the amount scrolled by the object.
|Code=&lt;div id{{=}}"oDiv" style{{=}}"position: absolute; 
    width: 200px; 
    height: 100px; 
    overflow: scroll" 
    onclick{{=}}"alert(this.scrollTop)"&gt;
	&lt;span style{{=}}"width: 250px"&gt;. . . &lt;/span&gt;
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollTop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This property's value equals the current vertical offset of the content within the scrollable range. Although you can set this property to any value, if you assign a value less than 0, the property is set to 0. If you assign a value greater than the maximum value, the property is set to the maximum value.
You can set this property inline, but the results might be inconsistent while the document is loading.
This property is always 0 for objects that do not have scroll bars. For these objects, setting the property has no effect.
When a '''marquee''' object scrolls horizontally, its '''scrollTop''' property is set to 0, overriding any script setting.
For more information about how to access the dimension and location of elements on the document through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
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