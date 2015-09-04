---
title: expressions
tags:
  - Tutorials
  - JavaScript
readiness: 'Almost Ready'
summary: 'This chapter describes JavaScript expressions and operators, including assignment, comparison, arithmetic, bitwise, logical, string, and special operators.'
uri: concepts/programming/javascript/expressions
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/expressions/js/objects/NaN
    - 'concepts/programming/javascript/expressions/js/guide/Working with objects'
    - js/operators/new

---
# expressions

## Summary

This chapter describes JavaScript expressions and operators, including assignment, comparison, arithmetic, bitwise, logical, string, and special operators.

## Expressions

An *expression* is any valid unit of code that resolves to a value.

Conceptually, there are two types of expressions: those that assign a value to a variable, and those that simply have a value. For example, the expression `x = 7` is an expression that assigns x the value seven. This expression itself evaluates to seven. Such expressions use *assignment operators*. On the other hand, the expression `3 + 4` simply evaluates to seven; it does not perform an assignment. The operators used in such expressions are referred to simply as *operators*.

JavaScript has the following types of expressions:

-   Arithmetic: evaluates to a number, for example 3.14159. (Generally uses [arithmetic operators](#Arithmetic_operators).)
-   String: evaluates to a character string, for example, "Fred" or "234". (Generally uses [string operators](#String_operators).)
-   Logical: evaluates to true or false. (Often involves [logical operators](#Logical_operators).)
-   Object: evaluates to an object. (See [special operators](#Special_operators) for various ones that evaluate to objects.)

## Operators

JavaScript has the following types of operators. This section describes the operators and contains information about operator precedence.

-   [Assignment operators](#Assignment_operators)
-   [Comparison operators](#Comparison_operators)
-   [Arithmetic operators](#Arithmetic_operators)
-   [Bitwise operators](#Bitwise_operators)
-   [Logical operators](#Logical_operators)
-   [String operators](#String_operators)
-   [Special operators](#Special_operators)

JavaScript has both *binary* and *unary* operators, and one special ternary operator, the conditional operator. A binary operator requires two operands, one before the operator and one after the operator:

    <em>operand1</em> <em>operator</em> <em>operand2</em>

For example, `3+4` or `x*y`.

A unary operator requires a single operand, either before or after the operator:

    <em>operator</em> <em>operand</em>

or

    <em>operand</em> <em>operator</em>

For example, `x++` or `++x`.

### Assignment operators

An assignment operator assigns a value to its left operand based on the value of its right operand. The basic assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = y assigns the value of y to x.

The other assignment operators are shorthand for standard operations, as shown in the following table.

<table class="standard-table">
<caption style="text-align: left;">
Table 3.1 Assignment operators

</caption>
\<thead\>

<tr>
<th scope="col" width="50%">
Shorthand operator

</th>
<th scope="col" width="50%">
Meaning

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`x += y`

</td>
<td>
`x = x + y`

</td>
</tr>
<tr>
<td>
`x -= y`

</td>
<td>
`x = x - y`

</td>
</tr>
<tr>
<td>
`x *= y`

</td>
<td>
`x = x * y`

</td>
</tr>
<tr>
<td>
`x /= y`

</td>
<td>
`x = x / y`

</td>
</tr>
<tr>
<td>
`x %= y`

</td>
<td>
`x = x % y`

</td>
</tr>
<tr>
<td>
`x <<= y`

</td>
<td>
`x = x << y`

</td>
</tr>
<tr>
<td>
`x >>= y`

</td>
<td>
`x = x >> y`

</td>
</tr>
<tr>
<td>
`x >>>= y`

</td>
<td>
`x = x >>> y`

</td>
</tr>
<tr>
<td>
`x &= y`

</td>
<td>
`x = x & y`

</td>
</tr>
<tr>
<td>
`x ^= y`

</td>
<td>
`x = x ^ y`

</td>
</tr>
<tr>
<td>
`x |= y`

</td>
<td>
`x = x | y`

</td>
</tr>
\</tbody\>

</table>
### Comparison operators

<span class="comment">This seems to me kind of poorly explained, mostly the difference betwen "==" and "==="...</span> A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert the operands to an appropriate type for the comparison. (The sole exceptions to this rule are `===` and `!==`, which perform "strict" equality and inequality and which do not attempt to convert the operands to compatible types before checking equality.) This generally results in a numerical comparison being performed. The following table describes the comparison operators, assuming the following code:

``` {.brush: .js}
var var1 = 3, var2 = 4;
```

<table class="standard-table">
<caption style="text-align: left;">
Table 3.2 Comparison operators

</caption>
\<thead\>

<tr>
<th scope="col">
Operator

</th>
<th scope="col">
Description

</th>
<th scope="col">
Examples returning true

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
Equal (`==`)

</td>
<td>
Returns true if the operands are equal.

</td>
<td>
`3 == var1`

`"3" == var1`

`3 == '3'`

</td>
</tr>
<tr>
<td>
Not equal (`!=`)

</td>
<td>
Returns true if the operands are not equal.

</td>
<td>
`var1 != 4         var2 != "3"`

</td>
</tr>
<tr>
<td>
Strict equal (`===`)

</td>
<td>
Returns true if the operands are equal and of the same type.

</td>
<td>
`3 === var1`

</td>
</tr>
<tr>
<td>
Strict not equal (`!==`)

</td>
<td>
Returns true if the operands are not equal and/or not of the same type.

</td>
<td>
`var1 !== "3"         3 !== '3'`

</td>
</tr>
<tr>
<td>
Greater than (`>`)

</td>
<td>
Returns true if the left operand is greater than the right operand.

</td>
<td>
`var2 > var1         "12" > 2`

</td>
</tr>
<tr>
<td>
Greater than or equal (`>=`)

</td>
<td>
Returns true if the left operand is greater than or equal to the right operand.

</td>
<td>
`var2 >= var1         var1 >= 3`

</td>
</tr>
<tr>
<td>
Less than (`<`)

</td>
<td>
Returns true if the left operand is less than the right operand.

</td>
<td>
`var1 < var2         "12" < "2"`

</td>
</tr>
<tr>
<td>
Less than or equal (`<=`)

</td>
<td>
Returns true if the left operand is less than or equal to the right operand.

</td>
<td>
`var1 <= var2         var2 <= 5`

</td>
</tr>
\</tbody\>

</table>
### Arithmetic operators

Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (\*), and division (/). These operators work as they do in most other programming languages when used with floating point numbers (in particular, note that division by zero produces `NaN`). For example:

``` {.brush: .js}
console.log(1 / 2); /* prints 0.5 */
console.log(1 / 2 == 1.0 / 2.0); /* also this is true */
```

In addition, JavaScript provides the arithmetic operators listed in the following table.

<table class="fullwidth-table">
<caption style="text-align: left;">
Table 3.3 Arithmetic operators

</caption>
\<thead\>

<tr>
<th scope="col">
Operator

</th>
<th scope="col">
Description

</th>
<th scope="col">
Example

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`%`
 (Modulus)

</td>
<td>
Binary operator. Returns the integer remainder of dividing the two operands.

</td>
<td>
12 % 5 returns 2.

</td>
</tr>
<tr>
<td>
`++`
 (Increment)

</td>
<td>
Unary operator. Adds one to its operand. If used as a prefix operator (`++x`), returns the value of its operand after adding one; if used as a postfix operator (`x++`), returns the value of its operand before adding one.

</td>
<td>
If `x` is 3, then `++x` sets `x` to 4 and returns 4, whereas `x++` returns 3 and, only then, sets `x` to 4.

</td>
</tr>
<tr>
<td>
`--`
 (Decrement)

</td>
<td>
Unary operator. Subtracts one from its operand. The return value is analogous to that for the increment operator.

</td>
<td>
If `x` is 3, then `--x` sets `x` to 2 and returns 2, whereas `x--` returns 3 and, only then, sets `x` to 2.

</td>
</tr>
<tr>
<td>
`-`
 (Unary negation)

</td>
<td>
Unary operator. Returns the negation of its operand.

</td>
<td>
If `x` is 3, then `-x` returns -3.

</td>
</tr>
\</tbody\>

</table>
### Bitwise operators

Bitwise operators treat their operands as a set of 32 bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers. For example, the decimal number nine has a binary representation of 1001. Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values.

The following table summarizes JavaScript's bitwise operators.

<table class="standard-table">
<caption style="text-align: left;">
Table 3.4 Bitwise operators

</caption>
\<thead\>

<tr>
<th scope="col">
Operator

</th>
<th scope="col">
Usage

</th>
<th scope="col">
Description

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
Bitwise AND

</td>
<td>
`a & b`

</td>
<td>
Returns a one in each bit position for which the corresponding bits of both operands are ones.

</td>
</tr>
<tr>
<td>
Bitwise OR

</td>
<td>
`a | b`

</td>
<td>
Returns a one in each bit position for which the corresponding bits of either or both operands are ones.

</td>
</tr>
<tr>
<td>
Bitwise XOR

</td>
<td>
`a ^ b`

</td>
<td>
Returns a one in each bit position for which the corresponding bits of either but not both operands are ones.

</td>
</tr>
<tr>
<td>
Bitwise NOT

</td>
<td>
`~ a`

</td>
<td>
Inverts the bits of its operand.

</td>
</tr>
<tr>
<td>
Left shift

</td>
<td>
`a << b`

</td>
<td>
Shifts `a` in binary representation `b` bits to the left, shifting in zeros from the right.

</td>
</tr>
<tr>
<td>
Sign-propagating right shift

</td>
<td>
`a >> b`

</td>
<td>
Shifts `a` in binary representation `b` bits to the right, discarding bits shifted off.

</td>
</tr>
<tr>
<td>
Zero-fill right shift

</td>
<td>
`a >>> b`

</td>
<td>
Shifts `a` in binary representation `b` bits to the right, discarding bits shifted off, and shifting in zeros from the left.

</td>
</tr>
\</tbody\>

</table>
#### Bitwise logical operators

Conceptually, the bitwise logical operators work as follows:

-   The operands are converted to thirty-two-bit integers and expressed by a series of bits (zeros and ones).
-   Each bit in the first operand is paired with the corresponding bit in the second operand: first bit to first bit, second bit to second bit, and so on.
-   The operator is applied to each pair of bits, and the result is constructed bitwise.

For example, the binary representation of nine is 1001, and the binary representation of fifteen is 1111. So, when the bitwise operators are applied to these values, the results are as follows:

<table class="standard-table">
<caption style="text-align: left;">
Table 3.5 Bitwise operator examples

</caption>
\<thead\>

<tr>
<th scope="col">
Expression

</th>
<th scope="col">
Result

</th>
<th scope="col">
Binary Description

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`15 & 9`

</td>
<td>
`9`

</td>
<td>
`1111 & 1001 = 1001`

</td>
</tr>
<tr>
<td>
`15 | 9`

</td>
<td>
`15`

</td>
<td>
`1111 | 1001 = 1111`

</td>
</tr>
<tr>
<td>
`15 ^ 9`

</td>
<td>
`6`

</td>
<td>
`1111 ^ 1001 = 0110`

</td>
</tr>
<tr>
<td>
`~15`

</td>
<td>
`0`

</td>
<td>
`~1111 = 0000`

</td>
</tr>
<tr>
<td>
`~9`

</td>
<td>
`6`

</td>
<td>
`~1001 = 0110`

</td>
</tr>
\</tbody\>

</table>
�

#### Bitwise shift operators

The bitwise shift operators take two operands: the first is a quantity to be shifted, and the second specifies the number of bit positions by which the first operand is to be shifted. The direction of the shift operation is controlled by the operator used.

Shift operators convert their operands to thirty-two-bit integers and return a result of the same type as the left operand.

The shift operators are listed in the following table.

<table class="fullwidth-table">
<caption style="text-align: left;">
Table 3.6 Bitwise shift operators

</caption>
\<thead\>

<tr>
<th scope="col">
Operator

</th>
<th scope="col">
Description

</th>
<th scope="col">
Example

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`<<`
 (Left shift)

</td>
<td>
This operator shifts the first operand the specified number of bits to the left. Excess bits shifted off to the left are discarded. Zero bits are shifted in from the right.

</td>
<td>
`9<<2` yields 36, because 1001 shifted 2 bits to the left becomes 100100, which is 36.

</td>
</tr>
<tr>
<td>
`>>`
 (Sign-propagating right shift)

</td>
<td>
This operator shifts the first operand the specified number of bits to the right. Excess bits shifted off to the right are discarded. Copies of the leftmost bit are shifted in from the left.

</td>
<td>
`9>>2` yields 2, because 1001 shifted 2 bits to the right becomes 10, which is 2. Likewise, `-9>>2` yields -3, because the sign is preserved.

</td>
</tr>
<tr>
<td>
`>>>`
 (Zero-fill right shift)

</td>
<td>
This operator shifts the first operand the specified number of bits to the right. Excess bits shifted off to the right are discarded. Zero bits are shifted in from the left.

</td>
<td>
`19>>>2` yields 4, because 10011 shifted 2 bits to the right becomes 100, which is 4. For non-negative numbers, zero-fill right shift and sign-propagating right shift yield the same result.

</td>
</tr>
\</tbody\>

</table>
### Logical operators

Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table.

<table class="fullwidth-table">
<caption style="text-align: left;">
Table 3.6 Logical operators

</caption>
\<thead\>

<tr>
<th scope="col">
Operator

</th>
<th scope="col">
Usage

</th>
<th scope="col">
Description

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
`&&`

</td>
<td>
`expr1 && expr2`

</td>
<td>
(Logical AND) Returns `expr1` if it can be converted to false; otherwise, returns `expr2`. Thus, when used with Boolean values, `&&` returns true if both operands are true; otherwise, returns false.

</td>
</tr>
<tr>
<td>
`||`

</td>
<td>
`expr1 || expr2`

</td>
<td>
(Logical OR) Returns `expr1` if it can be converted to true; otherwise, returns `expr2`. Thus, when used with Boolean values, `||` returns true if either operand is true; if both are false, returns false.

</td>
</tr>
<tr>
<td>
`!`

</td>
<td>
`!expr`

</td>
<td>
(Logical NOT) Returns false if its single operand can be converted to true; otherwise, returns true.

</td>
</tr>
\</tbody\>

</table>
Examples of expressions that can be converted to false are those that evaluate to null, 0, the empty string (""), or undefined.

The following code shows examples of the && (logical AND) operator.

``` {.brush: .js}
var a1 =  true && true;     // t && t returns true
var a2 =  true && false;    // t && f returns false
var a3 = false && true;     // f && t returns false
var a4 = false && (3 == 4); // f && f returns false
var a5 = "Cat" && "Dog";    // t && t returns Dog
var a6 = false && "Cat";    // f && t returns false
var a7 = "Cat" && false;    // t && f returns false
```

The following code shows examples of the || (logical OR) operator.

``` {.brush: .js}
var o1 =  true
|t returns true
var o2=false
|t returns true
var o3=true
|f returns true
var o4=false
|(3== 4); // f
|f returns false
var o5="Cat"
|t returns Cat
var o6=false
|t returns Cat
var o7="Cat"
|f returns Cat
```

The following code shows examples of the ! (logical NOT) operator\_

``` {.brush: .js}
var n1 = !true;  // !t returns false
var n2 = !false; // !f returns true
var n3 = !"Cat"; // !t returns false
```

#### Short-circuit evaluation

As logical expressions are evaluated left to right, they are tested for possible "short-circuit" evaluation using the following rules:

-   `false` && *anything* is short-circuit evaluated to false.
-   `true` || *anything* is short-circuit evaluated to true.

The rules of logic guarantee that these evaluations are always correct. Note that the *anything* part of the above expressions is not evaluated, so any side effects of doing so do not take effect.

### String operators

In addition to the comparison operators, which can be used on string values, the concatenation operator (+) concatenates two string values together, returning another string that is the union of the two operand strings. For example, `"my " + "string"` returns the string `"my string"`.

The shorthand assignment operator += can also be used to concatenate strings. For example, if the variable `mystring` has the value "alpha", then the expression `mystring += "bet"` evaluates to "alphabet" and assigns this value to `mystring`.

### Special operators

JavaScript provides the following special operators:

-   [Conditional operator](#Conditional_operator)
-   [Comma operator](#Comma_operator)
-   `delete`
-   `in`
-   `instanceof`
-   `new`
-   `this`
-   `typeof`
-   `void`

#### Conditional operator

The conditional operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition. The syntax is:

    <em>condition</em> ? <em>val1</em> : <em>val2</em>

If `condition` is true, the operator has the value of `val1`. Otherwise it has the value of `val2`. You can use the conditional operator anywhere you would use a standard operator.

For example,

``` {.brush: .js}
var status = (age >= 18) ? "adult" : "minor";
```

This statement assigns the value "adult" to the variable `status` if `age` is eighteen or more. Otherwise, it assigns the value "minor" to `status`.

#### Comma operator

The comma operator (`,`) simply evaluates both of its operands and returns the value of the second operand. This operator is primarily used inside a `for` loop, to allow multiple variables to be updated each time through the loop.

For example, if `a` is a 2-dimensional array with 10 elements on a side, the following code uses the comma operator to increment two variables at once. The code prints the values of the diagonal elements in the array:

``` {.brush: .js}
for (var i = 0, j = 9; i <= 9; i++, j--)
  document.writeln("a[" + i + "][" + j + "]= " + a[i][j]);
```

#### delete

The `delete` operator deletes an object, an object's property, or an element at a specified index in an array. The syntax is:

``` {.brush: .js}
delete objectName;
delete objectName.property;
delete objectName[index];
delete property; // legal only within a with statement
```

where `objectName` is the name of an object, `property` is an existing property, and `index` is an integer representing the location of an element in an array.

The fourth form is legal only within a `with` statement, to delete a property from an object.

You can use the `delete` operator to delete variables declared implicitly but not those declared with the `var` statement.

If the `delete` operator succeeds, it sets the property or element to `undefined`. The `delete` operator returns true if the operation is possible; it returns false if the operation is not possible.

``` {.brush: .js}
x = 42;
var y = 43;
myobj = new Number();
myobj.h = 4;    // create property h
delete x;       // returns true (can delete if declared implicitly)
delete y;       // returns false (cannot delete if declared with var)
delete Math.PI; // returns false (cannot delete predefined properties)
delete myobj.h; // returns true (can delete user-defined properties)
delete myobj;   // returns true (can delete if declared implicitly)
```

##### Deleting array elements

When you delete an array element, the array length is not affected. For example, if you delete `a[3]`, `a[4]` is still `a[4]` and `a[3]` is undefined.

When the `delete` operator removes an array element, that element is no longer in the array. In the following example, `trees[3]` is removed with `delete`. However, `trees[3]` is still addressable and returns `undefined`.

``` {.brush: .js}
var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
delete trees[3];
if (3 in trees) {
  // this does not get executed
}
```

If you want an array element to exist but have an undefined value, use the `undefined` keyword instead of the `delete` operator. In the following example, `trees[3]` is assigned the value `undefined`, but the array element still exists:

``` {.brush: .js}
var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
trees[3] = undefined;
if (3 in trees) {
  // this gets executed
}
```

#### in

The `in` operator returns true if the specified property is in the specified object. The syntax is:

``` {.brush: .js}
propNameOrNumber in objectName
```

where `propNameOrNumber` is a string or numeric expression representing a property name or array index, and `objectName` is the name of an object.

The following examples show some uses of the `in` operator.

``` {.brush: .js}
// Arrays
var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
0 in trees;        // returns true
3 in trees;        // returns true
6 in trees;        // returns false
"bay" in trees;    // returns false (you must specify the index number,
                   // not the value at that index)
"length" in trees; // returns true (length is an Array property)

// Predefined objects
"PI" in Math;          // returns true
var myString = new String("coral");
"length" in myString;  // returns true

// Custom objects
var mycar = {make: "Honda", model: "Accord", year: 1998};
"make" in mycar;  // returns true
"model" in mycar; // returns true
```

#### instanceof

The `instanceof` operator returns true if the specified object is of the specified object type. The syntax is:

``` {.brush: .js}
objectName instanceof objectType
```

where `objectName` is the name of the object to compare to `objectType`, and `objectType` is an object type, such as `Date` or `Array`.

Use `instanceof` when you need to confirm the type of an object at runtime. For example, when catching exceptions, you can branch to different exception-handling code depending on the type of exception thrown.

For example, the following code uses `instanceof` to determine whether `theDay` is a `Date` object. Because `theDay` is a `Date` object, the statements in the `if` statement execute.

``` {.brush: .js}
var theDay = new Date(1995, 12, 17);
if (theDay instanceof Date) {
  // statements to execute
}
```

#### new

You can use the `new` operator to create an instance of a user-defined object type or of one of the predefined object types `Array`, `Boolean`, `Date`, `Function`, `Image`, `Number`, `Object`, `Option`, `RegExp`, or `String`. On the server, you can also use it with `DbPool`, `Lock`, `File`, or `SendMail`. Use `new` as follows:

``` {.brush: .js}
var objectName = new objectType([param1, param2, ..., paramN]);
```

You can also create objects using object initializers, as described in [using object initializers](/w/index.php?title=concepts/programming/javascript/expressions/js/guide/Working_with_objects&action=edit&redlink=1).

See the `new` operator\</a\> page in the JavaScript Reference for more information.

#### this

Use the `this` keyword to refer to the current object. In general, `this` refers to the calling object in a method. Use `this` as follows:

``` {.brush: .js}
this["propertyName"]
```

``` {.brush: .js}
this.propertyName
```

**Example 1.**
 Suppose a function called `validate` validates an object's `value` property, given the object and the high and low values:

``` {.brush: .js}
function validate(obj, lowval, hival){
  if ((obj.value < lowval) {{!}}{{!}} (obj.value > hival))
    alert("Invalid Value!");
}
```

You could call `validate` in each form element's `onChange` event handler, using `this` to pass it the form element, as in the following example:

``` {.brush: .html}
<B>Enter a number between 18 and 99:</B>
<INPUT TYPE="text" NAME="age" SIZE=3
   onChange="validate(this, 18, 99);">
```

**Example 2.**
 When combined with the `form` property, `this` can refer to the current object's parent form. In the following example, the form `myForm` contains a `Text` object and a button. When the user clicks the button, the value of the `Text` object is set to the form's name. The button's `onClick` event handler uses `this.form` to refer to the parent form, `myForm`.

``` {.brush: .html}
<FORM NAME="myForm">
Form name:<INPUT TYPE="text" NAME="text1" VALUE="Beluga">
<P>
<INPUT NAME="button1" TYPE="button" VALUE="Show Form Name"
   onClick="this.form.text1.value = this.form.name;">
</FORM>
```

#### typeof

The `typeof` operator is used in either of the following ways:

1.  ``` {.brush: .js}
    typeof operand
    ```

2.  ``` {.brush: .js}
    typeof (operand)
    ```

The `typeof` operator returns a string indicating the type of the unevaluated operand. `operand` is the string, variable, keyword, or object for which the type is to be returned. The parentheses are optional.

Suppose you define the following variables:

``` {.brush: .js}
var myFun = new Function("5 + 2");
var shape = "round";
var size = 1;
var today = new Date();
```

The `typeof` operator returns the following results for these variables:

``` {.brush: .js}
typeof myFun;     // returns "function"
typeof shape;     // returns "string"
typeof size;      // returns "number"
typeof today;     // returns "object"
typeof dontExist; // returns "undefined"
```

For the keywords `true` and `null`, the `typeof` operator returns the following results:

``` {.brush: .js}
typeof true; // returns "boolean"
typeof null; // returns "object"
```

For a number or string, the `typeof` operator returns the following results:

``` {.brush: .js}
typeof 62;            // returns "number"
typeof 'Hello world'; // returns "string"
```

For property values, the `typeof` operator returns the type of value the property contains:

``` {.brush: .js}
typeof document.lastModified; // returns "string"
typeof window.length;         // returns "number"
typeof Math.LN2;              // returns "number"
```

For methods and functions, the `typeof` operator returns results as follows:

``` {.brush: .js}
typeof blur;        // returns "function"
typeof eval;        // returns "function"
typeof parseInt;    // returns "function"
typeof shape.split; // returns "function"
```

For predefined objects, the `typeof` operator returns results as follows:

``` {.brush: .js}
typeof Date;     // returns "function"
typeof Function; // returns "function"
typeof Math;     // returns "object"
typeof Option;   // returns "function"
typeof String;   // returns "function"
```

#### void

The `void` operator is used in either of the following ways:

1.  ``` {.brush: .js}
    void (expression)
    ```

2.  ``` {.brush: .js}
    void expression
    ```

The `void` operator specifies an expression to be evaluated without returning a value. `expression` is a JavaScript expression to evaluate. The parentheses surrounding the expression are optional, but it is good style to use them.

You can use the `void` operator to specify an expression as a hypertext link. The expression is evaluated but is not loaded in place of the current document.

The following code creates a hypertext link that does nothing when the user clicks it. When the user clicks the link, `void(0)` evaluates to undefined, which has no effect in JavaScript.

``` {.brush: .html}
<A HREF="javascript:void(0)">Click here to do nothing</A>
```

The following code creates a hypertext link that submits a form when the user clicks it.

``` {.brush: .html}
<A HREF="javascript:void(document.form.submit())">
Click here to submit</A>
```

### Operator precedence

The *precedence* of operators determines the order they are applied when evaluating an expression. You can override operator precedence by using parentheses.

The following table describes the precedence of operators, from highest to lowest.

<small>*In accordance with \<a href="/Talk:en-US/docs/JavaScript/Guide/Obsolete\_Pages/Operators\#Precedence\_Table" title="Talk:en-US/docs/JavaScript/Guide/Operators\#Precedence\_Table"\>relevant discussion\</a\>, this table was reversed to list operators in **decreasing** order of priority.*</small>

<table class="standard-table">
<caption style="text-align: left;">
Table 3.7 Operator precedence

</caption>
\<thead\>

<tr>
<th scope="col">
Operator type

</th>
<th scope="col">
Individual operators

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
member

</td>
<td>
`. []`

</td>
</tr>
<tr>
<td>
call / create instance

</td>
<td>
`() new`

</td>
</tr>
<tr>
<td>
negation/increment

</td>
<td>
`! ~ - + ++ -- typeof void delete`

</td>
</tr>
<tr>
<td>
multiply/divide

</td>
<td>
`* / %`

</td>
</tr>
<tr>
<td>
addition/subtraction

</td>
<td>
`+ -`

</td>
</tr>
<tr>
<td>
bitwise shift

</td>
<td>
`<< >> >>>`

</td>
</tr>
<tr>
<td>
relational

</td>
<td>
`< <= > >= in instanceof`

</td>
</tr>
<tr>
<td>
equality

</td>
<td>
`== != === !==`

</td>
</tr>
<tr>
<td>
bitwise-and

</td>
<td>
`&`

</td>
</tr>
<tr>
<td>
bitwise-xor

</td>
<td>
`^`

</td>
</tr>
<tr>
<td>
bitwise-or

</td>
<td>
`|`

</td>
</tr>
<tr>
<td>
logical-and

</td>
<td>
`&&`

</td>
</tr>
<tr>
<td>
logical-or

</td>
<td>
`||`

</td>
</tr>
<tr>
<td>
conditional

</td>
<td>
`?:`

</td>
</tr>
<tr>
<td>
assignment

</td>
<td>
`= += -= *= /= %= <<= >>= >>>= &= ^= |=`

</td>
</tr>
<tr>
<td>
comma

</td>
<td>
`,`

</td>
</tr>
\</tbody\>

</table>
A more detailed version of this table, complete with links to additional details about each operator, may be found in \<a href="/en-US/docs/JavaScript/Reference/Operators/Operator\_Precedence\#Table" title="en-US/docs/JavaScript/Reference/Operators/Operator\_Precedence\#Table"\>JavaScript Reference\</a\>.

## See also

### External resources

[Section on Expressions and Operators in the EcmaScript 5.1 spec](http://ecma-international.org/ecma-262/5.1/#sec-11)

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Expressions_and_Operators)

