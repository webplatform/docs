{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/xhr/objects/XMLHttpRequest
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example sets the
'''timeout''' property.
|LiveURL=
|Code=
var xhr;
xhr {{=}} new XMLHttpRequest();
xhr.open("GET", url, true);
xhr.timeout {{=}} 10000;
xhr.ontimeout {{=}} timeoutFired;
xhr.send(null);
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  
The '''timeout''' property has
a default value of 0.
If the time-out period expires, the
'''responseText''' property will be
null.
You should set a time-out value that is slightly longer than
the expected response time of the request.
The '''timeout''' property
may be set only in the time interval between a call to the
'''open''' method and the
first call to the '''send''' method.
If you set an '''XMLHttpRequest''' time-out value 
that is larger than the network stack's time-out value, the network stack
will time out first and the [[apis/xhr/events/timeout|'''ontimeout''']] 
event will not be raised.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>IHTMLXMLHttpRequest2</code>
*<code>XMLHttpRequest</code>
*<code>IHTMLXDomainRequest</code>
*<code>XDomainRequest</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}