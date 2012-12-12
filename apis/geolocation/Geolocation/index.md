{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The geolocation API is published through a geolocation child object within the navigator object.  If the object exists, geolocation services are available.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=You can test for the presence of geolocation thusly:

<code>
if ("geolocation" in navigator) {
  /* geolocation is available */
} else {
  alert("I'm sorry, but geolocation services are not supported by your browser.");
}
</code>
|Notes====Remarks===
Windows Internet Explorer 9.  The '''geolocation''' object is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
The '''geolocation object''' is not supported for applications hosting the WebBrowser Control.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_geoloc\ie]:%20geolocation object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes====Standards information===
There are no standards that apply here.

===Members===
The '''geolocation''' object has these types of members:
*[#methods Methods]


====Methods====
The '''geolocation''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/geolocation/methods/clearWatch|'''clearWatch''']]
|Stops listening for updates to the current geographical location.
|-
|[[apis/geolocation/methods/getCurrentPosition|'''getCurrentPosition''']]
|Obtains the geographic position, in terms of latitude and longitude coordinates, of the device running Internet Explorer.
|-
|[[apis/geolocation/methods/watchPosition|'''watchPosition''']]
|Begins listening for updates to the current geographical location of the device running the client.
|}
 
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
{{See_Also_Section}}
{{Topics|DOM, Geolocation}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}