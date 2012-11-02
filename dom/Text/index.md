{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/CharacterData, dom/Node
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''TextNode''' object to change the text of an '''li''' object.
|Code=&lt;script&gt;
function fnChangeText(){
   var oTextNode {{=}} document.createTextNode("New List Item 1");
   var oReplaceNode {{=}} oItem1.firstChild.replaceNode(oTextNode);
}
&lt;/script&gt;

&lt;ul onclick {{=}} "fnChangeText()"&gt;
&lt;li id {{=}} "oItem1"&gt;List Item 1&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes=Use the [[dom/methods/createTextNode|'''createTextNode''']] method to create a '''TextNode''' object. After you create the '''TextNode''', you can add to it using the [[dom/methods/appendChild|'''appendChild''']], [[dom/methods/replaceNode|'''replaceNode''']], or [[dom/methods/insertBefore|'''insertBefore''']] methods.
This object is available in script as of Microsoft Internet Explorer 5.
|Import_Notes====Members===
The '''TextNode''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TextNode''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/addEventListener|'''addEventListener''']]
|Registers an event handler for the specified event type.
|-
|[[dom/methods/appendData|'''appendData''']]
|Adds a new character string to the end of the object.
|-
|[[dom/methods/compareDocumentPosition|'''compareDocumentPosition''']]
|Compares the position of two nodes in a document.
|-
|[[dom/methods/deleteData|'''deleteData''']]
|Removes a specified range of characters from the object.
|-
|[[dom/methods/dispatchEvent|'''dispatchEvent''']]
|Sends an event to the current element.
|-
|[[dom/methods/insertData|'''insertData''']]
|Inserts a new character string in the object at a specified offset.
|-
|[[dom/methods/isDefaultNamespace|'''isDefaultNamespace''']]
|Indicates whether or not a namespace is the default namespace for a document.
|-
|[[dom/methods/isEqualNode|'''isEqualNode''']]
|Determines if two nodes are equal.
|-
|[[dom/methods/isSameNode|'''isSameNode''']]
|Determines if two node references refer to the same node.
|-
|[[dom/methods/isSupported|'''isSupported''']]
|Returns a value indicating whether or not the object supports a specific DOM standard.
|-
|[[dom/methods/lookupNamespaceURI|'''lookupNamespaceURI''']]
|Gets the URI of the namespace associated with a namespace prefix, if any.
|-
|[[dom/methods/lookupPrefix|'''lookupPrefix''']]
|Gets the namespace prefix associated with a URI, if any.
|-
|[[dom/methods/normalize|'''normalize''']]
|Merges adjacent DOM objects to produce a normalized document object model.
|-
|[[dom/methods/removeEventListener|'''removeEventListener''']]
|Removes an event handler that  the  [[dom/methods/addEventListener|'''addEventListener''']] method registered.
|-
|[[dom/methods/replaceData|'''replaceData''']]
|Replaces a specified range of characters in the object with a new character string.
|-
|[[dom/methods/replaceWholeText|'''replaceWholeText''']]
|Replaces the text of the current object.
|-
|[[dom/methods/splitText|'''splitText''']]
|Divides a text node at the specified index.
|-
|[[dom/methods/substringData|'''substringData''']]
|Extracts a range of characters from the object.
|}
 

====Properties====
The '''TextNode''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[dom/properties/data (TextNode)|'''data''']]
|Sets or gets the value of a '''TextNode''' object.
|-
|[[dom/properties/length (TextNode)|'''length''']]
|Gets the number of characters in a '''TextNode''' object.
|-
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
|-
|[[dom/properties/nextSibling|'''nextSibling''']]
|Retrieves a reference to the next child of the parent for the object.
|-
|[[dom/properties/nodeName|'''nodeName''']]
|Gets the name of a particular type of node.
|-
|[[dom/properties/nodeType|'''nodeType''']]
|Retrieves the type of the requested node.
|-
|[[dom/properties/nodeValue|'''nodeValue''']]
|Gets or sets the value of a node.
|-
|[[dom/properties/parentNode|'''parentNode''']]
|Retrieves the parent object in the document hierarchy.
|-
|[[dom/properties/prefix|'''prefix''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[dom/properties/previousSibling|'''previousSibling''']]
|Gets a reference to the previous child of the parent for the object.
|-
|[[dom/properties/textContent|'''textContent''']]
|Sets or retrieves the text content of an object and any child objects.
|-
|[[dom/properties/wholeText|'''wholeText''']]
|Retrieves the text of the current object.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}