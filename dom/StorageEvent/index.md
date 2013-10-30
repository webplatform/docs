{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example demonstrates how to respond to storage events.
|Code=function reportStorage(evt) {
    alert("Storage was updated for " + evt.url);
}
window.onload {{=}} function() {
    window.addEventListener('storage',reportStorage,false);
    window.sessionStorage.setItem('key','value');
}
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 5.11.1.5


===Members===
The '''StorageEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''StorageEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initEvent|'''initEvent''']]
|Initializes a new generic event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[apis/web-storage/methods/initStorageEvent|'''initStorageEvent''']]
|Initializes a new DOM storage event  that the [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/preventDefault|'''preventDefault''']]
|Cancels the default action of an event.
|-
|[[dom/methods/stopImmediatePropagation|'''stopImmediatePropagation''']]
|Prevents any further propagation of an event.
|-
|[[dom/methods/stopPropagation|'''stopPropagation''']]
|Prevents propagation of an event beyond the current target.
|}
 

====Properties====
The '''StorageEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/bubbles|'''bubbles''']]
|Gets a value that  indicates whether an event propagates up from the event target.
|-
|[[dom/properties/cancelable|'''cancelable''']]
|Gets a value that indicates whether you can cancel an event's default action.
|-
|[[dom/methods/cancelBubble|'''cancelBubble''']]
|Gets or sets a value that indicates whether an event should be stopped from propagating up from the current target.
|-
|[[dom/properties/currentTarget|'''currentTarget''']]
|Gets the event target that is currently being processed.
|-
|[[dom/properties/defaultPrevented|'''defaultPrevented''']]
|Gets a value that indicates whether the default action should be canceled.
|-
|[[dom/properties/eventPhase|'''eventPhase''']]
|Gets the event phase that is being evaluated.
|-
|[[dom/properties/isTrusted|'''isTrusted''']]
|Gets a value that indicates whether a trusted event source created an event.
|-
|[[apis/web-storage/properties/key|'''key''']]
|Gets  the key that  is  updated.
|-
|[[apis/web-storage/properties/newValue|'''newValue''']]
|Gets  the new value of the [[apis/web-storage/methods/key|'''key''']].
|-
|[[apis/web-storage/properties/oldValue|'''oldValue''']]
|Gets  the previous value of the [[apis/web-storage/methods/key|'''key''']].
|-
|[[dom/properties/srcElement|'''srcElement''']]
|Gets the element that the event was originally dispatched to. Compare to [[dom/properties/target|'''target''']].
|-
|[[apis/web-storage/properties/storageArea|'''storageArea''']]
|Gets  the '''Storage''' object of the  affected document.
|-
|[[dom/properties/target|'''target''']]
|Gets the element that is the target of the event.
|-
|[[dom/properties/timeStamp|'''timeStamp''']]
|Gets the time, in milliseconds, when an event occurred.
|-
|[[dom/properties/type (event)|'''type''']]
|Gets the name of an event.
|-
|[[apis/web-storage/properties/url|'''url''']]
|Gets  the address of the document that  the update affects.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/events/storage|onstorage]]</code>
*<code>[[apis/web-storage/properties/localStorage|localStorage]]</code>
*<code>[[apis/web-storage/properties/sessionStorage|sessionStorage]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}