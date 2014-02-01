{{Page_Title}}
{{Flags}}
{{Summary_Section|Contains information about errors.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= errorObj = new Error()}}{{JS_Syntax_Format
|Format= errorObj = new Error([ number ])}}{{JS_Syntax_Format
|Format= errorObj = new Error([ number [, description ]])}}
|Values={{JS_Syntax_Parameter
|Name=errorObj
|Required=Required
|Description=The variable name to which the Error object is assigned.}}{{JS_Syntax_Parameter
|Name=number
|Required=Optional
|Description=Numeric value assigned to an error. Zero if omitted.}}{{JS_Syntax_Parameter
|Name=description
|Required=Optional
|Description=Brief string that describes an error. Empty string if omitted.}}
}}
{{Remarks_Section
|Remarks=Whenever a run-time error occurs, an instance of the Error object is created to describe the error. This instance has two intrinsic properties that contain the description of the error ( '''description''' property) and the error number ( '''number''' property).

An error number is a 32-bit value. The upper 16-bit word is the facility code, while the lower word is the actual error code.

Error objects can also be explicitly created, using the syntax shown above, or thrown using the throw statement. In both cases, you can add any properties you choose to expand the capability of the Error object.

Typically, the local variable that is created in a '''try...catch''' statement refers to the implicitly created Error object. As a result, you can use the error number and description in any way you choose.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the Error object.

|Code= function checkInput(x) {
     try
     {
         if (isNaN(parseInt(x))) {
             throw new Error("Input is not a number.");
         }
     }
     catch(e)
     {
         document.write(e.description);
     }
 }
}}{{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the implicitly created Error object.

|Code= try
    {
    // Cause an error.
    x = y;
    }
 catch(e)
    {
       document.write(e);
       document.write ("&lt;br /&gt;");
 
       document.write ("Number: ");
       document.write (e.number &amp; 0xFFFF);
       document.write ("&lt;br /&gt;");
 
       document.write ("Facility Code: ");
       document.write(e.number&gt;&gt;16 &amp; 0x1FFF);
       document.write ("&lt;br /&gt;");
 
       document.write ("Description: ");
       document.write (e.description);
    }
 
 // Output:
 // ReferenceError: 'y' is undefined
 // Facility Code: 10
 // Number: 5009
 // Description: 'y' is undefined
}}}}
==Methods==
[[javascript/Error/toString|toString Method (Error)]] {{!}} [[javascript/Date/valueOf|valueOf Method (Date)]]
==Properties==
[[javascript/Error/constructor|constructor Property (Error)]] {{!}} [[javascript/Error/description|number Property]] {{!}} [[javascript/Error/prototype|prototype Property (Error)]] {{!}} [[javascript/Error/stack|stack Property (Error)]] {{!}} [[javascript/Error/stackTraceLimit|stackTraceLimit Property (Error)]]
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
* [[javascript/statements/throw{{!}}throw Statement]]
* [[javascript/statements/try catch finally{{!}}try...catch...finally Statement]]
* [[javascript/statements/var{{!}}var Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dww52sbt(v=vs.94).aspx
|HTML5Rocks_link=
}}