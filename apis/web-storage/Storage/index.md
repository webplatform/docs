{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=Key names are exposed as properties on this object. For example, the following statements are equivalent:
|LiveURL=
|Code=
sessionStorage.setItem('myKey', '...');
					
sessionStorage['myKey'] {{=}} '...'; 
	
sessionStorage.myKey {{=}} '...'; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Each '''Storage''' object provides access to a list of key/value pairs, which are sometimes called items. Keys are strings, and any string (including the empty string) is a valid key. Items contain values (which are also strings) and associated metadata.
Each '''Storage''' object is associated with a list of key/value pairs when it is created. Multiple '''Storage''' objects, such as two instances of [[apis/web-storage/properties/localStorage|'''localStorage''']], can be associated with the same list of key/value pairs simultaneously.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''HTMLStorage''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''HTMLStorage''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/web-storage/methods/clear|'''clear''']]
|Removes all key/value pairs from the Web Storage area.
|-
|[[apis/web-storage/methods/getItem|'''getItem''']]
|Retrieves the current value associated with the Web Storage key.
|-
|[[apis/web-storage/methods/key|'''key''']]
|Retrieves the key at the specified index in the collection.
|-
|[[apis/web-storage/methods/removeItem|'''removeItem''']]
|Deletes a key/value pair from the Web Storage collection.
|-
|[[apis/web-storage/methods/setItem|'''setItem''']]
|Sets a key/value pair.
|}
 

====Properties====
The '''HTMLStorage''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[apis/web-storage/properties/length|'''length''']]
|Retrieves the length of the key/value list.
|-
|[[apis/web-storage/properties/remainingSpace|'''remainingSpace''']]
|Retrieves the remaining memory space, in bytes, for the storage object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/web-storage/properties/localStorage|localStorage]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}