{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add specification, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''samp''' element represents output from a program or computing system.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''samp''' element to create a code sample.
|Code=&lt;p>Once the task is run, you should see 
&lt;samp&gt;Done, without errors&lt;/samp&gt;.&lt;/p>
}}
}}
{{Notes_Section
|Usage=The '''samp''' element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.
|Notes=By default, most browsers render the contents of '''samp''' elements in a fixed-width, monospaced font, but you can change that with CSS.

If you are looking to mark up programming code, the [[html/elements/code|'''code''' element]] would be more appropriate.

If you are looking to indicate user input (e.g. from a keyboard), the [[html/elements/kbd|'''kbd''']] element is more appropriate.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-samp-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-SAMP
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
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}