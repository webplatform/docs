{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the ID of the given track. This is the ID that can be used with a fragment identifier if the format supports the Media Fragments URI syntax, and that can be used with the getTrackById() method.}}
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
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=(function () {
    // grab the video element
    var video = document.getElementById("video");

    video.addEventListener("loadeddata", function () {

        // get the audiotracks from the video when it's loaded
        var audioTracks = video.audioTracks;

        var tracksSelection = document.getElementById("tracksSelection");

        // loop through the audio tracks
        for (var i = 0; i < audioTracks.length; i++) {
                    
            // create options for the dropdownlist with the id's
            // and languages of the tracks
            var opt = document.createElement('option');
            opt.value = audioTracks[i].id;
            opt.text = audioTracks[i].language;

            tracksSelection.add(opt);
        }
    });

    tracksSelection.addEventListener("change", function (e) {
        // when the item of the dropdownlist changes
        // grab the id from the selected option
        var audioTracks = video.audioTracks;
        var track = audioTracks.getTrackById(e.currentTarget.value);

        //disable all tracks to prevent them from playing all at once
        for (var i = 0; i < audioTracks.length; i++) {
            audioTracks.enabled = false;
        }

        //set the selected track for the video
        track.enabled = true;
    });
})();
|LiveURL=http://code.webplatform.org/gist/459f1a0ea9f70009b6fe
}}
}}
{{Notes_Section
|Usage=
|Notes=
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