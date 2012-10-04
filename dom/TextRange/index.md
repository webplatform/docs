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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example changes the text of a '''button''' element to "Clicked" through the '''TextRange''' object.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
var b {{=}} document.all.tags("BUTTON");
if (b!{{=}}null) {
    var r {{=}} b[0].createTextRange();
    if (r !{{=}} null) {
        r.text {{=}} "Clicked";
    }
}
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use this object to retrieve and modify text in an element, to locate specific strings in the text, and to carry out commands that affect the appearance of the text.
To retrieve a text range object, apply the [[dom/traversal/methods/createTextRange|'''createTextRange''']] method to a '''body''', '''button''', or '''textArea''' element or an '''input''' element that has [[html/attributes/type|'''TYPE''']] text.
Modify the extent of the text range by moving its start and end positions with methods such as [[dom/traversal/methods/move|'''move''']], [[dom/traversal/methods/moveToElementText|'''moveToElementText''']], and [[dom/traversal/methods/findText|'''findText''']]. Within the text range, you can retrieve and modify plain text or HTML text. These forms of text are identical except that HTML text includes HTML tags, and plain text does not.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''TextRange''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TextRange''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/traversal/methods/compareEndPoints|'''compareEndPoints''']]
|Compares an end point of a '''TextRange''' object with an end point of another range.
|-
|[[dom/traversal/methods/duplicate|'''duplicate''']]
|Returns a duplicate of the '''TextRange'''.
|-
|'''execCommand'''
|Executes a command on the current document, current selection, or the given range.
|-
|[[dom/traversal/methods/execCommandShowHelp|'''execCommandShowHelp''']]
|Displays help information for the given command identifier.
|-
|'''expand'''
|Expands the range so that partial units are completely contained.
|-
|[[dom/traversal/methods/findText|'''findText''']]
|Searches for text in the document and positions the start and end points of the range to encompass the search string.
|-
|[[dom/traversal/methods/getBookmark|'''getBookmark''']]
|Retrieves a bookmark (opaque string) that can be used with [[dom/traversal/methods/moveToBookmark|'''moveToBookmark''']] to return to the same range.
|-
|[[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']]
|Retrieves an object that specifies the bounds of a collection of [[dom/TextRectangle|'''TextRectangle''']] objects.
|-
|[[dom/methods/getClientRects|'''getClientRects''']]
|Retrieves a collection of rectangles that describes the layout of the contents of an object or range within the client. Each rectangle describes a single line.
|-
|[[dom/traversal/methods/inRange|'''inRange''']]
|Returns a value indicating whether one range is contained within another.
|-
|[[dom/traversal/methods/isEqual|'''isEqual''']]
|Returns a value indicating whether the specified range is equal to the current range.
|-
|[[dom/traversal/methods/move|'''move''']]
|Collapses the given text range and moves the empty range by the given number of units.
|-
|[[dom/traversal/methods/moveEnd|'''moveEnd''']]
|Changes the end position of the range.
|-
|[[dom/traversal/methods/moveStart|'''moveStart''']]
|Changes the start position of the range.
|-
|[[dom/traversal/methods/moveToBookmark|'''moveToBookmark''']]
|Moves to a bookmark.
|-
|[[dom/traversal/methods/moveToElementText|'''moveToElementText''']]
|Moves the text range so that the start and end positions of the range encompass the text in the given element.
|-
|[[dom/traversal/methods/moveToPoint|'''moveToPoint''']]
|Moves the start and end positions of the text range to the given point.
|-
|[[dom/traversal/methods/parentElement|'''parentElement''']]
|Retrieves the parent element for the given text range.
|-
|[[dom/traversal/methods/pasteHTML|'''pasteHTML''']]
|Pastes HTML text into the given text range, replacing any previous text and HTML elements in the range.
|-
|[[dom/traversal/methods/queryCommandEnabled|'''queryCommandEnabled''']]
|Returns a Boolean value that indicates whether a specified command can be successfully executed using '''execCommand''', given the current state of the document.
|-
|[[dom/traversal/methods/queryCommandIndeterm|'''queryCommandIndeterm''']]
|Returns a Boolean value that indicates whether the specified command is in the indeterminate state.
|-
|[[dom/traversal/methods/queryCommandState|'''queryCommandState''']]
|Returns a Boolean value that indicates the current state of the command.
|-
|[[dom/traversal/methods/queryCommandSupported|'''queryCommandSupported''']]
|Returns a Boolean value that indicates whether the current command is supported on the current range.
|-
|[[dom/traversal/methods/queryCommandText|'''queryCommandText''']]
|Retrieves the string associated with a command.
|-
|[[dom/traversal/methods/queryCommandValue|'''queryCommandValue''']]
|Returns the current value of the document, range, or current selection for the given command.
|-
|[[dom/traversal/methods/scrollIntoView|'''scrollIntoView''']]
|Causes the object to scroll into view, aligning it either at the top or bottom of the window.
|-
|[[dom/traversal/methods/select|'''select''']]
|Makes the selection equal to the current object.
|-
|[[dom/traversal/methods/setEndPoint|'''setEndPoint''']]
|Sets the endpoint of one range based on the endpoint of another range.
|-
|[[dom/traversal/methods/setEndPoint|'''setEndPoint''']]
|Sets the endpoint of one range based on the endpoint of another range.
|}
 

====Properties====
The '''TextRange''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|'''boundingHeight'''
|Retrieves the height of the rectangle that bounds the '''TextRange''' object.
|-
|'''boundingLeft'''
|Retrieves the distance between the left edge of the rectangle that bounds the '''TextRange''' object and the left side of the object that contains the '''TextRange'''.
|-
|'''boundingTop'''
|Retrieves the distance between the top edge of the rectangle that bounds the '''TextRange''' object and the top side of the object that contains the '''TextRange'''.
|-
|'''boundingWidth'''
|Retrieves the width of the rectangle that bounds the '''TextRange''' object.
|-
|[[dom/traversal/properties/htmlText|'''htmlText''']]
|Retrieves the HTML source as a valid HTML fragment.
|-
|[[dom/properties/offsetLeft|'''offsetLeft''']]
|Retrieves the calculated left position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetTop|'''offsetTop''']]
|Retrieves the calculated top position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/traversal/properties/text|'''text''']]
|Sets or retrieves the text contained within the range.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/methods/createTextRange|createTextRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}