{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
When a webpage is displayed in Windows Internet Explorer 9 mode, Windows Internet Explorer records timestamps that correspond to the time when various steps occurred during the process used to load a document. Each property of the '''performanceTiming''' object corresponds to one of these timestamps.
This object is not supported for Metro style apps using JavaScript.
The built-in performance marks occur in the following order:
*[[apis/timing/properties/navigationStart|'''navigationStart''']]
*[[apis/timing/properties/redirectStart|'''redirectStart''']]
*[[apis/timing/properties/unloadEventStart|'''unloadEventStart''']]
*[[apis/timing/properties/unloadEventEnd|'''unloadEventEnd''']]
*[[apis/timing/properties/redirectEnd|'''redirectEnd''']]
*[[apis/timing/properties/fetchStart|'''fetchStart''']]
*[[apis/timing/properties/domainLookupStart|'''domainLookupStart''']]
*[[apis/timing/properties/domainLookupEnd|'''domainLookupEnd''']]
*[[apis/timing/properties/connectStart|'''connectStart''']]
*[[apis/timing/properties/connectEnd|'''connectEnd''']]
*[[apis/timing/properties/requestStart|'''requestStart''']]
*[[apis/timing/properties/responseStart|'''responseStart''']]
*[[apis/timing/properties/responseEnd|'''responseEnd''']]
*[[apis/timing/properties/domLoading|'''domLoading''']]
*[[apis/timing/properties/domInteractive|'''domInteractive''']]
*[[apis/timing/properties/domContentLoadedEventStart|'''domContentLoadedEventStart''']]
*[[apis/timing/properties/domContentLoadedEventEnd|'''domContentLoadedEventEnd''']]
*[[apis/timing/properties/domComplete|'''domComplete''']]
*[[apis/timing/properties/loadEventStart|'''loadEventStart''']]
*[[apis/timing/properties/loadEventEnd|'''loadEventEnd''']]
*[[apis/timing/properties/msFirstPaint|'''msFirstPaint''']]

The properties of the '''performanceTiming''' object represent the number of milliseconds that have elapsed between midnight January 1, 1970 and the time the measurement was recorded.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_timing\ie]:%20performanceTiming object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}210425 Navigation Timing], Section 4.2


