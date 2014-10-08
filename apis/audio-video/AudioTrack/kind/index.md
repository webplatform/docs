{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the category the given track falls into.}}
{{API_Object_Property
|Property_applies_to=apis/audio-video/AudioTrack
|Read_only=Yes
|Example_object_name=AudioTrack
|Return_value_name=
|Javascript_data_type=String
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes===Possible values==

:"alternative": A possible alternative to the main track, e.g. a different take of a song (audio), or a different angle (video).  
::''Applies To'': Audio and video.  
"captions"  
	A version of the main video track with captions burnt in. (For legacy content; new content would use text tracks.)  
	Applies To: Video only.  
"descriptions"  
	An audio description of a video track. 
	Applies To: Audio only.  
"main"  
	The primary audio or video track.  
	Applies To: Audio and video.  
"main-desc"  
	The primary audio track, mixed with audio descriptions.  
	Applies To: Audio only.  
"sign"  
	A sign-language interpretation of an audio track.  
	Applies To: Video only.  
"subtitles"  
	A version of the main video track with subtitles burnt in. (For legacy content; new content would use text tracks.)  
	Applies To: Video only.  
"translation"  
	A translated version of the main audio track.  
	Applies To: Audio only.  
"commentary"  
	Applies To: Commentary on the primary audio or video track, e.g. a director's commentary.  
	Applies To: Audio and video.  
"" (empty string)  
	No explicit kind, or the kind given by the track's metadata is not recognised by the user agent.  
	Applies To: Audio and video.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5 Specification
|URL=http://dev.w3.org/html5/spec/single-page.html
|Status=W3C Editor's Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Audio, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}