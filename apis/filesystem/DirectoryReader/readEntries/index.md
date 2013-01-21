{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Read the next block of entries from this directory.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=successCallback
|Data type=String
|Description=Called once per successful call to readEntries to deliver the next previously-unreported set of Entries in the associated Directory. If all Entries have already been returned from previous invocations of readEntries, successCallback must be called with a zero-length array as an argument.
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=String
|Description=A callback indicating that there was an error reading from the Directory.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/DirectoryReader
|Example_object_name=DirectoryReader
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
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