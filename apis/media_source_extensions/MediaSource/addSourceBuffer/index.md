{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a new SourceBuffer and adds it to the SourceBuffers property of the MediaSource.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=MIME type
|Data type=String
|Description=The MIME type. This is expressed typically as 'video/mp4' or optionally as a MIME type and a codec: 'video/mp4;codecs=avc1.4d0020,mp4a.40.2'. Internet Explorer accepts both formats, though other browsers may require the codec be included.
|Optional=No
}}
|Method_applies_to=apis/media_source_extensions/MediaSource
|Example_object_name=MediaSource
|Return_value_name=sourcebuffer
|Javascript_data_type=Object
|Return_value_description=Type: SourceBuffer
The media source buffer. 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example gets a video object, creates a new MediaSource object, and assigns the MediaSource object to the src (source) of the video object. It then waits for the sourceopen event to fire, and then creates a video SourceBuffer using addSourceBuffer.
|Code=// Create mediaSource and initialize video 
function setupVideo() {
  clearLog(); // Clear console log

  //  Create the media source 
  if (window.MediaSource) {
    mediaSource = new window.MediaSource();
   } else {
    log("mediasource or syntax not supported");
    return;
  }
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

|LiveURL=http://code.webplatform.org/gist/9144919/
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
{{Topics|Media}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|HTML5Rocks_link=
}}