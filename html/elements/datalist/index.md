{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''datalist''' element (&lt;datalist&gt;) represents a set of [[/html/elements/option|option]] elements that represent predefined options for other controls. It may be associated with an [[/html/elements/input|input]] element by adding a list attribute to the input element.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<input type="text" name="locations" list="places">
<datalist id="places">
     <option>Amman, Jordan</option>
     <option>New York, NY, USA</option>
     <option>Paris, France</option>
     <option>Vienna, Austria</option>
</datalist>
}}
}}
{{Notes_Section
|Notes====Remarks===
The following example uses a '''datalist''' object and options to display a list of files from a files dialog.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.10


===Members===
The '''datalist''' object has these types of members:
*[#properties Properties]


====Properties====
The '''datalist''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/options (dom/options|'''options''']]
|A collection of '''option''' objects that represent possible selections for a '''datalist''' element.
|}
 
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
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}