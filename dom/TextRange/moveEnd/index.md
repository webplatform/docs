{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=needs example
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Changes the end position of the range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=Unit
|Data type=BSTR
|Description='''String''' that specifies the units to move, using one of the following values:

character - Moves one or more characters. 

word - Moves one or more words. A word is a collection of characters terminated by a space or some other white-space character, such as a tab. 

sentence - Moves one or more sentences. A sentence is a collection of words terminated by a punctuation character, such as a period. 

textedit - Moves to the start or end of the original range. 

|Optional=No
}}{{Method Parameter
|Name=Count
|Data type=Number
|Description='''Integer''' that specifies the number of units to move. This can be positive or negative. The default is '''1'''.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=textRange
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Integer that returns the number of units moved
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536620(v=vs.85).aspx moveEnd Method]
|HTML5Rocks_link=
}}