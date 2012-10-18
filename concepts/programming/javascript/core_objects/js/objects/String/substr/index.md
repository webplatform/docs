=== Summary ===
Returns a subset of a string starting at the given location through the given number of characters.

=== Syntax ===
<syntaxhighlight lang="javascript">
"string".substr(start [, length])
</syntaxhighlight>

=== Parameters ===
'''start''' 
:The location to start the subset of characters.
'''length''' 
:The number of characters to extract from the string.

=== Example ===
<syntaxhighlight lang="javascript">
var string = "The quick brown fox.";

print(string.substr(0, 3));     // "The"
print(string.substr(4));        // "quick brown fox."
print(string.substr(-3, 10));   // "ox."
</syntaxhighlight>