{{Page_Title|capture}}
{{Flags
|Checked_Out=Yes
|Editorial notes=this article is currently being worked on
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The capture attribute is a boolean attribute that, if specified, indicates that the capture of media directly from the device's environment using a media capture mechanism is preferred.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLInputElement|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Indicates that image files are accepted to be captured.
|Code=<input type="file" accept="image/*" capture>
}}{{Single Example
|Language=HTML
|Description=Indicates that video files are accepted to be captured.
|Code=<input type="file" accept="video/*" capture>
}}{{Single Example
|Language=HTML
|Description=Indicates that audio files are accepted to be captured.
|Code=<input type="file" accept="audio/*" capture>
}}{{Single Example
|Language=HTML
|Description=To take a picture using the device's camera, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="image" accept="image/*" capture>
  <input type="submit" value="Upload">
</form>
}}{{Single Example
|Language=HTML
|Description=To capture a video using the device's local video camera, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="video" accept="video/*" capture>
  <input type="submit" value="Upload">
</form>
}}{{Single Example
|Language=HTML
|Description=To capture audio using the device's local microphone, and upload the picture taken using an HTML form.
|Code=<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="audio" accept="audio/*" capture>
  <input type="submit" value="Upload">
</form>
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
|Topic_clusters=HTML, Mobile
}}
{{Topics|Mobile, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}