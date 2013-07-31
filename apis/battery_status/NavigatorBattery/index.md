{{Page_Title}}
{{Flags
|Checked_Out=Yes
|Editorial notes={{Editorial
| this article is currently being worked on
}}
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The NavigatorBattery interface is exposed on the Navigator object.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=navigator.battery.onlevelchange = function () {
  console.log(navigator.battery.level);
};

/* or alternatively */

navigator.battery.addEventListener('levelchange', function () {
  console.log(navigator.battery.level);
}, false);
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
{{See_Also_Section}}
{{Topics|API, Mobile, Battery Status}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}