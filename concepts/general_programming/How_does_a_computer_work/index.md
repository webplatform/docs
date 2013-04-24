{{Page_Title|General Programming Concepts}}
{{Flags
|High-level issues=Needs Topics, Needs Review
|Content=Incomplete
|Checked_Out=No
}}
{{Summary_Section|So, you think your computer is smart? It can do math faster than most people, even complex physics and acocunting algorithms. How does it do that?}}
{{Basic Page}}
==Computers are Stupid==
Computers are actually pretty stupid. They are very good at following directions, but we still have not built the computer that can truly think for itself. The computers that look like they think for themselves are still following the directions given them by the developer. Even when a computer seems to be misbehaving, it is still following the directions (poor as they may be) the developer gave it.
==Do computers really think in ones and zeros?==
At the very core, yes, most computers are dealing with a binary system. Colloquially, this tends to be translated as zero and one, but it can also be translated as off and on, open and closed, false and true, even 0 volts and 5 volts. While there have been computers that work in ternary, using zero, one, and two at the core, computers are predominantly binary and the rest of this article will assume a binary system. When you get down the most basic parts of the computer, you tend to be dealing with binary, one and zero.
===What is the difference between digital and analog?===
The definition of this difference is that digital media uses discrete values within a specific range and analog uses any value within that range. As an example, digital would be like saying, "Pick a number from one to ten, but it has to be an integer," and analog would be like saying, "Pick a number from one to ten." Where you have a specific number of digital choices (1, 2, 3,... 10), you have an infinite number of analog choices (1-3/5, 3.14159..., 2.71828..., 1.41421...). While analog offers more flexibility, it is also harder to reproduce correctly. When television was first broadcast, it was an analog broadcast; your television could pick up part of the signal and the rest was static. When television is broadcast in digital and your television receives the signal, it tends either to be perfectly clear or unavailable entirely.
===What is a transistor?===
Modern computers can quickly handle large amounts of discrete numbers because, at the very core of the computer, there are some very tiny, very basic components ready to handle discrete values. Computer processors are still measured by the number of transistors embedded in the integrated circuits. The transistor is the building block for nearly every computer in existence today. A very common use for a transistor today is as a switch, where the transistor simply represents either a one or a zero. The transistor does this by either connecting a circuit, allowing the signal through, or grounding the circuit, stopping the signal. Theoretically, the computer is providing 5 volts to the transistor and, when the transistor signals a one, the circuit is closed and the 5 volts go through the transistor to the other side; when the transistor signals a zero, the circuit is grounded (open) and 0 volts go through the transistor to the other side.
===How does the computer use ones and zeros?===
In the late 19th century, George Boole defined a system of logical algebra. Essentially, Boole made it possible to represent logic problems in terms of mathematics, defining algebraic ways to represent "and", "or", and "exclusive-or" (or "disjoint union"). With regard to his contributions, these mathematical functions are known as Boolean logic functions (or operations).

There are four simple Boolean logic operations: <code>NOT</code>, <code>OR</code>, <code>AND</code>, and <code>XOR</code>. Each of these operations has an associated "truth table", a table that defines when, based on the input given it, the operation will result in a true value (and, conversely, a false value). <code>NOT A</code> returns the opposite of A: if A is true, the result is false; if A is false, the result is true. <code>A AND B</code> returns true only if <code>A</code> is true _and_ <code>B</code> is true. <code>A OR B</code> returns true if at least <code>A</code> is true _or_ <code>B</code> is true. <code>A XOR B</code> returns true only if <code>A</code> is true _or_ <code>B</code> is true, but not if both are true.

The last paragraph described the results of these operations. However, would it be called a truth table if it didn't look like a table? Here is a truth table for the <code>NOT</code> operation. The <code>NOT</code> operation is known as a unary operation because it only takes one input (thus the un- prefix).
{| summary="Truth table for NOT operation" style="white-space: nowrap; width: 1%"
|+ <code>NOT</code> Truth Table
|-
! A &rarr;
! False
! True
|-
! 
| True
| False
|}
How do I read this truth table? Across the top, you have the value of <code>A</code>. Underneath each value of <code>A</code>, you have the corresponding result. If the value of <code>A</code> is <code>False</code>, the result is <code>True</code>; if the value of <code>A</code> is <code>True</code>, the result is <code>False</code>.

That should pretty understandable, but the computer deals in ones and zeros, right? Let's translate that same truth table into ones and zeros.
{| summary="Truth table for NOT operation" style="white-space: nowrap; width: 1%"
|+ <code>NOT</code> Truth Table
|-
! A &rarr;
! 0
! 1
|-
! 
| 1
| 0
|}
Pretty simple, yes? Let's look at the other truth tables. Notice that they take two inputs, <code>A</code> and <code>B</code>. The remaining operations are known as binary operations because they take two inputs (thus the bi- prefix). Notice that we now have a grid of results because we have two inputs and the axes are labeled across the top and down the left. Look at each value in the grid and see what value of <code>A</code> and what value of <code>B</code> produced that result. Does the truth table reflect the logic of the operation? If <code>A</code> is <code>1</code> <code>AND</code> <code>B</code> is <code>1</code>, is the result <code>1</code>?
{| summary="Truth table for AND operation" style="white-space: nowrap; width: 1%"
|+ <code>AND</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 0
| 0
|-
! 1
| 0
| 1
|}
{| summary="Truth table for OR operation" style="white-space: nowrap; width: 1%"
|+ <code>OR</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 0
| 1
|-
! 1
| 1
| 1
|}
{| summary="Truth table for XOR operation" style="white-space: nowrap; width: 1%"
|+ <code>XOR</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 0
| 1
|-
! 1
| 1
| 0
|}
So, those are the basic logic operations. Of course, Boole developed logic algebra, so we can't leave it at simple operations, can we? However, everything else can be represented as a combination of these simple operations. Just as multiplication can be derived from addition and exponents can be derived from multiplication, so more complex Boolean logic operations can be derived from simple logic operations. Here are some slightly more complex logic operations: <code>NAND</code>, <code>NOR</code>, and <code>XNOR</code>. All of these operations are the result of a simple operation passed through the <code>NOT</code> operation, i.e., inverted.
{| summary="Truth table for NAND operation" style="white-space: nowrap; width: 1%"
|+ <code>NAND</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 1
| 1
|-
! 1
| 1
| 0
|}
{| summary="Truth table for NOR operation" style="white-space: nowrap; width: 1%"
|+ <code>NOR</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 1
| 0
|-
! 1
| 0
| 0
|}
{| summary="Truth table for XNOR operation" style="white-space: nowrap; width: 1%"
|+ <code>XNOR</code> Truth Table
|-
! B &darr; A &rarr;
! 0
! 1
|-
! 0
| 1
| 0
|-
! 1
| 0
| 1
|}
Do you see how these truth tables are exactly the opposite of the respective truth tables above? We simply negated the results, turning <code>0</code> to <code>1</code> and <code>1</code> to <code>0</code>. Believe me, just as algebra can get pretty complex, so Boolean algebra can get pretty complex. We won't delve into more of the complexity here.
{{TODO|Logic operations &rarr; Logic gates &rarr; Made with transistors &rarr; Store information and perform mathematical operations}}
{{TODO|Processor has a clock &rarr; Square wave &rarr; Clock fires instructions so results are meaningful}}
{{TODO|Binary represented by octal and hexadecimal &rarr; nibbles and bytes &rarr; processor word size &rarr; registers}}