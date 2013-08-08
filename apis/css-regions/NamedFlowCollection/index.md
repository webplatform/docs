{{Page_Title|NamedFlowCollection}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Static snapshot array of a document's available [[css/concepts/named_flow|named flows]]}}
{{API_Object
|Subclass_of=dom/StaticNodeList
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Retrieve the ''main'' flow from the document, in one method-chained line:
|Code=var flow = document.getNamedFlows().namedItem('main');
}}{{Single Example
|Language=JavaScript
|Description=Same as above, but iterates over the '''NamedFlowCollection''' object represented in a ''flows'' variable:
|Code=var flow;
var flows = document.getNamedFlows();
for (var i = 0; i < flows.length; i++) {
    if (flows[i].name == 'main') {
        flow = flows[i];
        break;
    }
}

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}