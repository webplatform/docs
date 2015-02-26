{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Examples, compatibility, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Programmatically push a document state (including URI and document title) onto the user agent's history.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=statedata
|Data type=any
|Description=The data to push onto the session history.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=title
|Data type=any
|Description=The desired title for the data.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=url
|Data type=any
|Description=An optional URL to associate with the data.
|Optional=Yes
}}
|Method_applies_to=dom/History
|Example_object_name=history
|Return_value_name=
|Javascript_data_type=void
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/browsers.html#dom-history-pushstate
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}