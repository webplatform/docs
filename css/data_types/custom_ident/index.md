{{Page_Title|&lt;custom-ident&gt;}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{Summary_Section|The <code>&lt;custom-ident&gt;</code> CSS data type represents an identifier token created by the stylesheet author to reference content in a different part of the stylesheet.  It is used for counters and for animation.}}
{{Data_Type_Page
|Content=Identifiers are case-sensitive.  Valid custom identifier values:

* should usually contain letters, digits, non-ASCII characters, or the underscore ('''_''') or hyphen ('''-''') characters;
* ''may'' contain other ASCII characters if escaped with backslash ('''\''');
* must not use a digit as the first character unless it is escaped;
* must not match any keywords that are valid values for the property where it is used;
* must not match the CSS-wide keywords "initial" or "inherit" or the reserved word "default", in any combination of upper or lowercase letters.

Identifiers are not quoted.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The example uses three custom identifiers: <code>h1-counter</code>, <code>subSectionCounter</code>, and <code>colorChange</code>.
|Code=h1 {
    counter-increment: h1-counter;
    counter-reset: subSectionCounter;
    animation: colorChange 3s infinite alternate;
}
h1::before {
    content: counter(h1-counter); 
      /*counter tokens can contain digits and hyphens */
   padding:0.5em;
}
h2 {
   counter-increment: subSectionCounter; /* note case must match exactly */
}
h2::before {
   content: counter(h1-counter)  "."  counter(subSectionCounter);
   padding:0.5em;
}
@keyframes colorChange {
   from {
     color:blue;
   }
   to {
     color:green;
   }
}
|LiveURL=http://code.webplatform.org/gist/10605942
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|URL=http://www.w3.org/TR/css3-values/#custom-idents
|Status=W3C Candidate Recommendation
|Relevant_changes=Introduced the <code>&lt;custom-ident&gt;</code>  terminology.
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/syndata.html#counter
|Status=W3C Recommendation
|Relevant_changes=Described solely in the context of counters.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}