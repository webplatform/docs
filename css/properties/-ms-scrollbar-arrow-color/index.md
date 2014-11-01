{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add summery, values, specifications, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/properties
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following example shows how to create a style rule that sets the '''-ms-scrollbar-arrow-color''' property for a '''textArea''' element.
|Code=&lt;HTML&gt;
  &lt;HEAD&gt;
    &lt;STYLE&gt;
        TEXTAREA.BlueArrow  { scrollbar-arrow-color:blue }
    &lt;/STYLE&gt;
  &lt;/HEAD&gt;  
  &lt;BODY&gt;
    &lt;TEXTAREA CLASS{{=}}"BlueArrow"&gt;The arrows in the scroll bar for 
    this element will be blue.&lt;/TEXTAREA&gt;
  &lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-scrollbar-arrow-color''' attribute is an extension to CSS, and can be used as a synonym for '''scrollbar-arrow-color''' in IE8 Standards mode.
The scroll arrows, located at each end of a scroll bar, are the square buttons containing the arrows that move the content on the screen in small increments, either up and down or left and right.
This property applies to elements that display a scroll bar.  Cascading Style Sheets (CSS) enable scrolling on all objects through the [[css/properties/overflow|'''overflow''']] property.  These objects are not listed in the Applies To list for this property.
|Import_Notes====Syntax===
<code>'''-ms-scrollbar-arrow-color: '''variant</code>
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Scrollbar
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultSelected]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/-ms-scrollbar-3d-light-color|-ms-scrollbar-3dlight-color]]</code>
*<code>[[css/properties/-ms-scrollbar-base-color|-ms-scrollbar-base-color]]</code>
*<code>[[css/properties/-ms-scrollbar-darkshadow-color|-ms-scrollbar-darkshadow-color]]</code>
*<code>[[css/properties/-ms-scrollbar-face-color|-ms-scrollbar-face-color]]</code>
*<code>[[css/properties/-ms-scrollbar-highlight-color|-ms-scrollbar-highlight-color]]</code>
*<code>[[css/properties/-ms-scrollbar-shadow-color|-ms-scrollbar-shadow-color]]</code>
*<code>[[css/properties/-ms-scrollbar-track-color|-ms-scrollbar-track-color]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}