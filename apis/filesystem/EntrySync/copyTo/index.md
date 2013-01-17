{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Copy an EntrySync to a different location on the file system.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=parent
|Data type=String
|Description=The directory to which to move the EntrySync.
|Optional=No
}}{{Method Parameter
|Name=newName
|Data type=String
|Description=The new name of the EntrySync. Defaults to the EntrySync's current name if unspecified.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/EntrySync
|Example_object_name=EntrySync
|Return_value_description=EntrySync
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=It is an error to try to:
*copy a directory inside itself or to any child at any depth;
*copy an EntrySync into its parent if a name different from its current one isn't provided;
*copy a file to a path occupied by a directory;
*copy a directory to a path occupied by a file;
*copy any element to a path occupied by a directory which is not empty.

A copy of a file on top of an existing file must attempt to delete and replace that file.

A copy of a directory on top of an existing empty directory must attempt to delete and replace that directory.

Directory copies are always recursive--that is, they copy all contents of the directory.
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