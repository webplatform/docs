{{Page_Title|TimeRanges}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|A TimeRanges object represents the collection of ranges (time periods) from the media resource that have been buffered or played. Ranges in a TimeRanges collection are sequential and not empty. Adjacent ranges are combined together to create longer ones.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Description=The following script shows how to access the list of ranges that have been played.
|Code=var ranges {{=}} document.getElementById('myVideo').played;
for (var i{{=}}0; i&lt;ranges.length; i++)
    var start {{=}} ranges.start(i);
    var end {{=}} ranges.end(i);
    // display results to developer tools console window
    if (window.console.log){ window.console.log("Played from " + start + " to " + end);}
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5 Specification
|URL=http://dev.w3.org/html5/spec/single-page.html
|Status=W3C Editor's Draft
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
{{Topics|Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
}






}}