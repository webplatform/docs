{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|MediaSource}}
{{Summary_Section|Represents a source of media data (audio or video) for a media element. }}
{{API_Object
|Overview=Provides a buffer based source for a media object. The app creates a MediaSource object and adds it to the media (audio or video) object as a source for the src object. SourceBuffers are then added to the MediaSource object and media content is then appended to the buffers to provide streaming or multi-source playback.

<code>var mediaSource = new MediaSource();</code> 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example creates a new MediaSource object and adds it to a video object. It then adds a sourceBuffer and calls to start loading content. 

The link below goes to a sample that runs only on browser that support the W3C syntax and MP4 files. 
|Code=
// Create mediaSource and initialize video 
function setupVideo() {
  clearLog(); // Clear console log

  //  Create the media source 
  if (window.MediaSource) {
    mediaSource = new window.MediaSource();
    //  mediaSource = new (window.MediaSource || window.WebKitMediaSource)();
  } else {
    log("mediasource or syntax not supported");
    return;
  }
//      mediaSource = new (window.MediaSource || window.WebKitMediaSource)();
  var url = URL.createObjectURL(mediaSource);
  videoElement.pause();
  videoElement.src = url;
  videoElement.width = width;
  videoElement.height = height;

  // Wait for event that tells us that our media source object is 
  //   ready for a buffer to be added.
  mediaSource.addEventListener('sourceopen', function (e) {
    try {
      videoSource = mediaSource.addSourceBuffer('video/mp4');
      initVideo(initialization, file);           
    } catch (e) {
      log('Exception calling addSourceBuffer for video', e);
      return;
    }
  },false);

}

|LiveURL=http://samples.msdn.microsoft.com/Workshop/samples/media/mpdExampleWP.html
}}
}}
{{Notes_Section}}
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
{{See_Also_Section
|Topic_clusters=Multimedia
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}