{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Basic_Page}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The first rule in the user's style sheet in the following example contains an '''!important''' declaration, which overrides the corresponding declaration in the author's style sheet. The second declaration will also take precedence due to being marked '''!important'''. However, the third rule in the user's style sheet is not '''!important''', and will therefore lose to the second rule in the author's style sheet (which happens to set style on a shorthand property). Also, the third author rule will lose to the second author rule since the second rule is '''!important'''. This shows that '''!important''' declarations also have a function within author style sheets.
|LiveURL=
|Code=
/* From the user's style sheet */
p { text-indent: 1em ! important }
p { font-style: italic ! important }
p { font-size: 18pt }
/* From the author's style sheet */
p { text-indent: 1.5em !important }
p { font: normal 12pt sans-serif !important }
p { font-size: 24pt }
}}}}
{{Notes_Section
|Notes=
===Remarks===
CSS attempts to create a "balance of power" between author and user style sheets. By default, rules in an author's style sheet override those in a user's style sheet. However, for balance, an '''!important''' declaration takes precedence over a normal declaration. Both author and user style sheets may contain '''!important''' declarations, and user '''!important''' rules override author '''!important''' rules.
Declaring a shorthand property (for instance, the [[css/cssom/properties/background|'''background''']] property) to be '''!important''' is equivalent to declaring all of its sub-properties to be '''!important'''.
|Import_Notes=
===Syntax===
<code>
{ ''declaration''''' !important ''' }
</code>
===Parameters===
;''declaration'':A CSS property and value declaration within a rule set.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 6.4.2


}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}