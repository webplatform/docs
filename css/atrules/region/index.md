{{Page_Title|@region}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Applies CSS styles to portions of content as it appears when flowing within a specified set of ''regions''.}}
{{CSS_At_Rule
|Content=The basic syntax is as follows:

 @region &lt;region_selector> {
     &lt;content_selector> {
         /* ... CSS properties ... */
     }
 }

The ''region_selector'' specifies a set of region elements. Within that scope, the ''content_selector'' applies to any [[/dom/apis/range|''range'']] of the selected content when it appears within each region. This example produces the following result:

 /* default paragraph text */
 p { color: gray: }
 
 /* customized for fragments that appear within region */
 @region-style #intro {
     p { color: blue; }
 }

[[File:regionRule2.jpeg]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Inverts paragraph text within the first region
|Code=/* dark gray text color by default */
p {
    color: #444;
}

/* dark gray background for first region */
div.region:first-of-type {
    background-color: #444;
}

/* white text only within first region */
@region div.region:first-of-type {
    p {
        color: #fff;
    }
}

/* associate content with CSS regions */
article.content { flow-into: main; }
div.region { flow-from: main; }
}}
}}
{{Notes_Section
|Usage=The '''@region''' rule does not change the cascading order of content selectors.

Use the [[css/cssom/CSSRegionStyleRule|'''CSSRegionStyleRule''']] interface to apply '''@region''' rules programmatically.
|Notes=Only the following set of CSS properties work within '''@region''' rules:

* font properties ([[css/properties/font-weight|'''font-weight''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-variant|'''font-variant''']], [[css/properties/font-style|'''font-style''']], [[css/properties/font-family|'''font-family''']])
* [[css/properties/color|'''color''']]
* [[css/properties/opacity|'''opacity''']]
* background properties ([[css/properties/background-color|'''background-color''']], [[css/properties/background-image|'''background-image''']])
* alignment and justification properties ([[css/properties/text-align|'''text-align''']], [[css/properties/text-align-last|'''text-align-last''']], [[css/properties/word-spacing|'''word-spacing''']], [[css/properties/text-justify|'''text-justify''']])
* [[css/properties/letter-spacing|'''letter-spacing''']]
* [[css/properties/text-decoration|'''text-decoration''']]
* [[css/properties/text-transform|'''text-transform''']]
* [[css/properties/line-height|'''line-height''']]
* border properties ([[css/properties/border-color|'''border-color''']], [[css/properties/border-style|'''border-style''']], [[css/properties/border-width|'''border-width''']])
* [[css/properties/border-radius|'''border-radius''']]
* border image properties: ([[css/properties/border-image-source|'''border-image-source''']], [[css/properties/border-image-slice|'''border-image-slice''']], [[css/properties/border-image-width|'''border-image-width''']], [[css/properties/border-image-outset|'''border-image-outset''']], [[css/properties/border-image-repeat|'''border-image-repeat''']])
* [[css/properties/margin|'''margin''']]
* [[css/properties/padding|'''padding''']]
* [[css/properties/text-shadow|'''text-shadow''']]
* [[css/properties/box-shadow|'''box-shadow''']]
* [[css/properties/box-decoration-break|'''box-decoration-break''']]
* [[css/properties/width|'''width''']]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=534
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}