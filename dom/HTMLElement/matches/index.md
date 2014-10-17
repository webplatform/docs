{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=examples, compatibility, general clean-up/review for accuracy
|Checked_Out=No
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns <code>true</code> if an element matches a given selector. Otherwise, <code>false</code>.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=selector
|Data type=String
|Description=This string represents the selector to test the element against. This parameter is required and it must have a length of at least one. An empty string throws the error <code>Dom Exception 12.</code>
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=element
|Return_value_name=result
|Javascript_data_type=DOM Node
|Return_value_description=Returns true if the element matches the given selector or false if it doesn't.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Currently, few browsers support the unprefixed version. It is recommended to use the API as following:

<pre>var docEl = document.documentElement,
    matches = docEl.matches || docEl.webkitMatchesSelector || docEl.mozMatchesSelector || docEl.msMatchesSelector || docEl.oMatchesSelector;
matches.call(element, selector)</pre>
}}
{{Related_Specifications_Section
|Specifications=
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/API/Element.matches
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}