{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Sets up blocks of code in which errors that are thrown in one block are handled in another. Errors that are thrown inside the try block are caught in the catch block. JavaScript.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=try {
     tryStatements
} catch( exception ) {
     catchStatements
} finally {
     finallyStatements
}
}}
|Values={{JS Syntax Parameter
|Name=tryStatements
|Required=Required
|Description=Statements where an error can occur.
}}{{JS Syntax Parameter
|Name=exception
|Required=Required
|Description=Any variable name. The initial value of exception is the value of the thrown error.
}}{{JS Syntax Parameter
|Name=catchStatements
|Required=Optional
|Description=Statements to handle errors occurring in the associated tryStatements.
}}{{JS Syntax Parameter
|Name=finallyStatements
|Required=Optional
|Description=Statements that are unconditionally executed after all other error processing has occurred.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example causes a ReferenceError exception to be thrown and displays the name of the error and its message.
|Code=try {
     addalert("bad call");
 }
 catch(e) {
     document.write ("Error Message: " + e.message);
     document.write ("&lt;br /&gt;");
     document.write ("Error Code: ");
     document.write (e.number &amp; 0xFFFF)
     document.write ("&lt;br /&gt;");
     document.write ("Error Name: " + e.name);
 }
 
 // Output:
 Error Message: 'addalert' is undefined
 Error Code: 5009
 Error Name: ReferenceError
}}{{Single Example
|Language=JavaScript
|Description=The following example shows how to re-throw errors, as well as the execution of nested try...catch blocks. When the error is thrown from the nested try block, it passes to the nested catch block, which re-throws it. The nested finally block runs before the outer catch block handles the error, and at the end the outer finally block runs.
|Code=try {
     document.write("Outer try running...&lt;br/&gt;");
 
     try {
         document.write("Nested try running...&lt;br/&gt;");
         throw new Error(301, "an error");
     }
     catch (e) {
         document.write ("Nested catch caught " + e.message + "&lt;br/&gt;");
         throw e;
     }
     finally {
         document.write ("Nested finally is running...&lt;br/&gt;");
     }
 }
 catch (e) {
     document.write ("Outer catch caught " + e.message + "&lt;br/&gt;");
 }
 finally {
     document.write ("Outer finally running");
 }
 
 // Output:
 // Outer try running...
 // Nested try running...
 // Nested catch caught error from nested try
 // Nested finally is running...
 // Outer catch caught error from nested try
 // Outer finally running
}}
}}
{{Remarks_Section
|Remarks=The try...catch...finally statement provides a way to handle some or all of the errors that may occur in a given block of code, while still running code. If errors occur that are not handled, JavaScript provides the normal error message.

The try block contains code that may provoke an error, while the catch block contains the code that handles some or all errors. If an error occurs in the try block, program control is passed to the catch block. The value of exception is the value of the error that occurred in the try block. If no error occurs, the code in the catch block is never executed.

You can pass the error up to the next level by using the throw statement to re-throw the error.

After all the statements in the try block have been executed and error handling has been done in the catch block, the statements in the finally block are executed, whether or not an error was handled. The code in the finally block is guaranteed to run unless an unhandled error occurs (for example, a run-time error inside the '''catch''' block).
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/throw{{!}}throw Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4yahc5d8(v=vs.94).aspx
|HTML5Rocks_link=
}}