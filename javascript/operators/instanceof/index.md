{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value that indicates whether or not an object is an instance of a particular class.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result = object instanceof class}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=Required
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=Any object expression.}}{{JS_Syntax_Parameter
|Name=class
|Required=Required
|Description=Any defined object class.}}
}}
{{Remarks_Section
|Remarks=The '''instanceof''' operator returns true if object is an instance of class. It returns false if object is not an instance of class , or if object is null.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''instanceof''' operator.

|Code= function objTest(obj){
     var i, t, s = "";
     t = new Array();
     t["Date"] = Date;
     t["Object"] = Object;
     t["Array"] = Array;
         for (i in t){
             if (obj instanceof t[i]) { 
                 s += "obj is an instance of " + i + "&lt;br/&gt;";
             }
             else {
                 s += "obj is not an instance of " + i + "&lt;br/&gt;";
         }
     }
     return(s);
 }
 
 var obj = new Date();
 document.write(objTest(obj));
 
 // Output: 
 // obj is an instance of Date
 // obj is an instance of Object
 // obj is not an instance of Array
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/zh0zb36z(v=vs.94).aspx
|HTML5Rocks_link=
}}