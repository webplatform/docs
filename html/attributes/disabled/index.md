{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The disabled attribute prevents users from changing, clicking on, or submitting an element.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input
|Property_applies_to=dom/HTMLElement
|Content=When an element has the disabled attribute set, it appears dimmed and does not respond to user input. Disabled elements do not respond to mouse events or the [[html/attributes/contentEditable|contentEditable]] property.

If an element is contained within a disabled ([[html/attributes/fieldset|fieldset]], the fieldset will override its disabled attribute.

The disabled attribute will prevent javascript click events on the element.

If the disabled element is present without a value (<code><input disabled></code>) it will default to true. Other valid values are <code>true</code> and <code>false</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''disabled''' property to enable or disable a '''style''' object and a control.
|Code=&lt;style type{{=}}"text/css" id{{=}}"oStyle"&gt;
.styletest {
     background-color: black;
     color: white;
}
.styletest2 {
     background-color: black;
     color: red;
}
&lt;/style&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnSwitch(){
     if(oTest.enablement{{=}}{{=}}"enabled"){
          // Use an arbitrary attribute to track the status.
          oTest.enablement{{=}}"disabled";
          oButton.value{{=}}"Set disabled to false";
          oStyle.disabled{{=}}true;
          oDisableMe.disabled{{=}}true;
     }
     else{
          oButton.value{{=}}"Set disabled to true";
          oTest.enablement{{=}}"enabled";
          oStyle.disabled{{=}}false;
          oDisableMe.disabled{{=}}false;
     }
}
&lt;/script&gt;
...     
     &lt;p enablement{{=}}"enabled" id{{=}}"oTest" class{{=}}"styletest"&gt;
     A paragraph of text.
          &lt;input type{{=}}"button" id{{=}}"oDisableMe" class{{=}}"styletest" value{{=}}"Demonstration Button" onclick{{=}}"alert('Demonstration button')"&gt;
     &lt;/p&gt;
     &lt;input type{{=}}"button" id{{=}}"oButton" value{{=}}"Set disabled to true" onclick{{=}}"fnSwitch()"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/disabled.htm
}}
}}
{{Notes_Section}}
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
|Topic_clusters=HTML
}}
{{Topics|HTML, JavaScript, Security}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}