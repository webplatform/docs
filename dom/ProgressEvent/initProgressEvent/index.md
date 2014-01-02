{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=typeArg|Data type=DOMString|Description=The value of this parameter must be one of the following values.|Optional=}}
{{Method Parameter|Name=canBubbleArg|Data type=boolean|Description=Specifies whether an event bubbles.|Optional=}}
{{Method Parameter|Name=cancelableArg|Data type=boolean|Description=Specifies whether an event can be cancelled.|Optional=}}
{{Method Parameter|Name=lengthComputable|Data type=boolean|Description=Indicates whether the value of the [[dom/properties/total|'''total''']] attribute of the [[dom/objects/ProgressEvent|'''ProgressEvent''']] is accurate.|Optional=}}
{{Method Parameter|Name=loadedArg|Data type=integer|Description=Specifies the number of bytes already loaded or zero if not known.|Optional=}}
{{Method Parameter|Name=totalArg|Data type=integer|Description=Specifies the number of bytes to be loaded.  If ''lengthComputable'' is false, this must be zero ("0").|Optional=}}
|Method_applies_to=dom/ProgressEvent
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
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/ProgressEvent|ProgressEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}