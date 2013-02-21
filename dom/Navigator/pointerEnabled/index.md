{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Indicates if the browser will fire pointer events for pointing input.}}
{{API_Object_Property
|Property_applies_to=dom/navigator
|Read_only=Yes
|Example_object_name=navigator
|Javascript_data_type=Boolean
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Basic HTML5 Canvas painting application
|Code=<style>
  /* Disable intrinsic user agent touch behaviors (such as panning or zooming) so 
  that all events are given to the application instead. */
  
  html { 
    touch-action: none; 
  }
</style>

<canvas id="drawSurface" width="500px" height="500px" style="border:1px solid black;"></canvas>

<script type='text/javascript'>
window.addEventListener('load', function() {
  var canvas = document.getElementById("drawSurface"),
  context = canvas.getContext("2d");
  if (window.navigator.pointerEnabled) {
    canvas.addEventListener("pointermove", paint, false);
	if(window.navigator.maxTouchPoints>1)
		alert("Your user agent and hardware support multi-touch!");
  } 
  else {
	//Provide fallback for user agents that do not support Pointer Events
    canvas.addEventListener("mousemove", paint, false);
  }
  function paint(event) {
	if(event.buttons>0)
		context.fillRect(event.clientX, event.clientY, 5, 5);
  }
});
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents/
|Status=Working Draft
|Relevant_changes=Section 5
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=IE10
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Supported as: [http://msdn.microsoft.com/en-us/library/ie/hh972895(v=vs.85).aspx msPointerEnabled]
}}
}}
{{See_Also_Section
|Topic_clusters=Pointer Events
|Manual_sections=Feature Detection
* [[dom/navigator/maxTouchPoints|maxTouchPoints]]

Events
* [[dom/events/gotpointercapture|gotpointercapture]]
* [[dom/events/lostpointercapture|lostpointercapture]]
* [[dom/events/pointercancel|pointercancel]]
* [[dom/events/pointerdown|pointerdown]]
* [[dom/events/pointerenter|pointerenter]]
* [[dom/events/pointerleave|pointerleave]]
* [[dom/events/pointermove|pointermove]]
* [[dom/events/pointerout|pointerout]]
* [[dom/events/pointerover|pointerover]]
* [[dom/events/pointerup|pointerup]]

Objects
* [[dom/objects/PointerEvent|PointerEvent]]

Methods
* [[dom/methods/setPointerCapture|setPointerCapture]]
* [[dom/methods/releasePointerCapture|releasePointerCapture]]

CSS Properties
* [[css/properties/touch-action|touch-action]]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}