===Members===
The '''performanceTiming''' object has these types of members:
*[#properties Properties]


====Properties====
The '''performanceTiming''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/timing/properties/connectEnd|'''connectEnd''']]
|Gets the time that the user agent finishes establishing the connection to the server to retrieve the current document.
|-
|[[apis/timing/properties/connectStart|'''connectStart''']]
|Gets the time immediately before the user agent starts establishing the connection to the server to retrieve the document.
|-
|[[apis/timing/properties/domainLookupEnd|'''domainLookupEnd''']]
|The [[apis/timing/properties/domainLookupEnd|'''domainLookupEnd''']] property must return the time immediately after the user agent finishes the domain name lookup for the current document. If a persistent connection is used or the current document is retrieved from relevant application caches or local resources, this property must return the same value as [[apis/timing/properties/fetchStart|'''fetchStart''']].
|-
|[[apis/timing/properties/domainLookupStart|'''domainLookupStart''']]
|The [[apis/timing/properties/domainLookupStart|'''domainLookupStart''']] property must return the time immediately before the user agent starts the domain name lookup for the current document. If a persistent connection is used or the current document is retrieved from relevant application caches or local resources, this attribute must return the same value as [[apis/timing/properties/fetchStart|'''fetchStart''']].
|-
|[[apis/timing/properties/domComplete|'''domComplete''']]
|The [[apis/timing/properties/domComplete|'''domComplete''']] property must return the time immediately before the user agent sets the current document readiness to '''complete'''.
|-
|[[apis/timing/properties/domContentLoadedEventEnd|'''domContentLoadedEventEnd''']]
|Returns the time, in milliseconds, immediately after the document's '''DOMContentLoaded''' event completes.
|-
|[[apis/timing/properties/domContentLoadedEventStart|'''domContentLoadedEventStart''']]
|The [[apis/timing/properties/domContentLoadedEventStart|'''domContentLoadedEventStart''']] property must return the time immediately before the user agent fires the '''DOMContentLoaded''' event of the document.
|-
|[[apis/timing/properties/domInteractive|'''domInteractive''']]
|The [[apis/timing/properties/domInteractive|'''domInteractive''']] property must return the time immediately before the user agent sets the current document readiness to '''interactive'''.
|-
|[[apis/timing/properties/domLoading|'''domLoading''']]
|The [[apis/timing/properties/domLoading|'''domLoading''']] property must return the time immediately before the user agent sets the current document readiness to '''loading'''.
|-
|[[apis/timing/properties/fetchStart|'''fetchStart''']]
|Gets the time when the user agent starts fetching the resource.
|-
|[[apis/timing/properties/loadEventEnd|'''loadEventEnd''']]
|The [[apis/timing/properties/loadEventEnd|'''loadEventEnd''']] property must return the time when the load event of the current document is completed. It must return zero when the load event is not fired or is not completed.
|-
|[[apis/timing/properties/loadEventStart|'''loadEventStart''']]
|The [[apis/timing/properties/loadEventEnd|'''loadEventEnd''']] property must return the time immediately before the load event of the current document is fired. It must return zero if the load event has not been fired.
|-
|[[apis/timing/properties/msFirstPaint|'''msFirstPaint''']]
|Gets the time when the document loaded by the '''window''' object began to be displayed to the user.
|-
|[[apis/timing/properties/navigationStart|'''navigationStart''']]
|The [[apis/timing/properties/navigationStart|'''navigationStart''']] property must return the time immediately after the user agent finishes prompting to unload the previous document. If there is no previous document, this property must return the same value as [[apis/timing/properties/fetchStart|'''fetchStart''']].
|-
|[[apis/timing/properties/redirectEnd|'''redirectEnd''']]
|If there are HTTP redirects or equivalent when navigating and all redirects and equivalents are from the same origin, the [[apis/timing/properties/redirectEnd|'''redirectEnd''']] property must return the time immediately after receiving the last byte of the response of the last redirect. Otherwise, this property must return zero.
|-
|[[apis/timing/properties/redirectStart|'''redirectStart''']]
|If there are HTTP redirects or equivalent when navigating and if all the redirects or equivalent are from the same origin, the [[apis/timing/properties/redirectStart|'''redirectStart''']] property must return the starting time of the fetch that initiates the redirect. Otherwise, this attribute must return zero.
|-
|[[apis/timing/properties/requestStart|'''requestStart''']]
|The [[apis/timing/properties/requestStart|'''requestStart''']] property must return the time immediately before the user agent starts requesting the current document from the server, from relevant application caches, or from local resources.
|-
|[[apis/timing/properties/responseEnd|'''responseEnd''']]
|The [[apis/timing/properties/responseEnd|'''responseEnd''']] property must return the time immediately after the user agent receives the last byte of the current document or immediately before the transport connection is closed, whichever comes first. The document here can be received either from the server, relevant application caches, or from local resources.
|-
|[[apis/timing/properties/responseStart|'''responseStart''']]
|The [[apis/timing/properties/responseStart|'''responseStart''']] property must return the time immediately after the user agent receives the first byte of the response from the server, from relevant application caches, or from local resources.
|-
|[[apis/timing/properties/unloadEventEnd|'''unloadEventEnd''']]
|If the previous document and the current document have the same origin, the [[apis/timing/properties/unloadEventEnd|'''unloadEventEnd''']] property must return the time immediately after the user agent finishes the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document, or the unload is not yet completed, this attribute must return zero.
|-
|[[apis/timing/properties/unloadEventStart|'''unloadEventStart''']]
|If the previous document and the current document have the same origin, the [[apis/timing/properties/unloadEventStart|'''unloadEventStart''']] property must return the time immediately before the user agent starts the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document, this attribute must return zero.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}