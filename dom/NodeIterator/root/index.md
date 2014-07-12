{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.}}
{{API_Object_Property
|Property_applies_to=dom/NodeIterator
|Read_only=Yes
|Return_value_name=node
|Javascript_data_type=DOM Node
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
root {{=}} nodeIterator.root; // document.body in this case
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
root = nodeIterator.root;
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-nodeiterator-root
|Status=Living Standard
|Relevant_changes=No change
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.root NodeIterator.root]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974821(v=vs.85).aspx root Property]
|HTML5Rocks_link=
}}