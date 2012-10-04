{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=first|Data type=Any|Description=|Optional=}}
{{Method Parameter|Name=second|Data type=Any|Description=|Optional=}}
{{Method Parameter|Name=result|Data type=Number|Description=
Value
Meaning




-1



The first value is less than the second value.






0



The values are equal.






1



The first value is greater than the second value.


|Optional=}}
|Method_applies_to=apis/indexedDB/IDBFactory
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.



This method can throw the following [[dom/DOMException|'''DOMException''']] exceptions:

'''Note'''  As of Internet Explorer 10, the [[dom/properties/code|'''code''']] property is deprecated in lieu of the [[dom/properties/toString (DOMError)|'''name''']] property, which is preferred for standards compliance and future compatibility.

{| class="wikitable"
|-
!Exception properties
!Description
|-
|name: DataError
|A specified value is not valid or cannot be compared.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=
|LiveURL=
|Code=
var value1 {{=}} "Alpha";
var value2 {{=}} "Beta";
var result {{=}} window.indexedDB.cmp( value1, value2 );
comsole.log( "Comparison results: " + result );
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/indexedDB/properties/indexedDB|indexedDB]]</code>
*<code>[[apis/indexedDB/IDBFactory|IDBFactory]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}