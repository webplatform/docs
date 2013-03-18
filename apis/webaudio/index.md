{{Page_Title|Web Audio API}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Describes a high-level JavaScript API for processing and synthesizing audio in web applications.}}
{{API_Listing}}
{{Concept_Listing
|Query=[[Category:WebAudio]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=This specification describes a high-level JavaScript API for processing and synthesizing audio in web applications. The primary paradigm is of an audio routing graph, where a number of [[apis/webaudio/AudioNode|'''AudioNode''']] objects are connected together to define the overall audio rendering. The actual processing will primarily take place in the underlying implementation (typically optimized Assembly / C / C++ code), but direct JavaScript processing and synthesis is also supported.

This API is designed to be used in conjunction with other APIs and elements on the web platform, notably: [[apis/xhr/objects/XMLHttpRequest|'''XMLHttpRequest''']] (using the '''responseType''' and '''response''' attributes). For games and interactive applications, it is anticipated to be used with the canvas 2D and WebGL 3D graphics APIs.
}}
{{See_Also_Section
|Topic_clusters=Audio
}}
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}