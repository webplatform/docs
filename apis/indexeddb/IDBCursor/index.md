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
{{Notes_Section
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


===Members===
The '''IDBCursor''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''IDBCursor''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/indexedDB/methods/advance|'''advance''']]
|Advances the position of a cursor forward by a specified number of records.
|-
|[[apis/indexedDB/methods/continue|'''continue''']]
|Advances the position of cursor object to the next object.
|-
|[[apis/indexedDB/methods/openCursor|'''openCursor''']]
|Returns a cursor object positioned at the first record object in a data source, optionally filtered by a key range and ordered by a direction.
|-
|[[apis/indexedDB/methods/update|'''update''']]
|Updates a value in the current record of the cursor.
|}
 

====Properties====
The '''IDBCursor''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/indexedDB/properties/direction|'''direction''']]
|Indicates the direction of traversal within a '''cursor'''.
|-
|[[apis/indexedDB/properties/key|'''key''']]
|The key value for the record currently displayed by the cursor.
|-
|[[apis/indexedDB/properties/primaryKey|'''primaryKey''']]
|Returns the value of the primary key associated with a record.
|-
|[[apis/indexedDB/properties/source|'''source''']]
|Returns a reference to the source of a request, such as an object store or a cursor.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_idxdb\ie]:%20IDBCursor object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}