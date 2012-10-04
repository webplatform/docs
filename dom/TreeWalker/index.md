{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''TreeWalker''' is dynamic, reflecting the state of the document as it is edited or changed.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_tr\ie]:%20TreeWalker object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2


===Members===
The '''TreeWalker''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TreeWalker''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/traversal/methods/firstChild|'''firstChild''']]
|Retrieves a reference to the first child of the current node of the filtered '''TreeWalker''' hierarchy and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/lastChild|'''lastChild''']]
|Retrieves a reference to the last child of the current node of the filtered '''TreeWalker''' hierarchy and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/nextNode|'''nextNode''']]
|Returns the next node in the [[dom/traversal/NodeIterator|'''NodeIterator''']] or '''TreeWalker''' list and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/nextSibling|'''nextSibling''']]
|Retrieves the next sibling of the current node in the filtered '''TreeWalker''' hierarchy and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/parentNode|'''parentNode''']]
|Retrieves the parent object in the document hierarchy relative to the current node and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/previousNode|'''previousNode''']]
|Returns the previous node in the [[dom/traversal/NodeIterator|'''NodeIterator''']] or '''TreeWalker'''  list and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|-
|[[dom/traversal/methods/previousSibling|'''previousSibling''']]
|Retrieves the previous sibling of the current node in the filtered '''TreeWalker''' hierarchy and updates [[dom/traversal/properties/currentNode|'''currentNode''']].
|}
 

====Properties====
The '''TreeWalker''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/traversal/properties/currentNode|'''currentNode''']]
|Sets or retrieves where the current node in a filtered '''TreeWalker''' hierarchy is positioned.
|-
|[[dom/traversal/properties/expandEntityReferences|'''expandEntityReferences''']]
|Flag to specify whether or not the children of entity reference nodes are visible.
|-
|[[dom/traversal/properties/filter|'''filter''']]
|Gets the function object that the iterator uses to filter nodes that go into '''TreeWalker''' hierarchies or [[dom/traversal/NodeIterator|'''NodeIterator''']] lists.
|-
|[[dom/traversal/properties/root|'''root''']]
|Gets the root node that was specified when the object was created.
|-
|[[dom/traversal/properties/whatToShow|'''whatToShow''']]
|Gets which node types are presented through the iterator. Nodes that are not accepted are skipped, but their children are still considered.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}