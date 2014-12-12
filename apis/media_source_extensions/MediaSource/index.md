{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Represents a source of media data (audio or video) for a media element.}}
{{API_Object
|Subclass_of=
|Overview=Provides a buffer based source for a media object. The app creates a MediaSource object and adds it to the media (audio or video) object as a source for the src object. SourceBuffers are then added to the MediaSource object and media content is then appended to the buffers to provide streaming or multi-source playback.

<code>var mediaSource = new MediaSource();</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example creates a new MediaSource object and adds it to a video object. It then adds a sourceBuffer and calls to start loading content. 

The live sample only runs on a browser that support the W3C syntax and MP4 files.
|Code=// Create mediaSource and initialize video 
function setupVideo() {
  //  Create the media source 
  if (window.MediaSource) {
    mediaSource = new window.MediaSource();
  } else {
    log("mediasource or syntax not supported");
    return;
  }
  var url = URL.createObjectURL(mediaSource);
  videoElement.src = url;

  // Wait for event that tells us that our media source object is 
  //   ready for a buffer to be added.
  mediaSource.addEventListener('sourceopen', function (e) {
    try {
      videoSource = mediaSource.addSourceBuffer('video/mp4');
      //  initialize and start loading segments of video           
    } catch (e) {
      //  error reporting here
      return;
    }
  });
}
|LiveURL=http://code.webplatform.org/gist/9144919/
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Media Source Extensions
|URL=http://www.w3.org/TR/media-source/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Multimedia
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



}





}