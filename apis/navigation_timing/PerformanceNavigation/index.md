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
The '''performanceNavigation''' object provides two attributes:
*[[apis/timing/properties/type|'''type''']]
*[[apis/timing/properties/redirectCount|'''redirectCount''']]

The [[apis/timing/objects/performanceTiming|'''performanceTiming''']] object is created when a page navigation occurs. You can get a reference to the '''performanceTiming''' object by calling the [[apis/timing/properties/performance|'''performance''']].[[apis/timing/properties/timing|'''timing''']] property.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_timing\ie]:%20PerformanceNavigation object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}210425 Navigation Timing], Section 4.3


===Members===
The '''PerformanceNavigation''' object has these types of members:
*[#properties Properties]


====Properties====
The '''PerformanceNavigation''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/timing/properties/redirectCount|'''redirectCount''']]
|The [[apis/timing/properties/redirectCount|'''redirectCount''']] property must return the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, this property must return zero.
|-
|[[apis/timing/properties/type|'''type''']]
|The [[apis/timing/properties/type|'''type''']] property must return the type of the last non-redirect navigation in the current browsing context.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}