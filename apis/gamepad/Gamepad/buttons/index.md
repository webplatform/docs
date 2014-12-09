{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Array of values for all buttons of the gamepad.}}
{{API_Object_Property
|Property_applies_to=apis/gamepad/Gamepad
|Read_only=Yes
|Example_object_name=object
|Return_value_name=
|Javascript_data_type=
|Return_value_description=array of doubles.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The Gamepad API provides a function, [[dom/Navigator/getGamepads|Navigator.getGamepads]], that returns a list of all devices currently visible to the web page, as an array of Gamepad objects. When a gamepad is connected, this example reports its index, id, number of buttons, number of axes, and when the gamepad data was updated.
|Code=window.addEventListener("gamepadconnected", function(e) {
  var gp = navigator.getGamepads()[e.gamepad.index];
  console.log("Gamepad connected.");
  console.log("Gamepad index:", gp.index);
  console.log("Gamepad id:", gp.id);
  console.log("Gamepad buttons:", gp.buttons.length);
  console.log("Gamepad axes:", gp.axes.length);
  console.log("Gamepad last updated:", gp.timestamp);
});
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Gamepad Specification
|URL=https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Gamepad}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/Guide/API/Gamepad
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}