{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Gets or sets the length of the array. This is a number one higher than the highest element defined in an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=numVar = arrayObj.length
}}
|Values={{JS Syntax Parameter
|Name=numVar
|Required=Required
|Description=Any number.
}}{{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=Any '''Array''' object.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=In JavaScript arrays are sparse, and the elements in an array do not have to be contiguous. The '''length''' property is not necessarily the number of elements in the array. For example, in the following array definition, <code>my_array.length</code> contains 7, not 2:

 var my_array = new Array( );
 my_array[0] = "Test";
 my_array[6] = "Another Test";
If you make the '''length''' property smaller than its previous value, the array is truncated, and any elements with array indexes equal to or greater than the new value of the '''length''' property are lost.

If you make the length property larger than its previous value, the array is expanded, and any new elements created have the value undefined.

The following example illustrates the use of the '''length''' property:

 var a;
 a = new Array(0,1,2,3,4);
 document.write(a.length);
 
 // Output
 // 5
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Property
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d8ez24f2(v=vs.94).aspx
|HTML5Rocks_link=
}}