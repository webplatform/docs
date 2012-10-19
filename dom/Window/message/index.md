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
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=For example, if document A contains a reference to the [[dom/properties/contentWindow|'''contentWindow''']] of document B, script in document A can send document B a message by calling [[apis/web-messaging/methods/postMessage (window)|'''postMessage''']] as follows:
|LiveURL=
|Code=
var o {{=}} document.getElementsByTagName('iframe')[0];
o.contentWindow.postMessage('Hello World');
}}
{{Single_Example
|Description=The script in document B can respond to the message by registering the '''onmessage''' event handler for incoming messages.
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
For info on channel messaging with [[apis/workers/objects/Worker|'''Workers''']], see [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] and [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
The '''onmessage''' event is fired when script invokes [[apis/web-messaging/methods/postMessage (window)|'''postMessage''']] on a '''window''' object to send the target document a message. The [[dom/properties/data2|'''data''']] property of the incoming event is set to the value passed in '''postMessage'''.
'''Security Warning:  '''For best results, check the [[dom/properties/origin2|'''origin''']] attribute to ensure that messages are only accepted from domains that you expect. For more information, see Section 7.4.2 of the [http://go.microsoft.com/fwlink/?linkid{{=}}203771 HTML5 (Working Draft)] specification from the World Wide Web Consortium (W3C).
To invoke this event, do one of the following:
*Send a cross-document message with [[apis/web-messaging/methods/postMessage (window)|'''postMessage''']].
*Send a message to a [[apis/workers/objects/Worker|'''Worker''']] with [[apis/web-messaging/methods/postMessage (window)|'''postMessage''']].

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLWindowEvents3'''
*[[apis/web-messaging/objects/MessagePort|'''MessagePort''']]

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging], Section 5.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}