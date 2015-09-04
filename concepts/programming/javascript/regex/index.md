---
title: regex
tags:
  - JavaScript
readiness: 'Not Ready'
uri: concepts/programming/javascript/regex
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/regex/js/objects/RegExp
    - concepts/programming/javascript/regex/js
    - concepts/programming/javascript/regex/js/objects/RegExp/exec
    - concepts/programming/javascript/regex/js/objects/RegExp/test
    - concepts/programming/javascript/regex/js/objects/String/match
    - concepts/programming/javascript/regex/js/objects/String/search
    - concepts/programming/javascript/regex/js/objects/String/replace
    - concepts/programming/javascript/regex/js/objects/String/split

---
# Regular Expressions

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Creating a Regular Expression

You construct a regular expression in one of two ways:

-   Using a regular expression literal, as follows:

        var re = /ab+c/;

    Regular expression literals provide compilation of the regular expression when the script is evaluated. When the regular expression will remain constant, use this for better performance.

-   Calling the constructor function of the `RegExp` object, as follows:

        var re = new RegExp("ab+c");

    Using the constructor function provides runtime compilation of the regular expression. Use the constructor function when you know the regular expression pattern will be changing, or you don't know the pattern and are getting it from another source, such as user input.

## Writing a Regular Expression Pattern

