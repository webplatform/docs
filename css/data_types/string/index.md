---
title: <string>
code_samples:
  - 'http://gist.github.com/10608944'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;string&gt; CSS data type represents character data surrounded with either single ('') or double (&quot;) quote characters.  Any unicode characters can be included in the string, but many need to be expressed with escape sequences.'
tags:
  - Data
  - Type
uri: 'css/data types/string'

---
## Summary

The &lt;string&gt; CSS data type represents character data surrounded with either single (') or double (&quot;) quote characters. Any unicode characters can be included in the string, but many need to be expressed with escape sequences.

 The CSS escape character is the backslash (**\\**). There are two ways to create an escape sequence:

-   as a backslash followed by the special character (e.g., **\\"** for a double quote or **\\\\** for a backslash);
-   as a backslash followed by a hexadecimal number representing the unicode value (e.g., **\\22** for a double quote, **\\263A** for a smiley face or **\\a** for a line break); either lowercase or uppercase letters may be used for the hexadecimal digits.

Unicode characters may also be entered directly, if the file is saved with the correct encoding and a [`@charset` rule](/css/atrules/@charset) is declared at the top of the stylesheet file (for embedded style blocks, an equivalent charset declaration must be made in the HTML/XML).

The following characters always need to be escaped:

-   quotation marks of the same type used to delimit the string (but single quotes can be used unescaped in a double-quoted string and vice versa);
-   the backslash character;
-   line breaks (see below).

If you wish to break a long string of text across multiple lines in your source code, you can insert a **\\** escape character immediately before the line break. The escaped linebreak is **not** included in the resulting string. To include a line break character in the final string value, you will also need to add a **\\a** escape sequence.

## Examples

**Escape characters in strings**

``` css
body::before {
    content: "Don't you just \A \"\2665\22 \a the live \
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
```

[View live example](http://code.webplatform.org/gist/10608944)

## Related specifications

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#strings)
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#strings)
:   W3C Recommendation

