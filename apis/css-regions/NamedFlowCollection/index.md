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
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}