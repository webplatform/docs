{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=Yes
|Target=dom/Document
|Cancelable=Yes
|Content=The '''DOMContentLoaded''' event fires when the markup of a webpage has been parsed, which means it also fires before the [[dom/events/load|'''onload''']] event.
'''DOMContentLoaded''' is a good place to perform initialization tasks for your webpage, such as registering event handlers, initializing handles to support objects, and so on.  This allows your initialization tasks to occur while the remaining resources for the webpage are being downloaded.
For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}245080 DOMContentLoaded test drive demo.]
|Interface=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function logMsg( sMsg ) { 
  var oLog {{=}} document.getElementById('ResultLog');
  oLog.innerText +{{=}} "\n" + sMsg;
}

function addListener(obj, eventName, listener) {
	if( obj.addEventListener ) {
		obj.addEventListener( eventName, listener, false );
	} else {
		obj.attachEvent("on" + eventName, listener);
	}
}

function handleDCL( e ) {
  logMsg( "DOMContentLoaded event fired.\n" ); 
   var o {{=}} document.getElementById('button1');
   addListener(o, "click", handleClick1);
}

function handleClick1( e ) {
  logMsg( "Button 1 clicked.\n" ); 
}


if(!window.addEventListener) {
	logMsg( "Can't add eventListeners; not supported." )
} else {
   addListener(document, "DOMContentLoaded", handleDCL);
   addListener(window, "load", handleLoad);
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;button id{{=}}"button1"&gt;Click me&lt;/button&gt;
  &lt;div&gt;
   &lt;p id{{=}}"ResultLog"&gt;Results appear here &lt;/p&gt;
  &lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/single-page.html
|Status=Working Draft
|Relevant_changes=Section 8.2.6
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=16
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/events/load|onload]]</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}