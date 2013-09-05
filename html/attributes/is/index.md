{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Describes the base element from which the element with this attribute is extended.}}
{{Markup_Attribute
|Applies_to=dom/HTMLElement
|Property_applies_to=dom/HTMLElement
|Content=Extending an element with [[dom/document/createElement|document.createElement]] creates a new element. To use that element in markup, you must describe the element with a tag and include the <code>is=''</code> attribute with the value of the base element from which the new element is extended. See examples.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Markup for an extended element.
|Code=<button is="mega-button">
}}{{Single Example
|Language=JavaScript
|Description=Creates the custom element 'mega-button', which is extended from the 'button' element.
|Code=var megaButton = document.createElement('button', 'mega-button');
// megaButton instanceof MegaButton === true
}}
}}
{{Notes_Section
|Usage=The extended element name must contain at least one dash (-). So for example, <x-foo>, <foo-element>, and <my-foo-element> are valid names, while <tabs> and <foo_bar> are not.
|Notes=The custom element name must not be one of the following existing hyphen-containing element names:
* annotation-xml
* color-profile
* font-face
* font-face-src
* font-face-uri
* font-face-format
* font-face-name
* missing-glyph
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Custom Elements
|URL=https://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/custom/index.html
|Status=Working draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Web Components
|External_links=See [http://www.html5rocks.com/en/tutorials/webcomponents/customelements/ Custom Elements] on [http://www.html5rocks.com HTML5Rocks!].
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webcomponents/customelements/ Custom Elements
}}