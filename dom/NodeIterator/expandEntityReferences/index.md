{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Flag to specify whether or not the children of entity reference nodes are visible. }}
{{API_Object_Property
|Property_applies_to=dom/NodeIterator
|Read_only=Yes
|Javascript_data_type=Boolean
|Return_value_description=The NodeIterator.expandEntityReferences read-only property returns a Boolean flag indicating whether or not the children of entity reference nodes are visible to the NodeIterator.

If this value is false, the children of entity reference nodes (as well as all of their descendants) are rejected. This takes precedence over the value of the  NodeIterator.whatToShow method and the associated filter.
|Example_value_name=expand
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var nodeIterator {{=}} document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
expand {{=}} nodeIterator.expandEntityReferences;
}}
}}
{{Notes_Section
|Notes====Remarks===
Deprecated

This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#nodeiterator
|Status=Living Standard
|Relevant_changes=Removed from the spec
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.expandEntityReferences NodeIterator.explandEntityReferences]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974819(v=vs.85).aspx expandEntityReferences Property]
|HTML5Rocks_link=
}}