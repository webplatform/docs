{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A DOMString, starting with "::", containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, "".}}
{{API_Object_Property
|Property_applies_to=dom/AnimationEvent
|Read_only=Yes
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//for a predefined animation event
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the pseudo-element if used
var myAnimPseudoElem = myAnimEvent.pseudoElement;
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}