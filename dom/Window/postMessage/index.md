{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sends a cross-document message.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=msg
|Data type=String
|Description=A '''String''' that contains the message data.
|Optional=No
}}{{Method Parameter
|Name=targetOrigin
|Data type=String
|Description=A '''Variant''' of type '''String''' that specifies a target URI.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=targetFrame
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=If Document A contains a reference
to the [[dom/HTMLIFrameElement/contentWindow|'''contentWindow''']] property
of Document B, script in Document A can send a message to Document B
by calling the '''postMessage''' method
as follows:
|Code=var targetframe {{=}} document.getElementsByTagName('iframe')[0];
targetframe.contentWindow.postMessage('Hello World');
}}{{Single Example
|Language=JavaScript
|Description=The script in Document B can respond to the message
by registering the
[[dom/Element/message|'''onmessage''']] event handler
for incoming messages.
|Code=window.attachEvent('onmessage',function(e) {
    if (e.domain {{=}}{{=}} 'example.com') {
        if (e.data {{=}}{{=}} 'Hello World') {
            e.source.postMessage('Hello');
        } else {
            alert(e.data);
        }
    }
});
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Security Warning:  '''While "*" is a valid value for ''targetOrigin'', set the parameter to the value you expected to receive; otherwise, the security of your message might be compromised.  For more information about this security message, see Section 3.1.2 of the [http://go.microsoft.com/fwlink/?LinkId{{=}}199803 HTML5 Web Messaging] Specification (Editor's Draft) from the World Wide Web Consortium (W3C).
The '''postMessage''' method
allows cooperative text exchange between untrusted modules
from different domains embedded within a page. It does so
by ensuring a consistent and secure process
for text-based data exchange.
When a script invokes this method on a
'''window''' object,
the browser sends an
[[dom/Element/message|'''onmessage''']]
event to the target document
on which the
'''data''' property
has been set to the value passed in
''msg''.
When a target URI is passed into the method, it must have
at least a protocol and a host specified. The message will only be sent if
the target window has the same protocol and host as the specified target 
URI.
The '''postMessage''' method call
does not return until the event listeners of the target document
have finished executing.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging], Section 5.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=postMessage
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=3.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.postMessage postMessage]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/cc197015(v=vs.85).aspx postMessage Method]
|HTML5Rocks_link=
}}