{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=MSDN documentation only available on devChannel.
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Retrieves a snapshot of the data for the currently connected and interacted-with gamepads. Returns a [[apis/gamepad/Gamepad|Gamepad]] object.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Navigator
|Example_object_name=navigator
|Return_value_description=gamePads collection.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example detects when a gamepad is connected to the computer.
|Code=window.addEventListener("gamepadconnected", function(e) {
  var gp = navigator.getGamepads()[0];
  console.log("Gamepad connected at index %d: %s. %d buttons, %d axes.",
  gp.index, gp.id,
  gp.buttons.length, gp.axes.length);
});
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Gamepad Specification
|URL=https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html
|Status=W3C Working Draft
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
{{Topics|API, Gamepad}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Navigator.getGamepads navigator.getGamepads method]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/dn753843(v=vs.85).aspx Gamepad API in DevChannel]
|HTML5Rocks_link=
}}