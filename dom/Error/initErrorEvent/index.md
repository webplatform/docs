{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs summary, examples, compat and spec link
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=typeArg
|Data type=any
|Description=The type of the event being created
|Optional=No
}}{{Method Parameter
|Index=1
|Name=canBubbleArg
|Data type=any
|Description=Indicates whether the event can bubble.
When true
the event should propagate upward. 
When false
the event does not propagate upward.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=cancelableArg
|Data type=any
|Description=Indicates whether the event’s default action can be prevented.
When true, the default action can be canceled. 
When false, the default action cannot be canceled.
|Optional=No
}}{{Method Parameter
|Index=3
|Name=messageArg
|Data type=any
|Description=The error message string.
|Optional=No
}}{{Method Parameter
|Index=4
|Name=filenameArg
|Data type=any
|Description=The absolute URL of the script in which the error originally occurred.
|Optional=No
}}{{Method Parameter
|Index=5
|Name=linenoArg
|Data type=unsigned long
|Description=The line number where the error occurred in the script.
|Optional=No
}}
|Method_applies_to=dom/Error
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK

Type: '''HRESULT'''

This method can return one of these values.

S_OK
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}