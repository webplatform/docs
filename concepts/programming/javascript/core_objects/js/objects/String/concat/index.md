=== Summary ===
Returns value of joined strings without altering original string.  

One of multiple ways to do this.  Other ways include the addition operator ( + ) and the assignment operator ( += ).

=== Syntax ===
<syntaxhighlight lang="javascript">
"string".concat
</syntaxhighlight>

=== Parameters ===
string1, string2, stringN, etc...

=== Example ===
<syntaxhighlight lang="javascript">
var firstName="Patrick ";
var lastName="Wilson";
var describeThem=" is great";

var actorDescript = firstName.concat(lastName,describeThem);
</syntaxhighlight>