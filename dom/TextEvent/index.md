{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs an example?
http://help.dottoro.com/ljuecqgv.php
only works in webkit,
FX has no TextEvent,
IE11 has but above sample runs without errors or the expected result... appears IE prevent programmatic text input into input fields.
Missing initTextEvent Method
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Represents a text event that usually occurs when text is actually inserted into the document.}}
{{API_Object
|Subclass_of=dom/UIEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=txtEl=document.getElementById('txtInput'); // textarea
if(window.addEventListener){
txtEl.addEventListener('textinput', handler, false);
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events (20110531)
|URL=http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531
|Status=Outdated Working Draft
|Relevant_changes=Section 5.2.5
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974350(v=vs.85).aspx TextEvent Object]
|HTML5Rocks_link=
}}