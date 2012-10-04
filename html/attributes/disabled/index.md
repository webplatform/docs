{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''disabled''' property to enable or disable a '''style''' object and a control.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/disabled.htm
|Code=
&lt;style type{{=}}"text/css" id{{=}}"oStyle"&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
When an element is disabled, it appears dimmed and does not respond to user input. Disabled elements do not respond to mouse events, nor will they respond to the [[html/attributes/contentEditable|'''contentEditable''']] property.
If an element's '''disabled''' property is set to false but it is contained within a '''disabled''' element, it cannot override the  '''disabled''' state of its container.
For '''link''', '''style''' and [[css/cssom/styleSheet|'''styleSheet''']], the attribute sets or retrieves whether a style sheet is applied to the object.
'''Note'''  For '''OPTGROUP''' and '''OPTION''', the functionality specified by the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203769 HTML 4.01] standard is not currently implemented. You can define your own functionality.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>button</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>select</code>
*<code>textArea</code>
*<code>link</code>
*<code>style</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>optGroup</code>
*<code>option</code>
*<code>[[dom/properties/disabled (redundant)|disabled]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}