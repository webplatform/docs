{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a new SourceBuffer and adds it to the SourceBuffers property of the MediaSource.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
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
|Code=<syntaxhighlight>
// Create mediaSource and initialize video 
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
  },false);
}</syntaxhighlight>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=Exceptions:

INVALID_ACCESS_ERR  If type is null or an empty string.
 
NOT_SUPPORTED_ERR  If type contains a MIME type that's not supported or a MIME type that's not supported by SourceBuffer.
 
QUOTA_EXCEEDED_ERR  If the mediaSource can't handle any more SourceBuffer objects.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=34
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE11
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}