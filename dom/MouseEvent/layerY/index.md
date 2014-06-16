{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=Reviewed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/MouseEvent
|Read_only=No
|Javascript_data_type=Number
|Return_value_description=The scaled value of the mouse X and Y positions relative to the positioned elements' client position. This may be an integer or double value depending on the viewport scale value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=if(document.documentMode&&document.documentMode>=9){
  form.layerXCoords.value = evt.offsetX;
  form.layerYCoords.value = evt.offsetY;
  }
  else
  {
    form.layerXCoords.value = (evt.layerX)?evt.layerX:evt.offsetX;
  	form.layerYCoords.value = (evt.layerY)?evt.layerY:evt.offsetY;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
A positioned element is an element whose position property is set to <code>relative</code>, <code>absolute</code> or <code>fixed</code>. For more information about element positioning, see About Element Positioning.
'''Note'''  This property is provided for cross-browser compatibility. Use [[css/cssom/properties/y|'''y''']] instead.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
|Sources=MDN, MSDN, HTML5Rocks
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/event.layerX MDM Reference]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=[http://html5.litten.com/using-multiple-html5-canvases-as-layers/ Using Multiple HTML5 canvases as layers]
}}