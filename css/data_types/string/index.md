{{Page_Title|&lt;string&gt;}}
{{Flags
|State=Unreviewed
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{Summary_Section|The <code>&lt;string></code> CSS data type represents character data surrounded with either single ('''&apos;''') or double ('''"''') quote characters.  Any unicode characters can be included in the string, but many need to be expressed with escape sequences.}}
{{Data_Type_Page
|Content=The CSS escape character is the backslash ('''\''').  There are two ways to create an escape sequence: 

* as a backslash followed by the special character (e.g., '''\"''' for a double quote or '''\\''' for a backslash);
* as a backslash followed by a hexadecimal number representing the unicode value (e.g.,  '''\22''' for a double quote, '''\263A''' for a smiley face or '''\a''' for a line break); either lowercase or uppercase letters may be used for the hexadecimal digits. 

Unicode characters may also be entered directly, if the file is saved with the correct encoding and a [[css/atrules/@charset| <code>@charset</code> rule]] is declared at the top of the stylesheet file (for embedded style blocks, an equivalent charset declaration must be made in the HTML/XML).

The following characters always need to be escaped:

* quotation marks of the same type used to delimit the string (but single quotes can be used unescaped in a double-quoted string and vice versa);
* the backslash character;
* line breaks (see below).

If you wish to break a long string of text across multiple lines in your source code, you can insert a '''\''' escape character immediately before the line break.  The escaped linebreak is '''not''' included in the resulting string.  To include a line break character in the final string value, you will also need to add a '''\a''' escape sequence.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description='''Escape characters in strings'''
|Code=body::before {
    content: "Don't you just \A &#92;"&#92;2665&#92;22 \a the live \
              code examples?"; 
/* Displays as:
Don't you just 
"♥" 
the live code examples?
*/

    display:block; 
    white-space:pre-line; 
     /* preserve line breaks but collapse spaces */  
}
|LiveURL=http://code.webplatform.org/gist/10608944
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#strings
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/syndata.html#strings
|Status=W3C Recommendation
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}