{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Move an Entry to a different location on the file system.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=parent
|Data type=String
|Description=The directory to which to move the Entry.
|Optional=No
}}{{Method Parameter
|Name=newName
|Data type=String
|Description=The new name of the Entry. Defaults to the Entry's current name if unspecified.
|Optional=Yes
}}{{Method Parameter
|Name=successCallback
|Data type=String
|Description=A callback that is called with the Entry for the new location.
|Optional=Yes
}}{{Method Parameter
|Name=errorCallback
|Data type=String
|Description=A callback that is called when errors happen.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/Entry
|Example_object_name=Entry
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=It is an error to try to:
*move a directory inside itself or to any child at any depth;
*move an entry into its parent if a name different from its current one isn't provided;
*move a file to a path occupied by a directory;
*move a directory to a path occupied by a file;
*move any element to a path occupied by a directory which is not empty.

A move of a file on top of an existing file must attempt to delete and replace that file.

A move of a directory on top of an existing empty directory must attempt to delete and replace that directory.
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