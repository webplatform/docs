{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The NavigatorBattery interface is exposed on the Navigator object.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=navigator.battery.onlevelchange = function () {
  console.log(navigator.battery.level);
};

/* or alternatively */

navigator.battery.addEventListener('levelchange', function () {
  console.log(navigator.battery.level);
}, false);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Battery Status, Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
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