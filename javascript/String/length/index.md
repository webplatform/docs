{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the length of a '''String''' object.

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
{{JS_Return_Value}}
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
}}
}}
{{Remarks_Section
|Remarks=The '''length''' property contains an integer that indicates the number of characters in the '''String''' object. The last character in the '''String''' object has an index of i '''length''' - 1.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
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