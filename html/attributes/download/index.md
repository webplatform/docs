{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies that the target item is to be downloaded for offline viewing.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/a
|Content=If the download attribute is specified on the [[html/elements/a|anchor]] or [[html/elements/area|area]] elements, then the browser will attempt to download the item for viewing later. You can optionally give the attribute a value, which will then have the browser store that file with that filename overriding the resources default name.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<!doctype html>
<title>Download attribute demo</title>
&lt;!-- With the download attribute set and having a value the browser will attempt to save the file as the attribute name, overriding the default resource name of "video.mp4". -->
<a href="http://example.com/path/to/video.mp4" download="Web Platform Introduction.mp4">Download the WPD Introduction Video</a>
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
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}