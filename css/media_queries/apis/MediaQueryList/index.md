{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The following example displays a message as when the windows size is less or greater than 250 pixels.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199793 CSSOM View Module], Section 4.1


===Members===
The '''MediaQueryList''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''MediaQueryList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/media queries/apis/addListener|'''addListener''']]
|Adds the callback function to the list of listeners for the '''MediaQueryList''' object. The function is called whenever the evaluation of the media query changes.
|-
|[[css/media queries/apis/removeListener|'''removeListener''']]
|Removes the given callback function from the list of listeners for this '''MediaQueryList''' object.
|}
 

====Properties====
The '''MediaQueryList''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/media queries/apis/matches|'''matches''']]
|Returns '''TRUE''' if the list of media queries matches the state of the current window, or '''FALSE''' otherwise.
|-
|[[css/media queries/apis/media|'''media''']]
|Returns the serialized version of the media query list that was used to create the '''MediaQueryList''' (MQL) object.
|}
 

}}
{{See_Also_Section
|Topic_clusters=Media Queries
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}