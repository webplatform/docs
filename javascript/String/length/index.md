{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the length of a '''String''' object.

'''Caution''' -- JavaScript strings are immutable, so the length of a string cannot be modified.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strVariable.length}}{{JS_Syntax_Format
|Format= "String Literal".length }}
}}
{{Remarks_Section
|Remarks=The '''length''' property contains an integer that indicates the number of characters in the '''String''' object. The last character in the '''String''' object has an index of i '''length''' - 1.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use '''length'''. JavaScript strings are immutable and cannot be modified in place. However, you can write the reversed string to an array and then call '''join''' with the empty character, which produces a string with no separator characters.

|Code= var str = "every good boy does fine";
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
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3d616214(v=vs.94).aspx
|HTML5Rocks_link=
}}