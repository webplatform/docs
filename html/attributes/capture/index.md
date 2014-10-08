{{Page_Title|capture}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|HTML Media Capture}}
{{Summary_Section|The capture attribute facilitates user access to a device's media capture mechanism, such as a camera, or microphone, from within a file upload control, for capturing media on the spot.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLInputElement|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=The capture attribute is a boolean attribute that, if specified, indicates that the capture of media directly from the device's environment using a media capture mechanism is preferred.

The capture attribute applies to input elements when the type attribute's value is file and its accept attribute is specified. If the accept attribute's value is set to a MIME type that has no associated capture control type, the user agent acts as if there was no capture attribute.

The media capture mechanism builds upon the security and privacy protections provided by the <input type="file"> and the File API specifications; in particular, any offer to start capturing content from the user’s device requires a specific user interaction on an HTML element that is entirely controlled by the user agent.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Indicates that image files are accepted to be captured.
|Code=<input type="file" accept="image/*" capture>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Indicates that video files are accepted to be captured.
|Code=<input type="file" accept="video/*" capture>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Indicates that audio files are accepted to be captured.
|Code=<input type="file" accept="audio/*" capture>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=To take a picture using the device's camera, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="image" accept="image/*" capture>
  <input type="submit" value="Upload">
</form>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=To capture a video using the device's local video camera, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="video" accept="video/*" capture>
  <input type="submit" value="Upload">
</form>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=To capture audio using the device's local microphone, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="audio" accept="audio/*" capture>
  <input type="submit" value="Upload">
</form>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML Media Capture
|URL=http://www.w3.org/TR/html-media-capture/#the-capture-attribute
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Mobile
|Manual_links=
|External_links=* [http://www.w3.org/TR/html-media-capture/ HTML Media Capture - W3C Page]
* [http://dev.opera.com/articles/view/media-capture-in-mobile-browsers/ Article on Dev.Opera - 26 September 2013]
* [http://www.w3.org/TR/2013/CR-html-media-capture-20130509/ HTML Media Capture - W3C Candidate Recommendation 09 May 2013]
* [http://www.w3.org/2009/dap/ Device APIs working group]
* [http://www.w3.org/wiki/Media_Capture Media Capture Wiki]
|Manual_sections=
}}
{{Topics|Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
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