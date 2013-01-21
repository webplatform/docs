{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates or looks up a directory.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=path
|Data type=String
|Description=Either an absolute path or a relative path from this DirectoryEntry to the directory to be looked up or created. It is an error to attempt to create a directory whose immediate parent does not yet exist.
|Optional=No
}}{{Method Parameter
|Name=options
|Data type=String
|Description=*If create and exclusive are both true and the path already exists, getDirectory must fail.
*If create is true, the path doesn't exist, and no other error occurs, getDirectory must create and return a corresponding DirectoryEntry.
*If create is not true and the path doesn't exist, getDirectory must fail.
*If create is not true and the path exists, but is a file, getDirectory must fail.
*Otherwise, if no other error occurs, getDirectory must return a DirectoryEntry corresponding to path.
|Optional=Yes
}}{{Method Parameter
|Name=successCallback
|Data type=String
|Description=A callback that is called to return the DirectoryEntry selected or created.
|Optional=Yes
}}{{Method Parameter
|Name=errorCallback
|Data type=String
|Description=A callback that is called when errors happen.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/DirectoryEntry
|Example_object_name=DirectoryEntry
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