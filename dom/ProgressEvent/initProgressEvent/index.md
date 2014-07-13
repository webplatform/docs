{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Depreciated?
see MDN link https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.initProgressEvent
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Initializes the value of a ProgressEvent object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=typeArg
|Data type=String
|Description=The value of this parameter must be one of the following values.
'loadstart'  An operation has started.
'progress' An operation is in progress.
'error' The operation failed to complete.
'abort' The operation was cancelled.
'load' The operation completed successfully.

|Optional=No
}}{{Method Parameter
|Name=canBubbleArg
|Data type=Boolean
|Description=Specifies whether an event bubbles.
|Optional=No
}}{{Method Parameter
|Name=cancelableArg
|Data type=Boolean
|Description=Specifies whether an event can be cancelled.
|Optional=No
}}{{Method Parameter
|Name=lengthComputable
|Data type=Boolean
|Description=Indicates whether the value of the [[dom/ProgressEvent/total|'''total''']] attribute of the [[dom/ProgressEvent|'''ProgressEvent''']] is accurate.
|Optional=No
}}{{Method Parameter
|Name=loadedArg
|Data type=unsigned long
|Description=Specifies the number of bytes already loaded or zero if not known.
|Optional=No
}}{{Method Parameter
|Name=totalArg
|Data type=unsigned long
|Description=Specifies the number of bytes to be loaded.  If ''lengthComputable'' is false, this must be zero ("0").
|Optional=No
}}
|Method_applies_to=dom/ProgressEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=Depreciated
This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.

Non-standard
This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.
|Import_Notes====Syntax===
var retval = ProgressEvent.initProgressEvent(typeArg, canBubbleArg, cancelableArg, lengthComputable, loadedArg, totalArg); 
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.initProgressEvent ProgressEvent.initProgressEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772353(v=vs.85).aspx initProgressEvent Method]
|HTML5Rocks_link=
}}