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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script shows how to access the list of ranges that have been played.
|LiveURL=
|Code=
var ranges {{=}} document.getElementById('myVideo').played;
for (var i{{=}}0; i&lt;ranges.length; i++)
    var start {{=}} ranges.start(i);
    var end {{=}} ranges.end(i);
    // display results to developer tools console window
    if (window.console.log){ window.console.log("Played from " + start + " to " + end);}
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
A '''IHTMLTimeRanges''' object represents the collection of ranges from the media resource that have been buffered or played. Ranges in a '''IHTMLTimeRanges''' collection are sequential and not empty. Adjacent ranges are combined together to create longer ones.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.11


===Members===
The '''HTMLTimeRanges''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''HTMLTimeRanges''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/audio-video/methods/end|'''end''']]
|Returns the end of the time range by using  the specified index.
|-
|[[apis/audio-video/methods/start|'''start''']]
|Gets the start of the time range by using  the specified index.
|}
 

====Properties====
The '''HTMLTimeRanges''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/length (TimeRanges)|'''length''']]
|The number of time ranges in the collection.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>[[apis/audio-video/properties/buffered|buffered]]</code>
*<code>[[apis/audio-video/properties/played|played]]</code>
*<code>[[apis/audio-video/properties/seekable|seekable]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}