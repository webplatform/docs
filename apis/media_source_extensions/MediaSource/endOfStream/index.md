{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Used to indicate that the end of the stream has been reached.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=error
|Data type=enum
|Description=Type: EndOfStreamError

If an error has occurred, this optional parameter can be used to send error information. 

EndOfStreamError error values
;network 
:A network error occurred.
;decode 
:A decode error occurred.
|Optional=Yes
}}
|Method_applies_to=apis/media_source_extensions/MediaSource
|Example_object_name=MediaSource
|Javascript_data_type=void
|Return_value_description=No return value
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This method throws an <code>INVALID_STATE_ERR</code> exception under the following conditions:

*If the readyState attribute is not open.
*If the updating attribute is true on any SourceBuffer in sourceBuffers.
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}