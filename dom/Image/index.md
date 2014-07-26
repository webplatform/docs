{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Proper syntax and parameters
http://www.w3.org/html/wg/drafts/html/CR/embedded-content-0.html#dom-image
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Legacy. Use [[dom/Document/createElement|document.createElement("img")]] instead. Quickly constructs an [[html/elements/img|'''img''']] element.}}
{{API_Object
|Subclass_of=
|Overview=A shorter legacy constructor for creating and loading images.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script creates a new image and appends it to the '''body''' element.
|Code=var img {{=}} new Image(50, 50);
img.src {{=}} "image.png";
document.body.appendChild(img);
}}
}}
{{Notes_Section
|Usage=Use this constructor as a shorter way to instantiate new [[html/elements/img|'''img''']] elements before adding them to the document.

Syntax -

<code>new Image({{!((}}width{{!)}}, height{{!)}})</code>

You can specify up to two optional arguments:
{{{!}} class="wikitable"
{{!}}-
{{!}}width
{{!}}Optional. '''Integer''' that specifies the '''img''' width.
{{!}}-
{{!}}height
{{!}}Optional. '''Integer''' that specifies the '''img''' height.
{{!}}}
|Notes=The loading process of the image starts as soon as its '''src''' property is set, even when not added to a document.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/embedded-content.html#the-img-element
|Status=Living Standard
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element
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