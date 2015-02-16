{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''figure''' element (&lt;figure&gt;) represents self-contained content, optionally with a caption, that can be referenced as a single unit from the main content of the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows the '''figure''' element to mark up a code listing. The '''figcaption''' element represents the caption of the figure. The author has also provided a link to the figure in the main content by using a named anchor.
|Code=&lt;!-- Main Content --&gt;
&lt;p&gt;In &lt;a href{{=}}"#l4"&gt;listing 4&lt;/a&gt; we see the primary core interface API declaration.&lt;/p&gt;
&lt;!-- Figure Content --&gt;
&lt;figure id{{=}}"l4"&gt;
    &lt;figcaption&gt;Listing 4. The primary core interface API declaration.&lt;/figcaption&gt;
    &lt;pre&gt;&lt;code&gt;interface PrimaryCore {
 boolean verifyDataLine();
 void sendData(in sequence&amp;lt;byte&gt; data);
 void initSelfDestruct();
}&lt;/code&gt;&lt;/pre&gt;
&lt;/figure&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''figure''' element can be used to annotate content that can be referenced from the main content of the document, such as illustrations, diagrams, photos, code listings, and so on. Figures can be moved away from primary content without affecting the flow of the document.
You can jump to the figure from the main content by using a named anchor. The [[html/attributes/id|'''id''']] attribute of the '''figure''' element specifies the fragment identifier (name of the anchor).
The default CSS for the '''figure''' element is as follows.
 <code>margin: 1em 40px</code>
The '''figure''' element, like '''aside''', separates content from the main flow. Use the '''aside''' element when the content is simply related, but not essential. Use '''figure''' if the content is essential, but position is not important.
Windows Internet Explorer 9.  The '''figure''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
|Import_Notes====Standards information===
There are no standards that apply here.

===HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|block
|}

===Members===
The '''figure''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''figure''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''addBehavior'''
|Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
|-
|[[dom/methods/appendChild|'''appendChild''']]
|Appends an element as a child to the object.
|-
|[[dom/methods/applyElement|'''applyElement''']]
|Makes the element either a child or parent of another element.
|-
|[[dom/methods/attachEvent|'''attachEvent''']]
|Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
|-
|[[dom/methods/blur|'''blur''']]
|Causes the element to lose focus and fires the [[dom/events/blur|'''onblur''']] event.
|-
|[[dom/methods/clearAttributes|'''clearAttributes''']]
|Removes all attributes and values from the object.
|-
|[[dom/methods/click|'''click''']]
|Simulates a click by causing the [[dom/events/click|'''onclick''']] event to fire.
|-
|[[dom/methods/cloneNode|'''cloneNode''']]
|Copies a reference to the object from the document hierarchy.
|-
|[[dom/methods/componentFromPoint|'''componentFromPoint''']]
|Returns the component located at the specified coordinates via certain events.
|-
|'''contains'''
|Checks whether the given element is contained within the object.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttribute|'''hasAttribute''']]
|Determines whether an attribute with the specified name exists.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/hasAttributes|'''hasAttributes''']]
|Determines whether one or more attributes exist for the object.
|-
|[[dom/methods/insertAdjacentHTML|'''insertAdjacentHTML''']]
|Inserts the given HTML text into the element at the location.
|-
|[[dom/methods/insertAdjacentText|'''insertAdjacentText''']]
|Inserts the given text into the element at the specified location.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/normalize|'''normalize''']]
|Merges adjacent DOM objects to produce a normalized document object model.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|'''removeBehavior'''
|Detaches a behavior from the element.
|-
|[[dom/methods/removeNode|'''removeNode''']]
|Removes the object from the document hierarchy.
|-
|[[dom/methods/replaceAdjacentText|'''replaceAdjacentText''']]
|Replaces the text adjacent to the element.
|-
|[[dom/methods/replaceNode|'''replaceNode''']]
|Replaces the object with another element.
|-
|[[dom/methods/setActive|'''setActive''']]
|Sets the object as active without setting focus to the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/setCapture|'''setCapture''']]
|Sets the mouse capture to the object that belongs to the current document.
|-
|[[dom/methods/swapNode|'''swapNode''']]
|Exchanges the location of two objects in the document hierarchy.
|}
 

====Properties====
The '''figure''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/accessKey|'''accessKey''']]
|Sets or retrieves the access key for the object.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[dom/properties/canHaveChildren|'''canHaveChildren''']]
|Gets a value indicating whether the object can contain child objects.
|-
|[[dom/properties/className|'''className''']]
|Sets or retrieves the class of the object.
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[dom/properties/innerdom/innerHTML|'''innerHTML''']]
|Sets or retrieves the HTML between the start and end tags of the object.
|-
|[[dom/properties/innerText|'''innerText''']]
|Sets or retrieves the text between the start and end tags of the object.
|-
|[[dom/properties/isContentEditable|'''isContentEditable''']]
|Gets the value that indicates whether the user can edit the contents of the object.
|-
|[[dom/properties/isDisabled|'''isDisabled''']]
|Gets the value that indicates whether the user can interact with the object.
|-
|[[dom/traversal/properties/isTextEdit|'''isTextEdit''']]
|Retrieves whether a [[dom/traversal/TextRange|'''TextRange''']] object can be created using the object.
|-
|[[html/attributes/lang|'''lang''']]
|Sets or retrieves the language to use.
|-
|[[html/attributes/language|'''language''']]
|Sets or retrieves the language in which the current script is written.
|-
|[[dom/properties/offsetHeight|'''offsetHeight''']]
|Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetParent|'''offsetParent''']]
|Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|'''offsetTop''']] and [[dom/properties/offsetLeft|'''offsetLeft''']] properties of the object.
|-
|[[dom/properties/offsetWidth|'''offsetWidth''']]
|Retrieves the width of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/outerdom/outerHTML|'''outerHTML''']]
|Sets or retrieves the object and its content in HTML.
|-
|[[dom/properties/outerText|'''outerText''']]
|Sets or retrieves the text of the object.
|-
|[[dom/traversal/properties/parentElement|'''parentElement''']]
|Retrieves the parent object in the object hierarchy.
|-
|[[dom/traversal/properties/parentTextEdit|'''parentTextEdit''']]
|Retrieves the container object in the document hierarchy that can be used to create a [[dom/traversal/TextRange|'''TextRange''']] containing the original object.
|-
|'''recordNumber'''
|Retrieves the ordinal record from the data set that generated the object.
|-
|[[html/attributes/role|'''role''']]
|Sets or retrieves the role for this element.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/sourceIndex|'''sourceIndex''']]
|Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|'''all''']] collection.
|-
|[[dom/properties/tagName|'''tagName''']]
|Retrieves the tag name of the object.
|-
|[[dom/properties/tagUrn|'''tagUrn''']]
|Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[html/attributes/title|'''title''']]
|Sets or retrieves advisory information (a ToolTip) for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|}
 
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-figure-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>article</code>
*<code>aside</code>
*<code>figcaption</code>
*<code>footer</code>
*<code>header</code>
*<code>hgroup</code>
*<code>mark</code>
*<code>nav</code>
*<code>section</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}