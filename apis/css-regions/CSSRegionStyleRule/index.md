{{Page_Title|CSSRegionStyleRule interface}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Represents an [[css/atrules/@region|'''@region''']] rule in a CSS style sheet.}}
{{API_Object
|Subclass_of=css/cssom/CSSRule
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=CSS for following example:
|Code=@region div.region {
    p {
	color: #fff;
        background-color: #000;
    }
}
}}{{Single Example
|Language=JavaScript
|Description=Narrow scope of first rule within @region to first paragraph, and modify background color
|Code=// corresponds to @region rule above:
rule = document.styleSheets[0].cssRules[0];

// modify first nested style's selector:
rule.cssRules[0].selectorText = 'article > p:first-of-type';

// modify first nested style's background-color property:
rule.cssRules[0].style.backgroundColor = '#777';

// inspect first nested style as read-only string:
console.log(rule.cssRules[0].cssText);

// inspect CSS syntax for entire @region rule:
console.log(rule.cssText);
}}{{Single Example
|Language=CSS
|Description='''cssText''' above should now reflect these altered values:
|Code=@region div.region {
    p:first-of-type {
	color: #fff;
        background-color: #777;
    }
}
}}
}}
{{Notes_Section
|Usage='''CSSRegionStyleRule''' supplements the [[css/cssom/CSSRule|'''CSSRule''']] interface.
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
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
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
|External_links=* [http://html.adobe.com/webstandards/cssregions Adobe Web Standards: CSS Regions]
* [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}