{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]


===Members===
The '''IDBDatabase''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''IDBDatabase''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/indexedDB/methods/close|'''close''']]
|Closes the connection to a database.
|-
|[[apis/indexedDB/methods/createObjectStore|'''createObjectStore''']]
|Creates an object store.
|-
|[[apis/indexedDB/methods/deleteObjectStore|'''deleteObjectStore''']]
|Deletes an object store (and associated indexes) from the database.
|-
|[[apis/indexedDB/methods/setVersion|'''setVersion''']]
|Obsolete.  No longer supported.
|-
|[[apis/indexedDB/methods/transaction|'''transaction''']]
|Begins a transaction for the specified object stores.
|}
 

====Properties====
The '''IDBDatabase''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/indexedDB/properties/objectStoreNames|'''objectStoreNames''']]
|Returns the names of object stores  associated with a database.
|-
|[[apis/indexedDB/events/onerror|'''onerror''']]
|Defines a function handler that is executed when an error is encountered during a request, a transaction, or other database operation.
|-
|[[apis/indexedDB/properties/version|'''version''']]
|Gets the version of the database.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_idxdb\ie]:%20IDBDatabase object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
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