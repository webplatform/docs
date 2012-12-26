{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A metadata index to a referenced object store.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


===Members===
The '''IDBIndex''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''IDBIndex''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/indexedDB/methods/count|'''count''']]
|Returns the number of records in an object store corresponding to a key value or key range.
|-
|[[apis/indexedDB/methods/get|'''get''']]
|Retrieves a record from an object store.
|-
|[[apis/indexedDB/methods/getKey|'''getKey''']]
|Retrieves the key value from an index.
|-
|[[apis/indexedDB/methods/openCursor|'''openCursor''']]
|Returns a cursor object positioned at the first record object in a data source, optionally filtered by a key range and ordered by a direction.
|-
|[[apis/indexedDB/methods/openKeyCursor|'''openKeyCursor''']]
|Returns a set of records, organized by the index, optionally matching values specified by a key range and matching a specified direction.
|}
 

====Properties====
The '''IDBIndex''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/indexedDB/properties/name|'''name''']]
|The name of an object store, index, or other database object.
|-
|[[apis/indexedDB/properties/objectStore|'''objectStore''']]
|A reference to the object store associated with the index.
|-
|[[apis/indexedDB/properties/unique|'''unique''']]
|Indicates whether the index allows duplicate key values.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_idxdb\ie]:%20IDBIndex object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
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
{{Topics|IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}