A regular expression pattern is composed of simple characters, such as `/abc/`, or a combination of simple and special characters, such as `/ab*c/` or `/Chapter (\d+)\.\d*/`. The last example includes parentheses which are used as a memory device. The match made with this part of the pattern is remembered for later use, as described in [Using Parenthesized Substring Matches](#Using_Parenthesized_Substring_Matches).

### Using Simple Patterns

Simple patterns are constructed of characters for which you want to find a direct match. For example, the pattern `/abc/` matches character combinations in strings only when exactly the characters 'abc' occur together and in that order. Such a match would succeed in the strings "Hi, do you know your abc's?" and "The latest airplane designs evolved from slabcraft." In both cases the match is with the substring 'abc'. There is no match in the string "Grab crab" because it does not contain the substring 'abc'.

### Using Special Characters

When the search for a match requires something more than a direct match, such as finding one or more b's, or finding white space, the pattern includes special characters. For example, the pattern `/ab*c/` matches any character combination in which a single 'a' is followed by zero or more 'b's (`*` means 0 or more occurrences of the preceding item) and then immediately followed by 'c'. In the string "cbbabbbbcdebc," the pattern matches the substring 'abbbbc'.

The following table provides a complete list and description of the special characters that can be used in regular expressions.

<table>
<caption>
Table 4.1 Special characters in regular expressions.

</caption>
<tr>
<th scope="col">
Character

</th>
<th style="text-align:left;" scope="col">
Meaning

</th>
</tr>
<tr>
<th scope="row" id="special-backslash">
`\`

</th>
<td>
Either of the following:

-   For characters that are usually treated literally, indicates that the next character is special and not to be interpreted literally.
     `/b/`
    :   matches the character "*b*". By placing a backslash in front of *b*, that is by using `/\b/`, the character becomes special to mean match a word boundary.

-   For characters that are usually treated specially, indicates that the next character is not special and should be interpreted literally.
     `*`
    :   is a special character that means 0 or more occurrences of the preceding item should be matched; for example, `/a*/` means match 0 or more a's. To match `*` literally, precede it with a backslash; for example, `/a\*/` matches 'a\*'.
     Also
    :   do not forget to escape \\ itself while using the `new RegExp("pattern")` notation since `\` is also an escape character in strings.

</td>
</tr>
<tr>
<th scope="row" id="special-caret">
`^`

</th>
<td>
-   Matches beginning of input. If the multiline flag is set to true, also matches immediately after a line break character.
-   For example;
     `/^A/`
    :   does not match the 'A' in "an A", but does match the 'A' in "An E". This character means 'not' when it appears as the first character in a character set pattern.
     `/[^A-Za-z\s]/`
    :   matches any character that is not a letter or whitespace, and so would match the '3' in "I have 3 sisters".

</td>
</tr>
<tr>
<th scope="row" id="special-dollar">
`$`

</th>
<td>
-   Matches end of input. If the multiline flag is set to true, also matches immediately before a line break character.
-   For example;
     `/t$/`
    :   does not match the 't' in "eater", but does match it in "eat".

</td>
</tr>
<tr>
<th scope="row" id="special-asterisk">
`*`

</th>
<td>
-   Matches the preceding character 0 or more times.
-   For example;
     `/bo*/`
    :   matches 'boooo' in "A ghost booooed" and "*b*" in "A bird warbled", but nothing in "A goat grunted".

</td>
</tr>
<tr>
<th scope="row" id="special-plus">
`+`

</th>
<td>
-   Matches the preceding character 1 or more times. Equivalent to `{1,}`
-   For example;
     `/a+/`
    :   matches the 'a' in "candy" and all the a's in "caaaaaaandy".

</td>
</tr>
<tr>
<th scope="row" id="special-questionmark">
`?`

</th>
<td>
-   Matches the preceding character 0 or 1 time. Equivalent to {0,1}.
-   For example;
     `/e?le?/`
    :   matches the 'el' in "angel" and the 'le' in "angle" and also the 'l' in "oslo".
    �
    :   If used immediately after any of the quantifiers `*`, `+`, `?`, or `{}`, makes the quantifier non-greedy (matching the minimum number of times), as opposed to the default, which is greedy (matching the maximum number of times).
     `/\d+/` non-global
    :   match "123abc" return "123", if using /\\d+?/, only "1" will be matched.

-   Also used in lookahead assertions, described under x(?=y) and x(?!y) in this table.\</p\>

</td>
</tr>
<tr>
<th scope="row" id="special-dot">
`.`

</th>
<td>
-   (The decimal point) matches any single character except the newline character.
-   For example;
     `/.n/`
    :   matches 'an' and 'on' in "nay, an apple is on the tree", but not 'nay'.

</td>
</tr>
<tr>
<th scope="row" id="special-capturing-parentheses">
`(x)`

</th>
<td>
-   Matches 'x' and remembers the match. These are called capturing parentheses.
-   For example;
     `/(foo)/`
    :   matches and remembers 'foo' in "foo bar." The matched substring can be recalled from the resulting array's elements `[1]`, ..., `[n]`.

</td>
</tr>
<tr>
<th scope="row" id="special-non-capturing-parentheses">
`(?:x)`

</th>
<td>
-   Matches 'x' but does not remember the match. These are called non-capturing parentheses. The matched substring can not be recalled from the resulting array's elements `[1]`, ..., `[n]`

</td>
</tr>
<tr>
<th scope="row" id="special-lookahead">
`x(?=y)`

</th>
<td>
-   Matches 'x' only if 'x' is followed by 'y'. This is called a lookahead.
-   For example;
     `/Jack(?=Sprat)/`
    :   matches 'Jack' only if it is followed by 'Sprat'. `/Jack(?=Sprat|Frost)/` matches 'Jack' only if it is followed by 'Sprat' or 'Frost'. However, neither 'Sprat' nor 'Frost' is part of the match results.

</td>
</tr>
<tr>
<th scope="row" id="special-negated-look-ahead">
`x(?!y)`

</th>
<td>
-   Matches 'x' only if 'x' is not followed by 'y'. This is called a negated lookahead.
-   For example;
     `/\d+(?!\.)/`
    :   matches a number only if it is not followed by a decimal point. The regular expression `/\d+(?!\.)/.exec("3.141")` matches '`141`' but not '`3.141`'.

</td>
</tr>
<tr>
<th scope="row" id="special-or">
`x|y`

</th>
<td>
-   Matches either 'x' or 'y'.
-   For example;
     `/green|red/`
    :   matches 'green' in "green apple" and 'red' in "red apple."

</td>
</tr>
<tr>
<th scope="row" id="special-quantifier">
`{n}`

</th>
<td>
-   Where `n` is a positive integer. Matches exactly `n` occurrences of the preceding character.
-   For example;
     `/a{2}/`
    :   doesn't match the 'a' in "candy," but it matches all of the a's in "caandy," and the first two a's in "caaandy."

</td>
</tr>
<tr>
<th scope="row" id="special-quantifier-range">
`{n,m}`

</th>
<td>
-   Where `n` and `m` are positive integers. Matches at least `n` and at most `m` occurrences of the preceding character. When either `n` or `m` is zero, it can be omitted.
-   For example;
     `/a{1,3}/`
    :   matches nothing in "cndy", the 'a' in "candy," the first two a's in "caandy," and the first three a's in "caaaaaaandy" Notice that when matching "caaaaaaandy", the match is "aaa", even though the original string had more a's in it.

</td>
</tr>
<tr>
<th scope="row" id="special-character-set">
`[xyz]`

</th>
<td>
-   A character set. Matches any one of the enclosed characters. You can specify a range of characters by using a hyphen. Special characters (such as the dot (`.`) and the asterisk (`*`)) do not have any special meaning inside a character set. They need not be escaped. Escape sequences also work.
-   For example;
     `[abcd]`
    :   is the same as `[a-d]`. They match the 'b' in "brisket" and the 'c' in "city". `/[a-z.]+/` and `/[\w.]+/` both match everything in "`test.i.ng`".

</td>
</tr>
<tr>
<th scope="row" id="special-negated-character-set">
`[^xyz]`

</th>
<td>
-   A negated or complemented character set. That is, it matches anything that is not enclosed in the brackets. You can specify a range of characters by using a hyphen. Everything that works in the normal character set also works here.
-   For example;
     `[^abc]`
    :   is the same as `[^a-c]`. They initially match 'r' in "brisket" and 'h' in "chop."

</td>
</tr>
<tr>
<th scope="row" id="special-backspace">
`[\b]`

</th>
<td>
-   Matches a backspace `(U+0008)`. (Not to be confused with `\b`.)

</td>
</tr>
<tr>
<th scope="row" id="special-word-boundary">
`\b`

</th>
<td>
-   Matches a word boundary. A word boundary matches the position where a word character is not followed or preceeded by another word-character. Note that a matched word boundary is not included in the match. In other words, the length of a matched word boundary is zero. (Not to be confused with `[\b]`.)
-   For example;
     `/\bmoo/`
    :   matches the 'moo' in "moon"
     `/oo\b/`
    :   does not match the 'oo' in "moon", because 'oo' is followed by 'n' which is a word character;
     `/oon\b/`
    :   matches the 'oon' in "moon", because 'oon' is the end of the string, thus not followed by a word character;
     `/\w\b\w/`
    :   will never match anything, because a word character can never be followed by both a non-word and a word character.

</td>
</tr>
<tr>
<th scope="row" id="special-non-word-boundary">
`\B`

</th>
<td>
-   Matches a non-word boundary. This matches a position where the previous and next character are of the same type: Either both must be words, or both must be non-words. The beginning and end of a string are considered non-words.
-   For example;
     `/\B../`
    :   matches 'oo' in "noonday"
     `/y\B./`
    :   matches 'ye' in "possibly yesterday."

</td>
</tr>
<tr>
<th scope="row" id="special-control">
`\cX`

</th>
<td>
-   Where *X* is a character ranging from A to Z. Matches a control character in a string.
-   For example;
     `/\cM/`
    :   matches control-M (U+000D) in a string.

</td>
</tr>
<tr>
<th scope="row" id="special-digit">
`\d`

</th>
<td>
\* Matches a digit character. Equivalent to `[0-9]`.

-   For example;
     `/\d/` or `/[0-9]/`
    :   matches '2' in "B2 is the suite number."

</td>
</tr>
<tr>
<th scope="row" id="special-non-digit">
`\D`

</th>
<td>
-   Matches any non-digit character. Equivalent to `[^0-9]`.
-   For example;
     `/\D/` or `/[^0-9]/`
    :   matches 'B' in "B2 is the suite number."

</td>
</tr>
<tr>
<th scope="row" id="special-form-feed">
`\f`

</th>
<td>
-   Matches a form feed `(U+000C)`.

</td>
</tr>
<tr>
<th scope="row" id="special-line-feed">
`\n`

</th>
<td>
-   Matches a line feed `(U+000A)`.

</td>
</tr>
<tr>
<th scope="row" id="special-carriage-return">
`\r`

</th>
<td>
\* Matches a carriage return (U+000D).

</td>
</tr>
<tr>
<th scope="row" id="special-white-space">
`\s`

</th>
<td>
-   Matches a single white space character, including space, tab, form feed, line feed. Equivalent to `[ \f\n\r\t\v​\u00A0\u1680​\u180e\u2000​\u2001\u2002​\u2003\u2004​\u2005\u2006​\u2007\u2008​\u2009\u200a​\u2028\u2029​\u2028\u2029​\u202f\u205f​\u3000]`.
-   For example;
     `/\s\w*/`
    :   matches ' bar' in "foo bar."

</td>
</tr>
<tr>
<th scope="row" id="special-non-white-space">
`\S`

</th>
<td>
-   Matches a single character other than white space. Equivalent to `[^ \f\n\r\t\v​\u00A0\u1680​\u180e\u2000​\u2001\u2002​\u2003\u2004​\u2005\u2006​\u2007\u2008​\u2009\u200a​\u2028\u2029​\u2028\u2029​\u202f\u205f​\u3000]`.
-   For example;
     `/\S\w*/`
    :   matches 'foo' in "foo bar."

</td>
</tr>
<tr>
<th scope="row" id="special-tab">
`\t`

</th>
<td>
-   Matches a tab `(U+0009)`.

</td>
</tr>
<tr>
<th scope="row" id="special-vertical-tab">
`\v`

</th>
<td>
-   Matches a vertical tab `(U+000B)`.

</td>
</tr>
<tr>
<th scope="row" id="special-word">
`\w`

</th>
<td>
-   Matches any alphanumeric character including the underscore. Equivalent to `[A-Za-z0-9_]`.
-   For example;
     `/\w/`
    :   matches 'a' in "apple," '5' in "\$5.28," and '3' in "3D."

</td>
</tr>
<tr>
<th scope="row" id="special-non-word">
`\W`

</th>
<td>
-   Matches any non-word character. Equivalent to `[^A-Za-z0-9_]`.
-   For example;
     `/\W/` or `/[^A-Za-z0-9_]/`
    :   matches '%' in "50%."

</td>
</tr>
<tr>
<th scope="row" id="special-backreference">
`\n`

</th>
<td>
-   Where *n* is a positive integer. A back reference to the last substring matching the *n* parenthetical in the regular expression (counting left parentheses).
-   For example;
     `/apple(,)\sorange\1/`
    :   matches 'apple, orange,' in "apple, orange, cherry, peach."

</td>
</tr>
<tr>
<th scope="row" id="special-null">
`\0`

</th>
<td>
-   Matches a NULL (U+0000) character. Do not follow this with another digit, because `\0<digits>` is an octal escape sequence.

</td>
</tr>
<tr>
<th scope="row" id="special-hex-escape">
`\xhh`

</th>
<td>
-   Matches the character with the code hh (two hexadecimal digits)

</td>
</tr>
<tr>
<th scope="row" id="special-unicode-escape">
`\uhhhh`

</th>
<td>
-   Matches the character with the code hhhh (four hexadecimal digits).

</td>
</tr>
</table>
### Using Parentheses

Parentheses around any part of the regular expression pattern cause that part of the matched substring to be remembered. Once remembered, the substring can be recalled for other use, as described in [Using Parenthesized Substring Matches](#Using_Parenthesized_Substring_Matches).

For example, the pattern `/Chapter (\d+)\.\d*/` illustrates additional escaped and special characters and indicates that part of the pattern should be remembered. It matches precisely the characters 'Chapter ' followed by one or more numeric characters (`\d` means any numeric character and `+` means 1 or more times), followed by a decimal point (which in itself is a special character; preceding the decimal point with \\ means the pattern must look for the literal character '.'), followed by any numeric character 0 or more times (`\d` means numeric character, `*` means 0 or more times). In addition, parentheses are used to remember the first matched numeric characters.

This pattern is found in "Open Chapter 4.3, paragraph 6" and '4' is remembered. The pattern is not found in "Chapter 3 and 4", because that string does not have a period after the '3'.

To match a substring without causing the matched part to be remembered, within the parentheses preface the pattern with `?:`. For example, `(?:\d+)` matches one or more numeric characters but does not remember the matched characters.

## Working with Regular Expressions

Regular expressions are used with the `RegExp` methods `test` and `exec` and with the `String` methods `match`, `replace`, `search`, and `split`. These methods are explained in detail in the [JavaScript Reference](/w/index.php?title=concepts/programming/javascript/regex/js&action=edit&redlink=1).

<table class="standard-table">
<caption style="text-align: left">
Table 4.2 Methods that use regular expressions

</caption>
\<thead\>

<tr>
<th scope="col">
Method

</th>
<th scope="col">
Description

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`exec`

</td>
<td>
A `RegExp` method that executes a search for a match in a string. It returns an array of information.

</td>
</tr>
<tr>
<td>
`test`

</td>
<td>
A `RegExp` method that tests for a match in a string. It returns true or false.

</td>
</tr>
<tr>
<td>
`match`

</td>
<td>
A `String` method that executes a search for a match in a string. It returns an array of information or null on a mismatch.

</td>
</tr>
<tr>
<td>
`search`

</td>
<td>
A `String` method that tests for a match in a string. It returns the index of the match, or -1 if the search fails.

</td>
</tr>
<tr>
<td>
`replace`

</td>
<td>
A `String` method that executes a search for a match in a string, and replaces the matched substring with a replacement substring.

</td>
</tr>
<tr>
<td>
`split`

</td>
<td>
A `String` method that uses a regular expression or a fixed string to break a string into an array of substrings.

</td>
</tr>
\</tbody\>

</table>
When you want to know whether a pattern is found in a string, use the `test` or `search` method; for more information (but slower execution) use the `exec` or `match` methods. If you use `exec` or `match` and if the match succeeds, these methods return an array and update properties of the associated regular expression object and also of the predefined regular expression object, `RegExp`. If the match fails, the `exec` method returns `null` (which converts to `false`).

In the following example, the script uses the `exec` method to find a match in a string.

    var myRe = /d(b+)d/g;
    var myArray = myRe.exec("cdbbdbsbz");

If you do not need to access the properties of the regular expression, an alternative way of creating `myArray` is with this script:

    var myArray = /d(b+)d/g.exec("cdbbdbsbz");

If you want to construct the regular expression from a string, yet another alternative is this script:

    var myRe = new RegExp("d(b+)d", "g");
    var myArray = myRe.exec("cdbbdbsbz");

With these scripts, the match succeeds and returns the array and updates the properties shown in the following table.

<table>
<caption style="text-align: left">
Table 4.3 Results of regular expression execution.

</caption>
\<thead\>

<tr>
<th scope="col">
Object

</th>
<th scope="col">
Property or index

</th>
<th scope="col">
Description

</th>
<th scope="col">
In this example

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td rowspan="4">
`myArray`

</td>
<td>
�

</td>
<td>
The matched string and all remembered substrings.

</td>
<td>
`["dbbd", "bb"]`

</td>
</tr>
<tr>
<td>
`index`

</td>
<td>
The 0-based index of the match in the input string.

</td>
<td>
`1`

</td>
</tr>
<tr>
<td>
`input`

</td>
<td>
The original string.

</td>
<td>
`"cdbbdbsbz"`

</td>
</tr>
<tr>
<td>
`[0]`

</td>
<td>
The last matched characters.

</td>
<td>
`"dbbd"`

</td>
</tr>
<tr>
<td rowspan="2">
`myRe`

</td>
<td>
`lastIndex`

</td>
<td>
The index at which to start the next match. (This property is set only if the regular expression uses the g option, described in [Advanced Searching With Flags](#Advanced_Searching_With_Flags).)

</td>
<td>
`5`

</td>
</tr>
<tr>
<td>
`source`

</td>
<td>
The text of the pattern. Updated at the time that the regular expression is created, not executed.

</td>
<td>
`"d(b+)d"`

</td>
</tr>
\</tbody\>

</table>
As shown in the second form of this example, you can use a regular expression created with an object initializer without assigning it to a variable. If you do, however, every occurrence is a new regular expression. For this reason, if you use this form without assigning it to a variable, you cannot subsequently access the properties of that regular expression. For example, assume you have this script:

    var myRe = /d(b+)d/g;
    var myArray = myRe.exec("cdbbdbsbz");
    console.log("The value of lastIndex is " + myRe.lastIndex);

This script displays:

    The value of lastIndex is 5

However, if you have this script:

    var myArray = /d(b+)d/g.exec("cdbbdbsbz");
    console.log("The value of lastIndex is " + /d(b+)d/g.lastIndex);

It displays:

    The value of lastIndex is 0

The occurrences of `/d(b+)d/g` in the two statements are different regular expression objects and hence have different values for their `lastIndex` property. If you need to access the properties of a regular expression created with an object initializer, you should first assign it to a variable.

### Using Parenthesized Substring Matches

Including parentheses in a regular expression pattern causes the corresponding submatch to be remembered. For example, `/a(b)c/` matches the characters 'abc' and remembers 'b'. To recall these parenthesized substring matches, use the `Array` elements `[1]`, ..., `[n]`.

The number of possible parenthesized substrings is unlimited. The returned array holds all that were found. The following examples illustrate how to use parenthesized substring matches.

#### Example 1

The following script uses the `replace()` method to switch the words in the string. For the replacement text, the script uses the `$1` and `$2` in the replacement to denote the first and second parenthesized substring matches.

    var re = /(\w+)\s(\w+)/;
    var str = "John Smith";
    var newstr = str.replace(re, "$2, $1");
    console.log(newstr);

This prints "Smith, John".

### Advanced Searching With Flags

Regular expressions have four optional flags that allow for global and case insensitive searching. To indicate a global search, use the `g` flag. To indicate a case-insensitive search, use the `i` flag. To indicate a multi-line search, use the `m` flag. To perform a "sticky" search, that matches starting at the current position in the target string, use the `y` flag. These flags can be used separately or together in any order, and are included as part of the regular expression.

To include a flag with the regular expression, use this syntax:

    var re = /pattern/flags;

or

    var re = new RegExp("pattern", "flags");

Note that the flags are an integral part of a regular expression. They cannot be added or removed later.

For example, `re = /\w+\s/g` creates a regular expression that looks for one or more characters followed by a space, and it looks for this combination throughout the string.

    var re = /\w+\s/g;
    var str = "fee fi fo fum";
    var myArray = str.match(re);
    console.log(myArray);

This displays ["fee ", "fi ", "fo "]. In this example, you could replace the line:

    var re = /\w+\s/g;

with:

    var re = new RegExp("\\w+\\s", "g");

and get the same result.

The `m` flag is used to specify that a multiline input string should be treated as multiple lines. If the `m` flag is used, `^` and `$` match at the start or end of any line within the input string instead of the start or end of the entire string.

## Examples

The following examples show some uses of regular expressions.

### Changing the Order in an Input String

The following example illustrates the formation of regular expressions and the use of `string.split()` and `string.replace()`. It cleans a roughly formatted input string containing names (first name first) separated by blanks, tabs and exactly one semicolon. Finally, it reverses the name order (last name first) and sorts the list.

``` {.js}
// The name string contains multiple spaces and tabs,
// and may have multiple spaces between first and last names.
var names = "Harry Trump ;Fred Barney; Helen Rigby ; Bill Abel ; Chris Hand ";

var output = ["---------- Original String\n", names + "\n"];

// Prepare two regular expression patterns and array storage.
// Split the string into array elements.

// pattern: possible white space then semicolon then possible white space
var pattern = /\s*;\s*/;

// Break the string into pieces separated by the pattern above and
// store the pieces in an array called nameList
var nameList = names.split(pattern);

// new pattern: one or more characters then spaces then characters.
// Use parentheses to "memorize" portions of the pattern.
// The memorized portions are referred to later.
pattern = /(\w+)\s+(\w+)/;

// New array for holding names being processed.
var bySurnameList = [];

// Display the name array and populate the new array
// with comma-separated names, last first.
//
// The replace method removes anything matching the pattern
// and replaces it with the memorized string—second memorized portion
// followed by comma space followed by first memorized portion.
//
// The variables $1 and $2 refer to the portions
// memorized while matching the pattern.

output.push("---------- After Split by Regular Expression");

var i, len;
for (i = 0, len = nameList.length; i &lt; len; i++){
  output.push(nameList[i]);
  bySurnameList[i] = nameList[i].replace(pattern, "$2, $1");
}

// Display the new array.
output.push("---------- Names Reversed");
for (i = 0, len = bySurnameList.length; i &lt; len; i++){
  output.push(bySurnameList[i]);
}

// Sort by last name, then display the sorted array.
bySurnameList.sort();
output.push("---------- Sorted");
for (i = 0, len = bySurnameList.length; i &lt; len; i++){
  output.push(bySurnameList[i]);
}

output.push("---------- End");

console.log(output.join("\n"));
```

### Using Special Characters to Verify Input

In the following example, the user is expected to enter a phone number. When the user presses the "Check" button, the script checks the validity of the number. If the number is valid (matches the character sequence specified by the regular expression), the script shows a message thanking the user and confirming the number. If the number is invalid, the script informs the user that the phone number is not valid at all.

The regular expression looks for zero or one open parenthesis `\(?`, followed by three digits` \d{3}`, followed by zero or one close parenthesis `\)?`, followed by one dash, forward slash, or decimal point and when found, remember the character `([-\/\.])`, followed by three digits `\d{3}`, followed by the remembered match of a dash, forward slash, or decimal point `\1`, followed by four digits `\d{4}`.

The `Change` event activated when the user presses Enter sets the value of `RegExp.input`.

    <!DOCTYPE html>
    <html>
      <head>
        <meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
        <meta http-equiv="Content-Script-Type" content="text/javascript">
        <script type="text/javascript">
          var re = /\(?\d{3}\)?([-\/\.])\d{3}\1\d{4}/;
          function testInfo(phoneInput){
            var OK = re.exec(phoneInput.value);
            if (!OK)
              window.alert(RegExp.input + " isn't a phone number with area code!");
            else
              window.alert("Thanks, your phone number is " + OK[0]);
          }
        </script>
      </head>
      <body>
        <p>Enter your phone number (with area code) and then click "Check".
            <br>The expected format is like ###-###-####.</p>
        <form action="#">
          <input id="phone"><button onclick="testInfo(document.getElementById('phone'));">Check</button>
        </form>
      </body>
    </html>

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Regular_Expressions)

