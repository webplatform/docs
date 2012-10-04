{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=msg|Data type=BSTR|Description=A '''String''' that contains the message data.|Optional=}}
{{Method Parameter|Name=targetOrigin|Data type=VARIANT|Description=A '''Variant''' of type '''String''' that specifies a target URI.|Optional=}}
|Method_applies_to=dom/window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=If Document A contains a reference
to the [[dom/properties/contentWindow|'''contentWindow''']] property
of Document B, script in Document A can send a message to Document B
by calling the '''postMessage''' method
as follows:
|LiveURL=
|Code=
var o {{=}} document.getElementsByTagName('iframe')[0];
o.contentWindow.postMessage('Hello World');
}}
{{Single_Example
|Description=The script in Document B can respond to the message
by registering the
[[dom/events/message|'''onmessage''']] event handler
for incoming messages.
|LiveURL=
|Code=
window.attachEvent('onmessage',function(e) {
    if (e.domain {{=}}{{=}} 'example.com') {
        if (e.data {{=}}{{=}} 'Hello World') {
            e.source.postMessage('Hello');
        } else {
            alert(e.data);
        }
    }
});
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Security Warning:  '''While "*" is a valid value for ''targetOrigin'', set the parameter to the value you expected to receive; otherwise, the security of your message might be compromised.  For more information about this security message, see Section 3.1.2 of the [http://go.microsoft.com/fwlink/?LinkId{{=}}199803 HTML5 Web Messaging] Specification (Editor's Draft) from the World Wide Web Consortium (W3C).
The '''postMessage''' method
allows cooperative text exchange between untrusted modules

from different domains embedded within a page. It does so
by ensuring a consistent and secure process
for text-based data exchange.
When a script invokes this method on a
'''window''' object,
the browser sends an
[[dom/events/message|'''onmessage''']]
event to the target document

on which the
[[dom/properties/data|'''data''']] property
has been set to the value passed in
''msg''.
When a target URI is passed into the method, it must have
at least a protocol and a host specified. The message will only be sent if
the target window has the same protocol and host as the specified target 
URI.
The '''postMessage''' method call
does not return until the event listeners of the target document
have finished executing.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging], Section 5.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>[[dom/events/message|onmessage]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}