{{Page_Title|MediaStream Recording}}
{{Flags
|Checked_Out=Yes
|Editorial notes={{Editorial
| this article is currently being worked on
}}
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Allows users to record camera/microphone's streams}}
{{API_Listing}}
{{Concept_Listing
|Query=[[Category:Media_Recorder]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=This API attempts to make basic recording very simple, while still allowing for more complex use cases. In the simplest case, the application instantiates the MediaRecorder object, calls record() and then calls stopRecord() or waits for the MediaStream to be ended. The contents of the recording will be made available in the platform's default encoding via the dataavailable event. Functions are available to query the platform's available set of encodings, and to select the desired ones if the author wishes. The application can also choose how much data it wants to receive at one time. By default a Blob containing the entire recording is returned when the recording finishes. However the application can choose to receive smaller buffers of data at regular intervals.
}}
{{See_Also_Section
|Topic_clusters=Mobile
|External_links=* [http://www.w3.org/TR/mediastream-recording/ MediaStream Recording]
* [http://www.w3.org/TR/2013/WD-mediastream-recording-20130205/ MediaStream Recording - W3C Working Draft 05 February 2013]
* [http://www.w3.org/2009/dap/ Device APIs working group]
* [http://www.w3.org/wiki/Media_Capture Media Capture Wiki]
}}
{{Topics|API, JavaScript, Mobile, Media Recorder}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}