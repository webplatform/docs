{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates or looks up a file.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=path
|Data type=String
|Description=Either an absolute path or a relative path from this DirectoryEntrySync to the file to be looked up or created. It is an error to attempt to create a file whose immediate parent does not yet exist.
|Optional=No
}}{{Method Parameter
|Name=options
|Data type=String
|Description=*If create and exclusive are both true and the path already exists, getFile must fail.
*If create is true, the path doesn't exist, and no other error occurs, getFile must create it as a zero-length file and return a corresponding FileEntry.
*If create is not true and the path doesn't exist, getFile must fail.
*If create is not true and the path exists, but is a directory, getFile must fail.
*Otherwise, if no other error occurs, getFile must return a FileEntrySync corresponding to path.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/DirectoryEntrySync
|Example_object_name=DirectoryEntrySync
|Return_value_description=FileEntrySync
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