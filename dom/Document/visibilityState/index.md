{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Returns the visibility state of a webpage.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=visibilityState
|Javascript_data_type=String
|Return_value_description=The current visibility state of the document, one of "hidden", "visible", "prerender", "unloaded".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var timer = 0;
var PERIOD_VISIBLE = 1000;
var PERIOD_NOT_VISIBLE = 60000;

function onLoad() {
   timer = setInterval(checkEmail, (document.hidden) ? PERIOD_NOT_VISIBLE : PERIOD_VISIBLE);
   if(document.addEventListener) document.addEventListener("visibilitychange", visibilityChanged);
}

function visibilityChanged() {
   clearTimeout(timer);
   timer = setInterval(checkEmail, (document.hidden) ? PERIOD_NOT_VISIBLE : PERIOD_VISIBLE);
}

function checkEmail() { 
   // Check server for new messages
}

window.onload = onLoad;
}}
}}
{{Notes_Section
|Notes=Use the [[dom/Document/visibilitychange|'''visibilitychange''']] property to track changes to the visibility state.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Page Visibility
|URL=http://www.w3.org/TR/page-visibility/
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Performance
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Document/hidden|hidden]]</code>
*<code>[[dom/Document/visibilitychange|visibilitychange]]</code>
}}
{{Topics|DOM, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}