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
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13


===Members===
The '''Range''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''Range''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/traversal/methods/cloneContents|'''cloneContents''']]
|Returns a document fragment containing the nodes of a range. If any nodes are partially selected, their start or end nodes are included.
|-
|[[dom/traversal/methods/cloneRange|'''cloneRange''']]
|Returns a new range with boundary points that are equal to the original range.
|-
|[[dom/traversal/methods/collapse|'''collapse''']]
|Collapses (or removes) a range by moving the insertion point to the beginning or end of the current range.
|-
|[[dom/traversal/methods/compareBoundaryPoints|'''compareBoundaryPoints''']]
|Compares two ranges by comparing their boundary points.
|-
|[[dom/traversal/methods/RangeException|'''createContextualFragment''']]
|The createContextualFragment() method enables you to parse a string of HTML into a DocumentFragment using the starting node of a DOM Range as the parsing context.
|-
|[[dom/traversal/methods/deleteContents|'''deleteContents''']]
|Removes all contents within a selected range.
|-
|[[dom/traversal/methods/detach|'''detach''']]
|Removes or detaches an object and associated resources.
|-
|[[dom/traversal/methods/extractContents|'''extractContents''']]
|Removes the contents of a range from a document or document fragment and puts it a new document fragment.
|-
|[[dom/traversal/methods/insertNode|'''insertNode''']]
|Inserts a node into the start of a '''Range''' object.
|-
|[[dom/traversal/methods/selectNode|'''selectNode''']]
|Selects a range node and all of its contents.
|-
|[[dom/traversal/methods/selectNodeContents|'''selectNodeContents''']]
|Selects the contents within a node in a range.
|-
|[[dom/traversal/methods/setEnd|'''setEnd''']]
|Sets the end point of the range.
|-
|[[dom/traversal/methods/setEndAfter|'''setEndAfter''']]
|Sets the end of a range to a point after a specific node.
|-
|[[dom/traversal/methods/setEndBefore|'''setEndBefore''']]
|Sets the end of the range to a point before a specific node.
|-
|[[dom/traversal/methods/setStart|'''setStart''']]
|Sets the starting point of a range.
|-
|[[dom/traversal/methods/setStartAfter|'''setStartAfter''']]
|Sets the starting point of the range to a point after a specific node.
|-
|[[dom/traversal/methods/setStartBefore|'''setStartBefore''']]
|Sets the start point of a range to a point before a specific node.
|-
|[[dom/traversal/methods/surroundContents|'''surroundContents''']]
|Moves the contents of a Range to a new parent node, placing the new parent node at the start position of the Range.
|-
|[[dom/traversal/methods/toString|'''toString''']]
|Returns the contents of a '''Range''' as a string. This string contains only the data characters, no markup.
|}
 

====Properties====
The '''Range''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/traversal/properties/collapsed|'''collapsed''']]
|Retrieves whether a range is collapsed or empty.
|-
|[[dom/traversal/properties/commonAncestorContainer|'''commonAncestorContainer''']]
|Returns the deepest node in which two boundary points exist.
|-
|[[dom/traversal/properties/endContainer|'''endContainer''']]
|Retrieves the end point node of the current range.
|-
|[[dom/traversal/properties/endOffset|'''endOffset''']]
|Retrieves the ending boundary point relative to the [[dom/traversal/properties/startContainer|'''startContainer''']] in the current range.
|-
|[[dom/traversal/properties/startContainer|'''startContainer''']]
|Retrieves the starting node of a current range.
|-
|[[dom/traversal/properties/startOffset|'''startOffset''']]
|Retrieves the offset of the starting boundary point relative to the [[dom/traversal/properties/startContainer|'''startContainer''']] in the current range.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_tr\ie]:%20Range object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}