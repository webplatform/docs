{{Page_Title}}
{{Flags}}
{{Summary_Section|Combines two or more arrays.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= array1.concat([ item1 [, item2 [, . . . [, itemN ]]]]) }}
|Values={{JS_Syntax_Parameter
|Name=array1
|Required=Required
|Description=The '''Array''' object to which the other arrays are concatenated.}}{{JS_Syntax_Parameter
|Name=item1,. . ., itemN
|Required=Optional
|Description=Additional items to add to the end of array1.}}
}}
{{Remarks_Section
|Remarks=The '''concat''' method returns an '''Array''' object containing the concatenation of array1 and any other supplied items.

The items to be added ( item1  itemN ) to the array are added, in order, starting from the first item in the list. If one of the items is an array, its contents are added to the end of array1. If the item is anything other than an array, it is added to the end of the array as a single array element.

Elements of source arrays are copied to the resulting array as follows:

* If an object is copied from any of the arrays being concatenated to the new array, the object reference continues to point to the same object. A change in either the new array or the original array will result in a change to the other.
* If a number or string value is added to the new array, only the value is copied. Changing the value in one array does not affect the value in the other.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''concat''' method when used with an array:

|Code= var a, b, c, d;
 a = new Array(1,2,3);
 b = "dog";
 c = new Array(42, "cat");
 d = a.concat(b, c);
 document.write(d);
 
 //Output: 
 1, 2, 3, "dog", 42, "cat"
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String/concat{{!}}concat Method (String)]]
* [[javascript/Array/join{{!}}join Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/2e06zxh0(v=vs.94).aspx
|HTML5Rocks_link=
}}