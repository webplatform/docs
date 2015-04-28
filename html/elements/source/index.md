{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Allows developer to specify multiple alternative media resources for media elements, such as <code><video></code> and <code><audio></code>. It does not represent anything on its own, and is used with <code>src</code> attribute to specify the URL.}}
{{Markup_Element
|DOM_interface=dom/HTMLSourceElement
|Tag_omissions=required
|CSS_display=none
|Content=== Attributes ==

* <code>src</code> =  URL potentially surrounded by spaces<br />The address of the media source.
* <code>type</code> = MIME type<br />The type of the media source (used for helping the UA determine, before fetching this media source, if it can play it).<br />A string that identifies a valid MIME media type, as defined in [RFC2046].
* <code>media</code> = media-query list<br />The intended media type of the media source (used for helping the UA determine, before fetching this media source, if it is useful to the user).<br />A valid media query list, as defined in [MediaQueries].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<nowiki><video controls="controls">
 <source src="http://media.w3.org/2010/05/sintel/trailer.mp4"
         type='video/mp4; codecs="avc1, mp4a"/>
 <source src="http://media.w3.org/2010/05/sintel/trailer.ogv"
         type='video/ogg; codecs="theora, vorbis"/>
 <p>Your user agent does not support the HTML5 Video element.</p>
</video></nowiki>
|LiveURL=http://test.w3.org/html/examples/elements/source/source01.html
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  If you change the media file using the [[apis/audio-video/properties/src|'''src''']] property on an '''audio''' or '''video''' object, you need to call the [[apis/audio-video/methods/load|'''load''']] method before calling the [[apis/audio-video/methods/play|'''play''']] method. If you change the '''src''' and call the play() method without loading first, it will continue to play the file specified by the '''source''' element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-source-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-source-element
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>audio</code>
*<code>video</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}