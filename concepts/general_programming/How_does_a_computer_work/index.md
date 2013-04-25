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
The definition of this difference is that digital media uses discrete values within a specific range and analog media uses any value within that range. As an example, digital would be like saying, "Pick a number from one to ten, but it has to be an integer," and analog would be like saying, "Pick a number from one to ten." Where you have a specific number of digital choices (1, 2, 3,... 10), you have an infinite number of analog choices (1-3/5, 3.14159..., 2.71828..., 1.41421...). While analog offers more flexibility, it is also harder to reproduce correctly. When television was first broadcast, it was an analog broadcast; your television could pick up part of the signal and the rest was static. When television is broadcast in digital and your television receives the signal, it tends either to be perfectly clear or unavailable entirely.
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

That should be pretty understandable, but the computer deals in ones and zeros, right? Let's translate that same truth table into ones and zeros.
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
==How does my computer use logic operations?==
Computers use transistors to store information and perform various operations. The logic operations above are implemented physically with transistors that make up logic "gates", so you can find logic gates for all of the logic operations listed above, including the inverted operations. Processors use logic gates to perform many tasks, including mathematics and memory access. The internal workings of a process are incredibly complex and the result of decades of innovation.

Also internal to a processor is a clock. While you and I can look at a logic chart and come up with the result, the modern processor is analyzing the results of these operations billions of times each second. In order for the results to make sense, the processor uses the clock to time the operations. Without using this device, the computer might not match up the result with the right operation.

Compare it to this situation. You work in one office and your supervisor works across the street in another office. Two messengers are always walking back and forth between you and your supervisor, picking up what is in your outbox and taking it to your supervisor. The messengers take exactly five minutes to travel between the two desks, regardless of direction, and time each other so one is picking up what is in your outbox when the other is delivering the previous batch to your supervisor. Due to the impeccable timing and performance of the messengers, your supervisor knows (within a five minute window) when you did the work. The computer uses a similar system in conjunction with the clock to time its operations with the results.
==Do programmers really think in ones and zeros?==
Perhaps a few programmers think in ones and zeros, but most programmers do not. Binary is a reasonably efficient number system (after ternary, base 3, and quaternary, base 4), but most people find it cumbersome. Today, most people use a decimal number system, but decimal is not very compatible with binary. As a compromise, programmers have worked with octal (base 8) in the past, but hexadecimal (base 16) is more common today.
===How do you write in octal and hexadecimal?===
Ready for some math? We are going to look at exponents and bases for a moment. Why are octal (base 8) and hexadecimal (base 16) reasonable compromises for working with binary compared to decimal (base 10)? Octal works because 8 is equal to 2<sup>3</sup>, so each octal digit represents three (and exactly three) binary digits. Hexadecimal works because 16 is equal to 2<sup>4</sup>, so each hexadecimal digit represents four (and exactly four) binary digits.

Decimal, base 10, means that there are ten digits involved in writing numbers in that system. We start with zero and go up to nine. Just as we start at zero and count up, so does the exponent on the base start at zero and count up. Though we may not tend to think about it this way, these first ten numbers (0 through 9) are multiplied by 10<sup>0</sup>. Why do we not tend to think about it this way? That is probably because 10<sup>0</sup> is 1 and any number multiplied by 1 is equal to itself (the identity property of multiplication). When we exhaust our ten digits, we add another in front and that digit is multiplied by the base to the power of the next exponent. In this case, that is 10<sup>1</sup>, or simply 10. So now we have 1 &times; 10<sup>1</sup> + 0 &times; 10<sup>0</sup>. We continue on up, getting to 99 (9 &times; 10<sup>1</sup> + 9 &times; 10<sup>0</sup>) and continuing to 100 (1 &times; 10<sup>2</sup> + 0 &times; 10<sup>1</sup> + 0 &times; 10<sup>0</sup>). Do you see how this works?

Now we extend this to octal. Just as decimal, base 10, has ten digits, so octal, base 8, has eight digits: 0 through 7. (You can clarify that you are writing in octal by writing the base as a subscript after the number, as in 10<sub>8</sub>.) We start with 0 and go to 7 and we have run out of digits. Just as we did with decimal when we ran out of digits, we add another number in front. So 10<sub>8</sub> is 1 &times; 8<sup>1</sup> + 0 &times; 8<sup>0</sup>. When we get to 63<sub>10</sub>, we have 77<sub>8</sub> (7 &times; 8<sup>1</sup> + 7 &times; 8<sup>0</sup>). As we continue, 64<sub>10</sub> is represented as 100<sub>8</sub> (1 &times; 8<sup>2</sup> + 0 &times; 8<sup>1</sup> + 0 &times; 8<sup>0</sup>).

Hexadecimal works much the same way, but we need to come up with more digits. Our decimal system only has ten digits, but a hexadecimal system, base 16, needs sixteen digits. As a result, we use the first six letters of the English alphabet to supplement, meaning that hexadecimal digits start at 0 and go to F. (Technically, case doesn't matter, so bd and BD are the same number. This article will use uppercase.) So you get to F<sub>16</sub> and the next number, 16<sub>10</sub>, is represented as 10<sub>16</sub> (1 &times; 16<sup>1</sup> + 0 &times; 16<sup>0</sup>). The next place is introduced when you get to 256<sub>10</sub>, which is written as 100<sub>16</sub> (1 &times; 16<sup>2</sup> + 0 &times; 16<sup>1</sup> + 0 &times; 16<sup>0</sup>).

Do you remember how I said that octal and hexadecimal are used because they have these nice ratios to binary digits (one octal digit to three binary digits, one hexadecimal digit to four binary digits)? We can look at a couple of examples. Take a look at this table.
{| style="white-space: nowrap; width: 1%" summary="Comparison of binary to octal and hexadecimal"
|+ Comparing binary to octal and hexadecimal
! Binary
! Octal
! Hexadecimal
|-
| 0000
| 00
| 0
|-
| 0001
| 01
| 1
|-
| 0010
| 02
| 2
|-
| 0011
| 03
| 3
|-
| 0100
| 04
| 4
|-
| 0101
| 05
| 5
|-
| 0110
| 06
| 6
|-
| 0111
| 07
| 7
|-
| 1000
| 10
| 8
|-
| 1001
| 11
| 9
|-
| 1010
| 12
| A
|-
| 1011
| 13
| B
|-
| 1100
| 14
| C
|-
| 1101
| 15
| D
|-
| 1110
| 16
| E
|-
| 1111
| 17
| F
|}
If you compare the binary and the octal, you will notice that the right-most octal digit cycles twice from 0 to 7 and each matches perfectly with the same three right-most digits in the binary column. Because of the 1:3 ratio between octal and binary and the 1:4 ratio between hexadecimal and binary, you can use a lookup table like this to switch between the three. If I write BD<sub>16</sub> (189<sub>10</sub>), we can use the table to translate that to 1011 1101<sub>2</sub>, move the spaces around (10 111 101<sub>2</sub>), and translate that to 275<sub>8</sub>. Do you see how that works? Try this exercise with some other numbers.
===How does understanding hexadecimal help me?===
{{TODO|nibbles and bytes &rarr; color codes and other uses}}