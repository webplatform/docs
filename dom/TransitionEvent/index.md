{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Missing Events
transitionstart, transitionend
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Provides specific contextual information associated with Cascading Style Sheets (CSS) transitions.}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The completion of a CSS transition generates a corresponding Document Object Model (DOM) event. An event is fired for each property that undergoes a transition. This allows a content developer to perform actions that synchronize with the completion of a transition. 

Each event provides the name of the property the transition is associated with as well as the duration of the transition.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transitions
|URL=http://dev.w3.org/csswg/css-transitions/#Events-TransitionEvent
|Status=Working Draft
|Relevant_changes=Initial Specification
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/TransitionEvent.TransitionEvent TransitionEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772135(v=vs.85).aspx TransitionEvent Object]
|HTML5Rocks_link=
}}