{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=In the following example, an '''article''' (part of a larger document about apples) contains two short sections.
|LiveURL=
|Code=
&lt;article&gt;
 &lt;hgroup&gt;
  &lt;h1&gt;Apples&lt;/h1&gt;
  &lt;h2&gt;Tasty, delicious fruit!&lt;/h2&gt;
 &lt;/hgroup&gt;
 &lt;p&gt;The apple is the pomaceous fruit of the apple tree.&lt;/p&gt;
 &lt;section&gt;
  &lt;h1&gt;Red Delicious&lt;/h1&gt;
  &lt;p&gt;These bright red apples are the most common found in many
  supermarkets.&lt;/p&gt;
 &lt;/section&gt;
 &lt;section&gt;
  &lt;h1&gt;Granny Smith&lt;/h1&gt;
  &lt;p&gt;These juicy, green apples make a great filling for
  apple pies.&lt;/p&gt;
 &lt;/section&gt;
&lt;/article&gt;
}}
{{Single_Example
|Description=The rank of '''h1-h6''' elements is determined by the number in their name.  The '''h1''' element is said to have the highest rank; the '''h6''' element has the lowest rank.  Two elements with the same name have the same rank. The default style applied to '''hn''' elements varies according to the rank of the element. However, the rank of headings that appear within a '''section''' element is automatically reduced.  This affects the visual appearance of the headings inside the '''section''' element. In the following example, the author uses '''h1''' elements without worrying whether a particular section is at the top level, the second level, the third level, and so on. The two outlines produce equivalent output.
|LiveURL=
|Code=
&lt;!-- First outline --&gt;
&lt;h1&gt;Let's call it a draw(ing surface)&lt;/h1&gt;
&lt;h2&gt;Diving in&lt;/h2&gt;
&lt;h2&gt;Simple shapes&lt;/h2&gt;
&lt;h2&gt;Canvas coordinates&lt;/h2&gt;
&lt;h3&gt;Canvas coordinates diagram&lt;/h3&gt;
&lt;h2&gt;Paths&lt;/h2&gt;
&lt;hr/&gt;
&lt;!-- Equivalent outline using section elements --&gt;
&lt;h1&gt;Let's call it a draw(ing surface)&lt;/h1&gt;
&lt;section&gt;
&lt;h1&gt;Diving in&lt;/h1&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Simple shapes&lt;/h1&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Canvas coordinates&lt;/h1&gt;
&lt;section&gt;
&lt;h1&gt;Canvas coordinates diagram&lt;/h1&gt;
&lt;/section&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Paths&lt;/h1&gt;
&lt;/section&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 9.  The '''section''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
A section, in this context, is a thematic grouping of content, typically with a heading. Examples of sections would be chapters, the various tabbed pages in a tabbed dialog box, or the numbered sections of a thesis. A website's home page could be split into sections for an introduction, news items, and contact information.
A section, in this context, is a thematic grouping of content, typically with a heading. Examples of sections would be chapters or the numbered sections of a thesis. A document's main page could be split into sections for an introduction, news items, and contact information.
The '''section''' element is not a generic container element. Authors are encouraged to use the '''div''' element for styling purposes or when an element is needed as a convenience for scripting. The '''section''' element is appropriate only if the element's contents would be listed explicitly in the document's outline.
'''Note'''  Authors are encouraged to use the '''article''' element instead of the '''section''' element when it would make sense to syndicate the contents of the element.
|Import_Notes=
===Standards information===
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
The '''section''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''section''' object has these methods.
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
The '''section''' object has these properties.
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
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>article</code>
*<code>aside</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>footer</code>
*<code>header</code>
*<code>hgroup</code>
*<code>mark</code>
*<code>nav</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}