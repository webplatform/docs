{{Page_Title}}
{{Flags}}
{{Summary_Section|Removes the last element from an array and returns it.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= arrayObj.pop( )}}
}}
{{Remarks_Section
|Remarks=The [[javascript/Array/push{{!}}push]] and '''pop''' methods enable you to simulate a stack, which uses the principle of last in, first out (LIFO) to store data.

The required arrayObj reference is an '''Array''' object.

If the array is empty, undefined is returned.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the pop method.

|Code= var number;
 var my_array = new Array();
 
 my_array.push (5, 6, 7);
 my_array.push (8, 9);
 
 number = my_array.pop();
 while (number != undefined)
    {
    document.write (number + " ");
    number = my_array.pop();
    }
 
 // Output: 9 8 7 6 5
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/push{{!}}push Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hx9fbx10(v=vs.94).aspx
|HTML5Rocks_link=
}}