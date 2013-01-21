{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This interface lets a user list files and directories in a directory.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If there are no additions to or deletions from a directory between the first and last call to readEntries, and no errors occur, then:
*A series of calls to readEntries must return each entry in the directory exactly once.
*Once all entries have been returned, the next call to readEntries must produce an empty array.
*If not all entries have been returned, the array produced by readEntries must not be empty.
*The entries produced by readEntries must not include the directory itself ["."] or its parent [".."].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C File API: Directories and System Specification
|URL=http://dev.w3.org/2009/dap/file-system/pub/FileSystem/
|Status=W3C Working Draft
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
{{Topics|FileSystemAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}