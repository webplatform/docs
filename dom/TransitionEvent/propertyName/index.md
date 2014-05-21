{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/TransitionEvent
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the [[dom/Element/propertychange|'''onpropertychange''']] event to change the value of the '''propertyName''' property.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
function changeProp()
{
    btnProp.value {{=}} "This is the new VALUE";
}

function changeCSSProp()
{
    btnStyleProp.style.backgroundColor {{=}} "aqua";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;The event object property propertyName is 
    used here to return which property has been 
    altered.&lt;/P&gt;

&lt;INPUT TYPE{{=}}button ID{{=}}btnProp onclick{{=}}"changeProp()"
       VALUE{{=}}"Click to change the VALUE property 
       of this button"
       onpropertychange{{=}}'alert(event.propertyName + " 
       property has changed value")'&gt;
&lt;INPUT TYPE{{=}}button ID{{=}}btnStyleProp
       onclick{{=}}"changeCSSProp()"
       VALUE{{=}}"Click to change the CSS backgroundColor 
       property of this button"
       onpropertychange{{=}}'alert(event.propertyName + " 
       property has changed value")'&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/propertyNameEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
You can alter the value of '''propertyName''' by using it with the [[dom/Element/propertychange|'''onpropertychange''']] event.
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
{{See_Also_Section
|Topic_clusters=Javascript
}}
{{Topics|DOM, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}