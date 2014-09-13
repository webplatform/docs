{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns the codepoint length of a '''String''' object.

'''Caution''' -- JavaScript strings are immutable, so the length of a string cannot be modified.
}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=strVariable.length
}}{{JS Syntax Format
|Format="String Literal".length
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use '''length'''. JavaScript strings are immutable and cannot be modified in place. However, you can write the reversed string to an array and then call '''join''' with the empty character, which produces a string with no separator characters.
|Code=var str = "every good boy does fine";
         var start = 0;
         var end = str.length - 1;
         var tmp = "";
         var arr = new Array(end);
 
         while (end &gt;= 0) {
             arr[start++] = str.charAt(end--);
         }
 
 // Join the elements of the array with a 
         var str2 = arr.join('');
         document.write(str2);
 
 // Output: enif seod yob doog yreve
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The '''length''' property contains an integer that indicates the number of characters in the '''String''' object. The last character in the '''String''' object has an index of i '''length''' - 1.
}}
{{Notes_Section
|Usage=Use this property to get the codepoint length of a '''String''' object.
|Notes=*A codepoint length is the number of unicode codepoints that represent the value. While most of the characters are represented using a single codepoint, rarely used characters from little used languages are represented using two codepoints, which simplistically means that such a character is technically a combination of two character.
*Because a codepoint can consist of more than a single byte, the codepoint length of a string is not necessarily equal to the number of bytes used for the string. For example, in UTF-8 (the emerging standard encoding of the web), Hebrew characters consist of 2 bytes, so the size of a string that only includes 2 Hebrew characters is actually 4 bytes, but its codepoint length is 2.
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3d616214(v=vs.94).aspx
|HTML5Rocks_link=
}}