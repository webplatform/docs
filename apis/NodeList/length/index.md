{{Page_Title|length}}
{{Flags
|State=Not Ready
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The number of nodes in the list.}}
{{API_Object_Property
|Property_applies_to=dom/NodeList
|Read_only=Yes
|Example_object_name=list
|Return_value_name=
|Javascript_data_type=unsigned long
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<!-- Three divs -->
<ul>
	<li class="fruit">Apple</li>
	<li class="fruit">Banana</li>
	<li class="fruit">Cherry</li>
</ul>
<div id="fruit"></div>

<script>
	// Query the DOM for the nodes with the class 'fruit'
	var fruitNodes = document.querySelectorAll('.fruit');
	
	// Get the number of nodes found by using 'length'
	var fruitNodeCount = fruitNodes.length;
	
	// Displaying the value in the DOM
	document.getElementById('fruit').innerHTML = 'Number of fruit nodes: ' + fruitNodeCount;

// Number of fruit nodes: 3
</script>
|LiveURL=http://result.webplatformstaging.org/gist/66472399f3509d96204a/37c44f44eee101bcc19487fd1cf470e8a5c998d8
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/level-one-core.html#ID-536297177
|Status=Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=DOM
|URL=http://www.w3.org/TR/dom/#nodelist
|Status=Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}