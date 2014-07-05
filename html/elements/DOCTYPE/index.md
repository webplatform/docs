{{Page_Title}}
{{Flags
|State=In Progress
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|A '''Document Type Declaration''', or '''DOCTYPE''', is an instruction that associates a particular [[SGML]] or [[XML]] document (for example, a [[webpage]]) with a [[Document Type Definition]] (DTD) (for example, the formal definition of a particular version of [[HTML]]). In the [[Serialization|serialized]] form of the document, it manifests as a short string of [[Markup language|markup]] that conforms to a particular syntax. Not including <!DOCTYPE> may trigger [[html/Quirks_mode|Quirks mode]].}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=HTML5 has one doctype declaration
|Code=<!DOCTYPE html>
}}{{Single Example
|Language=HTML
|Description=HTML 4.01 Strict
|Code=<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
}}{{Single Example
|Language=HTML
|Description=HTML 4.01 Transitional
|Code=<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
}}
}}
{{Notes_Section
|Usage=Add <syntaxhighlight lang="HTML5">
<!DOCTYPE html>
</syntaxhighlight> to the start of your document.
|Notes=The <!DOCTYPE> declaration must be the very first thing in an HTML document, before the <html> tag. 

This is not a HTML tag but an instruction for the browser about the version of the document.

In HTML 4.01, the <!DOCTYPE> declaration refers to a DTD, because HTML 4.01 was based on SGML. The DTD specifies the rules for the markup language, so that the browsers render the content correctly.

[[HTML5]] is not based on SGML, and therefore does not require a reference to a DTD.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Deprecated, HTML
|Manual_links=html/quirksmode
}}
{{Topics|DOCTYPE, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}