{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=Yes
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=
|LiveURL=
|Code=
&lt;!doctype html&gt;
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

}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''DOMContentLoaded''' event fires when the markup of a webpage has been parsed, which means it also fires before the [[dom/events/load|'''onload''']] event.
'''DOMContentLoaded''' is a good place to perform initialization tasks for your webpage, such as registering event handlers, initializing handles to support objects, and so on.  This allows your initialization tasks to occur while the remaining resources for the webpage are being downloaded.
For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}245080 DOMContentLoaded test drive demo.]
'''Note'''  The '''DOMContentLoaded''' event is supported only for webpages displayed using IE9 Standards mode or higher.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 8.2.6


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''[[dom/objects/Event|<b>Event''']]</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/events/load|onload]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}