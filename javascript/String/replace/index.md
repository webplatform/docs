{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Replaces text in a string, using a regular expression or search string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=stringObj. replace( rgExp , replaceText )
}}
|Values={{JS Syntax Parameter
|Name=stringObj
|Required=Required
|Description=The String object or string literal on which to perform the replacement. This string is not modified by the '''replace''' method. Rather, the return value of this method is the string produced by the replacement.
}}{{JS Syntax Parameter
|Name=rgExp
|Required=Required
|Description=An instance of a '''Regular Expression''' object containing the regular expression pattern and applicable flags. Can also be a String object or string literal that represents the regular expression. If rgExp is not an instance of a '''Regular Expression''' object, it is converted to a string, and an exact search is made for the results; no attempt is made to convert the string into a regular expression.
}}{{JS Syntax Parameter
|Name=replaceText
|Required=Required
|Description=A String object or string literal containing the text to replace for every successful match of rgExp in stringObj. In Internet Explorer 5.5 or later, the replaceText argument can also be a function that returns the replacement text.
}}
}}
{{JS_Return_Value
|Description=The result of the '''replace''' method is a copy of stringObj after the specified replacements have been made.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''replace''' method to replace all instances of "the" with "a."
|Code=var s = "the batter hit the ball with the bat";
 
 // Replace "the" with "a".
 var re = /the/g;
 var result = s.replace(re, "a");
 document.write(result);
 // Output: a batter hit a ball with a bat
}}{{Single Example
|Language=JavaScript
|Description=In addition, the '''replace''' method can also replace subexpressions in the pattern. The following example exchanges each pair of words in the string.
|Code=var s = "The quick brown fox jumped over the lazy dog.";
 var re = /(\S+)(\s+)(\S+)/g;
 // Exchange each pair of words.
 var result = s.replace(re, "");
 document.write(result);
 
 // Output:  quick The fox brown over jumps lazy the dog.
}}{{Single Example
|Language=JavaScript
|Description=The following example, which works in JavaScript 5.5 and later, shows how to use a function that returns the replacement text. It replaces any instance of a number followed by "F" with a Celsius conversion.
|Code=function f2c(s1) {
     // Initialize pattern.
     var test = /(\d+(\.\d*)?)F\b/g;
 
     // Use a function for the replacement.
     var s2 = s1.replace(test,
       function(		<div class="multipleTemplateStarter" style="display: none">			<table>
			<tr>
			<td> 
</p>
<table class="formtable">

<tr>
<th> Language (for syntax highlighting, use HTML for XML):
</th>
<td> <span class="inputSpan"><select id="input_38" tabindex="11" name="Single Example[num][Language]" class="createboxInput">	<option value=""></option>
<option value="HTML">HTML</option><option value="CSS">CSS</option><option value="JavaScript">JavaScript</option><option value="Other">Other</option></select></span>
</td></tr>
<tr>
<th> Description (optional; comments in code preferred):
</th>
<td> <span class="inputSpan"><textarea tabindex="11" name="Single Example[num][Description]" id="input_39" class="createboxInput" rows="3" cols="90" style="width: 100%">
}}
}}
{{Remarks_Section
|Remarks=Any of the following match variables can be used to identify the most recent match and the string from which it came. The match variables can be used in text replacement where the replacement string has to be determined dynamically.

{{{!}} class='wikitable'
{{!}}-
! Characters
! Meaning
{{!}}-
{{!}} '''$$'''
{{!}} $ (Internet Explorer 5.5 or later)
{{!}}-
{{!}} '''$&amp;'''
{{!}} Specifies that portion of stringObj that the entire pattern matched. (Internet Explorer 5.5 or later)
{{!}}-
{{!}} '''$`'''
{{!}} Specifies that portion of stringObj that precedes the match described by '''$&amp;'''. (Internet Explorer 5.5 or later)
{{!}}-
{{!}} '''$''''
{{!}} Specifies that portion of stringObj that follows the match described by '''$&amp;'''. (Internet Explorer 5.5 or later)
{{!}}-
{{!}} $ n
{{!}} The n th captured submatch, where n is a single decimal digit from 1 through 9. (Internet Explorer 5.5 or later)
{{!}}-
{{!}} $ nn
{{!}} The nn th captured submatch, where nn is a two-digit decimal number from 01 through 99. (Internet Explorer 5.5 or later)
{{!}}} 
If replaceText is a function, for each matched substring the function is called with the following m + 3 arguments where m is the number of left capturing parentheses in the rgExp. The first argument is the substring that matched. The next m arguments are all of the captures that resulted from the search. Argument m + 2 is the offset within stringObj where the match occurred, and argument m + 3 is stringObj. The result is the string value that results from replacing each matched substring with the corresponding return value of the function call.

The '''replace''' method updates the properties of the global '''RegExp''' object.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/exec{{!}}exec Method (Regular Expression)]]
* [[javascript/String/match{{!}}match Method (String)]]
* [[javascript/RegExp{{!}}RegExp Object]]
* [[javascript/String/search{{!}}search Method (String)]]
* [[javascript/regular expression/test{{!}}test Method (Regular Expression)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t0kbytzc(v=vs.94).aspx
|HTML5Rocks_link=
}}