{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrKey|Data type=BSTR|Description=The name of the key (a valid UTF-16 string, including the empty string).|Optional=}}
{{Method Parameter|Name=bstrValue|Data type=BSTR|Description=The value (a valid UTF-16 string) of the key/value pair.|Optional=}}
|Method_applies_to=apis/web-storage/HTMLStorage
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|E_OUTOFMEMORY
|There is insufficient memory to complete the operation.
|-
|E_ACCESSDENIED
|The operation is not allowed.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|-
|W3CException_DOM_QUOTA_EXCEEDED_ERR
|IE9 mode only. 
The operation would exceed storage limits.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|E_OUTOFMEMORY
|There is insufficient memory to complete the operation.
|-
|E_ACCESSDENIED
|The operation is not allowed.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|-
|W3CException_DOM_QUOTA_EXCEEDED_ERR
|IE9 mode only. 
The operation would exceed storage limits.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code examples are equivalent. The first sets a key/value pair by calling '''setItem'''. The second uses array syntax to find the key in the collection. The final example uses property name syntax to set an expando property.
|LiveURL=
|Code=
sessionStorage.setItem('myKey', '...');
					
sessionStorage['myKey'] {{=}} '...'; 
	
sessionStorage.myKey {{=}} '...'; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
This implementation of '''setItem''' differs from '''setItem''' in return code only. In IE9 mode, this method might also return W3CException_DOM_QUOTA_EXCEEDED_ERR.
Any valid UTF-16 string, including the empty string, is a valid key name. If ''bstrKey'' or ''bstrValue'' are not valid UTF-16 strings, the '''setItem''' method throws an error.
Non-string variable types are automatically type-converted to strings, if possible. Structured data must be converted to a string before storing.
This method first checks if a key/value pair with the specified ''bstrKey'' already exists in the list associated with the object. If not, a new key/value pair with the given value is added to the list. If the key/value pair already exists, the value is updated.
Keys are also available as expando properties on the '''Storage''' object. If the property name does not exist, a key/value pair is created for it. For an illustration of this, see the example below.
If the size of the value is larger than the disk quota remaining for the storage area, an "Out of memory" exception is thrown. If necessary, check [[apis/web-storage/properties/remainingSpace|'''remainingSpace''']] before storing the value.
Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196999 Web Storage], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Storage</code>
*<code>Reference</code>
*<code>[[apis/web-storage/methods/getItem|getItem]]</code>
*<code>[[apis/web-storage/properties/remainingSpace|remainingSpace]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}