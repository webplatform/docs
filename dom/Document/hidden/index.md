{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
|Checked_Out=No
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=state
|Javascript_data_type=Boolean
|Return_value_description=<code>hidden</code> is a boolean value which is <code>true</code> if the page is not visible, even the smallest part, and this typically happens when the tab is in background or the browser is minimized. It's important to note that this rule has some exceptions for accessibility tools that act in full-screen mode.
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
|Notes====Remarks===
The '''Visibility''' API provides Web applications with the means to programmatically determine the current visibility of a page and be notified of visibility changes.
You can use this property to determine whether a page is visible or not. If it is not visible, you can throttle page activity and resource usage to create more power- and CPU-efficient applications.
This is a property of the '''document''' object.  You can also use the [[dom/Document/visibilityState|'''visibilityState''']] and [[dom/Document/visibilityState|'''visibilitychange''']] properties to learn more about the page visibility state.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=13.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=10.0
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Performance
|Manual_sections====Related pages (MSDN)===
*<code>window</code>
}}
{{Topics|DOM, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}