{{Page_Title|namedItem()}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Retrieve a [[css/concepts/named_flow|named flow]] by its name}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=the name of the named flow
|Optional=No
}}
|Method_applies_to=apis/css-regions/NamedFlowCollection
|Example_object_name=flows
|Return_value_name=flow
|Javascript_data_type=DOM Node
|Return_value_description=the [[apis/css-regions/NamedFlow|'''NamedFlow''']] object that corresponds to the specified name
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Retrieve the ''main'' flow from the document, in one method-chained line:
|Code=var flow = document.getNamedFlows().namedItem('main');
}}
}}
{{Notes_Section
|Usage=The [[apis/css-regions/NamedFlowCollection|'''NamedFlowCollection''']] object is an array snapshot of a document's named flows. This method allows you to access a specific flow directly by its name, rather than by iterating over the array.
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