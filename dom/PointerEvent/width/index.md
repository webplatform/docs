{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The width (magnitude on the X axis), in CSS pixels, of the contact geometry of the pointer.}}
{{API_Object_Property
|Property_applies_to=dom/objects/PointerEvent
|Read_only=Yes
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Resizing an element to match the contact geometry
|Code=<div style="position:absolute; top:0px; left:0px; width:100px;height:100px;"></div>
<script>
window.addEventListener("pointerdown", checkPointerSize, false);
function checkPointerSize(event) {
	event.target.style.width = event.width + "px";
	event.target.style.height = event.height + "px";
}
</script>
}}{{Single Example}}
}}
{{Notes_Section
|Usage=This value may be updated on each event for a given pointer. For devices which have a contact geometry but the actual geometry is not reported by the hardware, a default value may be provided by the user agent to approximate the geometry typical of that pointer type. Otherwise, the value must be 0.
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}