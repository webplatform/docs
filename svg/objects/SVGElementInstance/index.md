{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=

===Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The root object in the instance tree is pointed to by the [[svg/properties/instanceRoot|'''instanceRoot''']] attribute on the [[svg/elements/use|'''SVGUseElement''']] object for the corresponding '''use''' element.

If the [[svg/elements/use|'''use''']] element references a simple graphics element such as [[svg/elements/rect|'''rect''']],  there is only  one  '''SVGElementInstance'''  object, and the [[svg/properties/correspondingElement|'''correspondingElement''']] attribute on this '''SVGElementInstance''' object is the '''SVGRectElement''' that corresponds to the referenced '''rect''' element.

If the [[svg/elements/use|'''use''']] element references a [[svg/elements/g|'''g''']] element that contains two [[svg/elements/rect|'''rect''']] elements, the instance tree contains three '''SVGElementInstance''' objects: a root '''SVGElementInstance''' object whose [[svg/properties/correspondingElement|'''correspondingElement''']] attribute is the  '''SVGGElement'''  object for the '''g''' element, and then two child '''SVGElementInstance''' objects that have their '''correspondingElement''' attribute that is an '''SVGRectElement''' object.

If the referenced object is  a [[svg/elements/use|'''use''']] element, or if there are  '''use''' subelements within the referenced object, the instance tree contains a  recursive expansion of the indirect references to form a complete tree. For example, if a  '''use'''  element references a  [[svg/elements/g|'''g''']] element, and the  '''g''' element  contains a  '''use''' element, and that '''use''' element references a  [[svg/elements/rect|'''rect''']] element, the instance tree for the original (outermost)  '''use''' consists  of a hierarchy of '''SVGElementInstance'''  objects, as follows:

  SVGElementInstance #1 (parentNode=null, firstChild=#2, correspondingElement is the 'g')
    SVGElementInstance #2 (parentNode=#1, firstChild=#3, correspondingElement is the other 'use')
      SVGElementInstance #3 (parentNode=#2, firstChild=null, correspondingElement is the 'rect')

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.9

===Members===

The '''SVGElementInstance''' object has these methods:

*[[svg/methods/addListener|'''addEventListener''']]: Registers an event listener
*[[svg/methods/dispatchEvent|'''dispatchEvent''']]: Dispatches an event to an object.
*[[svg/methods/removeListener|'''removeEventListener''']]: Removes an event listener.

The '''SVGElementInstance''' object has these properties:

*[[svg/properties/childNodes|'''childNodes''']]: Gets an [[svg/objects/SVGElementInstanceList|'''SVGElementInstanceList''']] object that contains all children of this '''SVGElementInstance''' object within the instance tree.
*[[svg/properties/correspondingElement|'''correspondingElement''']]: Gets the corresponding element that this object is an instance of.
*[[svg/properties/correspondingUseElement|'''correspondingUseElement''']]: Gets the corresponding [[svg/elements/use|'''use''']] element that this object belongs to.
*[[svg/properties/firstChild|'''firstChild''']]: Gets the first child of this '''SVGElementInstance''' object in the instance tree.
*[[svg/properties/lastChild|'''lastChild''']]: Gets the last child of this '''SVGElementInstance''' object in the instance tree.
*[[svg/properties/nextSibling|'''nextSibling''']]: Gets the '''SVGElementInstance''' object that immediately follows this '''SVGElementInstance''' object.
*[[svg/properties/parentNode|'''parentNode''']]: Gets the parent of this '''SVGElementInstance''' object within the instance tree.
*[[svg/properties/previousSibling|'''previousSibling''']]: Gets the '''SVGElementInstance''' object that immediately precedes this '''SVGElementInstance''' object.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}