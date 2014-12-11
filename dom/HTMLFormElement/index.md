{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=stub page, automatic content only (needs summary at minimum)
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/HTMLElement
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Iterate over elements in a form using the [[dom/HTMLElement/elements|HTMLElement#elements]] property
|Code=var form = document.getElementById('form');
var elements = {};
for(var i=0; i<form.elements.length; i++){
  if(!form.elements[i].name) continue;
  elements[form.elements[i].name] = form.elements[i];
}
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}