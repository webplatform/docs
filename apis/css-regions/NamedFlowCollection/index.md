{{Page_Title|NamedFlowCollection}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
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
{{Notes_Section
|Usage=For any flows in the collection that  disappear when they are no longer assigned to any content, '''item()''' and [[apis/css-regions/NamedFlowCollection/namedItem|'''namedItem()''']] yield '''null'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://www.w3.org/TR/2013/WD-css3-regions-20130528/
|Status=W3C Working Draft 28 May 2013
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
|Topic_clusters=Regions
}}
{{Topics|CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}