{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes={{Editorial/Merge_Candidate
|Other=css/selectors/id_selector}}
|Checked_Out=No
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The #id selector styles the element with the specified id.}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule applies to the element with id{{=}}"navigation" and its descendants.
|Code=&lt;style&gt;
    #navigation { line-height: 0px; font-size: x-small; }
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The id attribute allows authors to uniquely identify an element instance in the document tree. ID selectors match an element instance based on its identifier. The id attribute value must immediately follow the "pound" (#) notation.
'''Note'''  Windows Internet Explorer allows multiple elements to share a single ID value. If more than one element exists, the style rule will apply to all elements with the given ID. Only one id attribute may be present on any given element.
In the event that a style declaration conflicts with another declaration, the rule with a higher level of specificity is used. (See Understanding CSS Selectors.) If a Class Selector and ID Selector are in conflict, the id is chosen.
|Import_Notes====Syntax===
<code><strong/>''sel'''''#'''''value'' {...}
</code>
===Parameters===
;''sel'':Selector
;''value'':String that specifies the value of the "id" attribute.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 1.5
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
{{See_Also_Section
|Topic_clusters=Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}