{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Perspective in graphic arts is the representation on a flat surface of what the viewer's eye would see in a 3D space. If there were a clear window pane between the viewer and the object, you could place points on the window surface that correspond to the points that exist beyond the glass. (See [http://en.wikipedia.org/wiki/Perspective_(graphical) Wikipedia] for more information about graphical perspective and diagrams.)

The illusion of perspective on a flat surface, such as a computer screen, is created by placing points on the flat surface as they would appear if the flat surface were a clear window pane through which the viewer was looking at the object.

Perspective-origin is the location of the viewer's eye. For example, if the viewer is looking down at an object it appears differently than if the viewer is looking up at an object or from the side.

The perspective-origin property virtually sets the x and y point location of the eye that is viewing an object. As perspective-origin-x changes, the virtual eye moves along the x axis (left or right of the center of the screen). As perspective-origin-y changes, the eye moves along the y axis (closer to the top or bottom of the screen).
The illusion of perspective on a flat surface, such as a computer screen, is created by placing points on the flat surface as they would appear if the flat surface were a clear window pane through which the viewer was looking at the object.

Perspective-origin is the location of the viewer's eye. For example, if the viewer is looking down at an object it appears differently than if the viewer is looking up at an object or from the side.

The perspective-origin property virtually sets the x and y point location of the eye that is viewing an object. As perspective-origin-x changes, the virtual eye moves along the x axis (left or right of the center of the screen). As perspective-origin-y changes, the eye moves along the y axis (closer to the top or bottom of the screen).
}}
{{CSS Property
|Initial value=50% 50%
|Applies to=block-level and inline-level elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>em</code>,
<code>ex</code>,
or <code>px</code>), that indicates the origin of transformation.
For more information about the supported length units,
see CSS Values and Units.
}}{{CSS Property Value
|Data Type=percentage
|Description=An integer, followed by a %. The value is a percentage of the total box length (for the first value) or the total box height (for the second value, if specified).
}}{{CSS Property Value
|Data Type=left
|Description=First value only. Equal to 0% or a zero length.
}}{{CSS Property Value
|Data Type=center
|Description=First value only. Equal to 50% or half the length of the box.
}}{{CSS Property Value
|Data Type=right
|Description=First value only. Equal to 100% or the full box length.
}}{{CSS Property Value
|Data Type=top
|Description=Second value only. Equal to 0% or a zero height.
}}{{CSS Property Value
|Data Type=center
|Description=Second value only. Equal to 50% or a half the height of the box.
}}{{CSS Property Value
|Data Type=bottom
|Description=Second value only. Equal to 100% or the full box height.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-perspective-origin''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
This property does not affect how the object is rendered.
This property has no effect on the child elements if the [[css/properties/perspective|'''perspective''']] property is not set for the object.
|Import_Notes====Syntax===
<code>'''perspective-origin: ''''''[''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ? ''']''' '''{{!}}''' '''[''' '''[''' left '''{{!}}''' center '''{{!}}''' right ''']''' {{!}}{{!}} '''[''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 11
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}