{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Legacy method. Use [[css/selectors_api/querySelectorAll|document.querySelectorAll("img")]] instead. Gets a live collection of [[html/elements/img|img]] elements in a document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=imageCollection
|Return_value_description=A live collection of [[html/elements/img|img]] elements in the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Logging the source URL of the first image in the document using the legacy property.
|Code=// Caching the collection, instead of looking up the images property every time.
// Alternatively and more efficiently, use document.querySelectorAll("img") here instead.
var imageList = document.images;
// Verifying the collection is not empty.
if (imageList.length) {
  console.log(
    "The source URL of the first image in the document is - " +
    // Getting the src property of the first item in the collection.
    imageList[0].src);
}
}}
}}
{{Notes_Section
|Usage=This is a legacy property. Use [[css/selectors_api/querySelectorAll|document.querySelectorAll("img")]] instead, which returns a static list instead.

Use this property to get a live collection of [[html/elements/img|img]] elements in a document.
|Notes=Since this property returns a live collection, there are performance implications.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#dom-document-images
|Status=Living Standard
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/dom.html#dom-document-images
|Status=Last Call Working Draft
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}