{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oNode
|Data type=any
|Description= Object containing the previous node in the list.
|Optional=No
}}
|Method_applies_to=dom/NodeIterator
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}InvalidStateError _ERR
{{!}}NodeIterator raises this exception if detach has been invoked on the object.
{{!}}}
 

This method returns null when the current node is the first node in the set.


[[dom/Node|'''Node''']]

 Object containing the previous node in the list.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var nodeIterator {{=}} document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false // this optional argument is not used any more
);
currentNode {{=}} nodeIterator.nextNode(); // returns the next node
previousNode {{=}} nodeIterator.previousNode(); // same result, since we backtracked to the previous nod
}}
}}
{{Notes_Section
|Notes=In old browsers, as specified in old versions of the specifications, the method may throws the INVALID_STATE_ERR DOMException if this method is called after the NodeIterator.detach()method. Recent browsers never throw.
|Import_Notes====Syntax===
node = nodeIterator.previousNode();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-nodeiterator-previousnode
|Status=Living Standard
|Relevant_changes=As detach() is now a no-op method, this method cannot throw anymore.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.previousNode NodeIterator.previousNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975284(v=vs.85).aspx previousNode Method]
|HTML5Rocks_link=
}}