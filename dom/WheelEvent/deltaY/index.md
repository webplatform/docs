{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the distance that a mouse wheel has rotated around the y-axis (vertical).}}
{{API_Object_Property
|Property_applies_to=dom/WheelEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=deltaY
|Javascript_data_type=Number
|Return_value_description=The Y rotation distance in pixels, lines or pages.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to determine the deltaY property of the WheelEvent.
Note: to feature test for deltaY you need to use the 'deltaY' in event as deltaY may have a value of 0 (false)... (event.deltaY) can return false negatives.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function getDeltaMode(dMode){
	switch (dMode){
		case WheelEvent.DOM_DELTA_LINE:// 1
			return 'DOM_DELTA_LINE (1)';
		case WheelEvent.DOM_DELTA_PAGE:// 2
			return 'DOM_DELTA_PAGE (2)';
		case WheelEvent.DOM_DELTA_PIXEL:// 0
			return 'DOM_DELTA_PIXEL (0)';
		default:
			return 'Unknown DeltaMode:' + dMode;
		
	}
}
   function showWheelEvent(evt){
   		if(!evt)evt{{=}}window.event;
   		theform{{=}}document.forms.frmEvent;
   		if(evt.type{{=}}{{=}}'wheel'){
   			theform.deltamode.value{{=}}('deltaMode' in evt)?getDeltaMode(evt.deltaMode):'N/A';
   			theform.deltax.value{{=}}('deltaX' in evt)?evt.deltaX:'N/A';
   			theform.deltay.value{{=}}('deltaY' in evt)?evt.deltaY:'N/A';
   			theform.deltaz.value{{=}}('deltaZ' in evt)?evt.deltaZ:'N/A';
   		}
   
   }
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes=The measurement of the distance can be determined using the [[dom/WheelEvent/deltaMode|deltaMode]] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.4
}}
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent WheelEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974800(v=vs.85).aspx deltaY Property]
|HTML5Rocks_link=
}}