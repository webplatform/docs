{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Reserved.  
Always returns -1.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Each [[css/cssom/page|'''page''']] object represents a style sheet that corresponds to a '''@page''' rule in the document.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Parameters===
;''bstrSelector'' [in]:Type: '''[[css/cssom/page|<b>page''']] object.
;''bstrStyle'' [in]:Type: '''[[css/cssom/page|<b>page''']] object. This style takes the same form as an inline style specification. For example, "<code>color:blue</code>" is a valid style parameter.
;''lIndex'' [in]:Type: '''Integer''' '''<b>Integer''' that specifies the zero-based position in the 	[[css/cssom/pages|'''pages''']] collection where the new [[css/cssom/page|'''page''']] object should be placed.<dl class{{=}}"indent"><dt><a id{{=}}"-1"/>'''-1'''</dt><dd>Default. The [[css/cssom/page|'''page''']] object is added to the end of the collection.</dd></dl>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}