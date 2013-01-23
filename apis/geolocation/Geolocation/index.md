{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The geolocation API is published through a Geolocation child object within the navigator object.  If the object exists, geolocation services are available.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=You can test for the presence of geolocation thusly:

<code>
if ("geolocation" in navigator) {
  /* geolocation is available */
} else {
  alert("I'm sorry, but geolocation services are not supported by your browser.");
}
</code>
|Notes=Windows Internet Explorer 9.  The '''geolocation''' object is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
The '''geolocation object''' is not supported for applications hosting the WebBrowser Control.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Geolocation Specification
|URL=http://dev.w3.org/geo/api/spec-source.html
|Status=W3C Proposed Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Geolocation}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}