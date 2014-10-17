{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat and better spec link
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Fires when a message is received from another context (frame, window, worker and similar).}}
{{Event
|Event_applies_to=dom/Window
|Synchronous=No
|Bubbles=No
|Target=dom/Window
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=For example, if document A contains a reference to the [[dom/HTMLIFrameElement/contentWindow|'''contentWindow''']] of document B, script in document A can send document B a message by calling [[dom/Window/postMessage|'''postMessage''']] as follows:
|Code=var o {{=}} document.getElementsByTagName('iframe')[0];
o.contentWindow.postMessage('Hello World');
|LiveURL=
}}{{Single Example
|Language=
|Description=The script in document B can respond to the message by registering the '''onmessage''' event handler for incoming messages.
|Code=window.attachEvent('onmessage',function(e) {
    if (e.domain {{=}}{{=}} 'example.com') {
        if (e.data {{=}}{{=}} 'Hello World') {
            e.source.postMessage('Hello');
        } else {
            alert(e.data);
        }
    }
});
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=For info on channel messaging with [[apis/workers/Worker|'''Workers''']], see [[apis/web-messaging/MessagePort|'''MessagePort''']] and [[apis/web-messaging/MessageChannel|'''MessageChannel''']].
The '''onmessage''' event is fired when script invokes [[dom/Window/postMessage|'''postMessage''']] on a '''window''' object to send the target document a message. The [[dom/MessageEvent/data2|'''data''']] property of the incoming event is set to the value passed in '''postMessage'''.
'''Security Warning:  '''For best results, check the [[dom/MessageEvent/origin|'''origin''']] attribute to ensure that messages are only accepted from domains that you expect. For more information, see Section 7.4.2 of the [http://go.microsoft.com/fwlink/?linkid{{=}}203771 HTML5 (Working Draft)] specification from the World Wide Web Consortium (W3C).
To invoke this event, do one of the following:
*Send a cross-document message with '''postMessage'''.
*Send a message to a '''Worker''' with '''postMessage'''.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLWindowEvents3'''
*[[apis/web-messaging/MessagePort|'''MessagePort''']]
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging], Section 5.3
}}
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}