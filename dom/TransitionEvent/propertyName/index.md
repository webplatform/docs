{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Specifies or retrives a string containg name of changed property.}}
{{API_Object_Property
|Property_applies_to=dom/TransitionEvent
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[dom/Element/propertychange|'''onpropertychange''']] event to change the value of the '''propertyName''' property.
|Code=&lt;!DOCTYPE html&gt;
&lt;html lang{{=}}"en"&gt;
&lt;head&gt;
&lt;script&gt;
    function inform() {
        //Get propertyName property
        alert(event.propertyName + " property has changed value")
    };

    function changeProperty() {
        btnProp.value {{=}} "This is the new VALUE";
    };

    function changeCSSProperty() {
        btnStyleProp.style.backgroundColor {{=}} "aqua";
    };
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;The event object property propertyName is used here to return which property has been altered.&lt;/p&gt;
    &lt;input 
      id{{=}}"btnProp"
      type{{=}}"button"
      value{{=}}"Click to change the VALUE property of this button"
      onclick{{=}}"changeProperty()"
      onpropertychange{{=}}"inform()"
    /&gt;
    &lt;input 
      id{{=}}"btnStyleProp"
      type{{=}}"button"
      value{{=}}"Click to change the CSS backgroundColor property of this button"
      onclick{{=}}"changeCSSProperty()"
      onpropertychange{{=}}"inform()"
    /&gt;
&lt;/body&gt;
&lt;/html&gt;
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