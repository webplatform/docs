---
title: How does a computer work
tags:
  - Basic
  - Pages
readiness: 'Ready to Use'
summary: 'So, you think your computer is smart? It can do math faster than most people, even complex physics and accounting algorithms. How does it do that?'
uri: 'concepts/general programming/How does a computer work'

---
# How does a computer work?

## Summary

So, you think your computer is smart? It can do math faster than most people, even complex physics and accounting algorithms. How does it do that?

## Computers are Stupid

Computers are actually pretty stupid. They are very good at following directions, but we still have not built the computer that can truly think for itself. The computers that look like they think for themselves are still following the directions given them by the developer. Even when a computer seems to be misbehaving, it is still following the directions (poor as they may be) the developer gave it.

## Do computers really think in ones and zeros?

At the very core, yes, most computers are dealing with a binary system. Colloquially, this tends to be translated as zero and one, but it can also be translated as off and on, open and closed, false and true, even 0 volts and 5 volts. While there have been computers that work in ternary, using zero, one, and two at the core, computers are predominantly binary and the rest of this article will assume a binary system. When you get down the most basic parts of the computer, you tend to be dealing with binary, one and zero.

### What is the difference between digital and analog?

The definition of this difference is that digital media uses discrete values within a specific range and analog media uses any value within that range. As an example, digital would be like saying, "Pick a number from one to ten, but it has to be an integer," and analog would be like saying, "Pick a number from one to ten." Where you have a specific number of digital choices (1, 2, 3,... 10), you have an infinite number of analog choices (1-3/5, 3.14159..., 2.71828..., 1.41421...). While analog offers more flexibility, it is also harder to reproduce correctly. When television was first broadcast, it was an analog broadcast; your television could pick up part of the signal and the rest was static. When television is broadcast in digital and your television receives the signal, it tends either to be perfectly clear or unavailable entirely.

### What is a transistor?

Modern computers can quickly handle large amounts of discrete numbers because, at the very core of the computer, there are some very tiny, very basic components ready to handle discrete values. Computer processors are still measured by the number of transistors embedded in the integrated circuits. The transistor is the building block for nearly every computer in existence today. A very common use for a transistor today is as a switch, where the transistor simply represents either a one or a zero. The transistor does this by either connecting a circuit, allowing the signal through, or grounding the circuit, stopping the signal. Theoretically, the computer is providing 5 volts to the transistor and, when the transistor signals a one, the circuit is closed and the 5 volts go through the transistor to the other side; when the transistor signals a zero, the circuit is grounded (open) and 0 volts go through the transistor to the other side.

### How does the computer use ones and zeros?

In the late 19th century, George Boole defined a system of logical algebra. Essentially, Boole made it possible to represent logic problems in terms of mathematics, defining algebraic ways to represent "and", "or", and "exclusive-or" (or "disjoint union"). With regard to his contributions, these mathematical functions are known as Boolean logic functions (or operations).

There are four simple Boolean logic operations: `NOT`, `OR`, `AND`, and `XOR`. Each of these operations has an associated "truth table", a table that defines when, based on the input given it, the operation will result in a true value (and, conversely, a false value). `NOT A` returns the opposite of A: if A is true, the result is false; if A is false, the result is true. `A AND B` returns true only if `A` is true <u>and</u> `B` is true. `A OR B` returns true if at least `A` is true <u>or</u> `B` is true. `A XOR B` returns true only if `A` is true <u>or</u> `B` is true, but not if both are true.

The last paragraph described the results of these operations. However, would it be called a truth table if it failed to look like a table? Here is a truth table for the `NOT` operation. The `NOT` operation is known as a unary operation because it only takes one input (thus the un- prefix).

<table class="wikitable" summary="Truth table for NOT operation">
<caption>
`NOT` Truth Table

</caption>
<tr>
<th>
A →

</th>
<th>
False

</th>
<th>
True

</th>
</tr>
<tr>
<th>
</th>
<td>
True

</td>
<td>
False

</td>
</tr>
</table>
How do I read this truth table? Across the top, you have the value of `A`. Underneath each value of `A`, you have the corresponding result. If the value of `A` is `False`, the result is `True`; if the value of `A` is `True`, the result is `False`.

That should be pretty understandable, but the computer deals in ones and zeros, right? Now we translate that same truth table into ones and zeros.

<table class="wikitable" summary="Truth table for NOT operation">
<caption>
`NOT` Truth Table

</caption>
<tr>
<th>
A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
</th>
<td>
1

</td>
<td>
0

</td>
</tr>
</table>
Pretty simple, yes? Take a look at the other truth tables. Notice that they take two inputs, `A` and `B`. The remaining operations are known as binary operations because they take two inputs (thus the bi- prefix). Notice that we now have a grid of results because we have two inputs and the axes are labeled across the top and down the left. Look at each value in the grid and see what value of `A` and what value of `B` produced that result. Does the truth table reflect the logic of the operation? If `A` is `1` `AND` `B` is `1`, is the result `1`?

<table class="wikitable" summary="Truth table for AND operation">
<caption>
`AND` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
0

</td>
<td>
0

</td>
</tr>
<tr>
<th>
1

</th>
<td>
0

</td>
<td>
1

</td>
</tr>
</table>
<table class="wikitable" summary="Truth table for OR operation">
<caption>
`OR` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
0

</td>
<td>
1

</td>
</tr>
<tr>
<th>
1

</th>
<td>
1

</td>
<td>
1

</td>
</tr>
</table>
<table class="wikitable" summary="Truth table for XOR operation">
<caption>
`XOR` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
0

</td>
<td>
1

</td>
</tr>
<tr>
<th>
1

</th>
<td>
1

</td>
<td>
0

</td>
</tr>
</table>
So, those are the basic logic operations. Of course, Boole developed logic algebra, so we cannot leave it at simple operations, can we? However, everything else can be represented as a combination of these simple operations. Just as multiplication can be derived from addition and exponents can be derived from multiplication, so more complex Boolean logic operations can be derived from simple logic operations. Here are some slightly more complex logic operations: `NAND`, `NOR`, and `XNOR`. All of these operations are the result of a simple operation passed through the `NOT` operation, i.e., inverted.

<table class="wikitable" summary="Truth table for NAND operation">
<caption>
`NAND` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
1

</td>
<td>
1

</td>
</tr>
<tr>
<th>
1

</th>
<td>
1

</td>
<td>
0

</td>
</tr>
</table>
<table class="wikitable" summary="Truth table for NOR operation">
<caption>
`NOR` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
1

</td>
<td>
0

</td>
</tr>
<tr>
<th>
1

</th>
<td>
0

</td>
<td>
0

</td>
</tr>
</table>
<table class="wikitable" summary="Truth table for XNOR operation">
<caption>
`XNOR` Truth Table

</caption>
<tr>
<th>
B ↓ A →

</th>
<th>
0

</th>
<th>
1

</th>
</tr>
<tr>
<th>
0

</th>
<td>
1

</td>
<td>
0

</td>
</tr>
<tr>
<th>
1

</th>
<td>
0

</td>
<td>
1

</td>
</tr>
</table>
Do you see how these truth tables are exactly the opposite of the respective truth tables above? We simply negated the results, turning `0` to `1` and `1` to `0`. Believe me, just as algebra can get pretty complex, so Boolean algebra can get pretty complex, but we will not delve into more of the complexity here.

## How does my computer use logic operations?

Computers use transistors to store information and perform various operations. The logic operations above are implemented physically with transistors that make up logic "gates", so you can find logic gates for all of the logic operations listed above, including the inverted operations. Processors use logic gates to perform many tasks, including mathematics and memory access. The internal workings of a process are incredibly complex and the result of decades of innovation.

Also internal to a processor is a clock. While you and I can look at a logic chart and come up with the result, the modern processor is analyzing the results of these operations billions of times each second. In order for the results to make sense, the processor uses the clock to time the operations. Without using this device, the computer might not match up the result with the right operation.

Compare it to this situation. You work in one office and your supervisor works across the street in another office. Two messengers are always walking back and forth between you and your supervisor, picking up what is in your outbox and taking it to your supervisor. The messengers take exactly five minutes to travel between the two desks, regardless of direction, and time each other so one is picking up what is in your outbox when the other is delivering the previous batch to your supervisor. Due to the impeccable timing and performance of the messengers, your supervisor knows (within a five minute window) when you did the work. The computer uses a similar system in conjunction with the clock to time its operations with the results.

## Do programmers really think in ones and zeros?

Perhaps a few programmers think in ones and zeros, but most programmers do not. Binary is a reasonably efficient number system (after ternary, base 3, and quaternary, base 4), but most people find it cumbersome. Today, most people use a decimal number system, but decimal is not very compatible with binary. As a compromise, programmers have worked with octal (base 8) in the past, but hexadecimal (base 16) is more common today.

### How do you write in octal and hexadecimal?

Ready for some math? We are going to look at exponents and bases for a moment. Why are octal (base 8) and hexadecimal (base 16) reasonable compromises for working with binary compared to decimal (base 10)? Octal works because 8 is equal to 2<sup>3</sup>, so each octal digit represents three (and exactly three) binary digits. Hexadecimal works because 16 is equal to 2<sup>4</sup>, so each hexadecimal digit represents four (and exactly four) binary digits.

Decimal, base 10, means that there are ten digits involved in writing numbers in that system. We start with zero and go up to nine. Just as we start at zero and count up, so does the exponent on the base start at zero and count up. Though we may not tend to think about it this way, these first ten numbers (0 through 9) are multiplied by 10<sup>0</sup>. Why do we not tend to think about it this way? That is probably because 10<sup>0</sup> is 1 and any number multiplied by 1 is equal to itself (the identity property of multiplication). When we exhaust our ten digits, we add another in front and that digit is multiplied by the base to the power of the next exponent. In this case, that is 10<sup>1</sup>, or simply 10. So now we have 1 × 10<sup>1</sup> + 0 × 10<sup>0</sup>. We continue on up, getting to 99 (9 × 10<sup>1</sup> + 9 × 10<sup>0</sup>) and continuing to 100 (1 × 10<sup>2</sup> + 0 × 10<sup>1</sup> + 0 × 10<sup>0</sup>). Do you see how this works?

Now we extend this to octal. Just as decimal, base 10, has ten digits, so octal, base 8, has eight digits: 0 through 7. (You can clarify that you are writing in octal by writing the base as a subscript after the number, as in 10<sub>8</sub>.) We start with 0 and go to 7 and we have run out of digits. Just as we did with decimal when we ran out of digits, we add another number in front. So 10<sub>8</sub> is 1 × 8<sup>1</sup> + 0 × 8<sup>0</sup>. When we get to 63<sub>10</sub>, we have 77<sub>8</sub> (7 × 8<sup>1</sup> + 7 × 8<sup>0</sup>). As we continue, 64<sub>10</sub> is represented as 100<sub>8</sub> (1 × 8<sup>2</sup> + 0 × 8<sup>1</sup> + 0 × 8<sup>0</sup>).

Hexadecimal works much the same way, but we need to come up with more digits. Our decimal system only has ten digits, but a hexadecimal system, base 16, needs sixteen digits. As a result, we use the first six letters of the English alphabet to supplement, meaning that hexadecimal digits start at 0 and go to F. (Technically, case doesn't matter, so bd and BD are the same number. This article will use uppercase.) So you get to F<sub>16</sub> and the next number, 16<sub>10</sub>, is represented as 10<sub>16</sub> (1 × 16<sup>1</sup> + 0 × 16<sup>0</sup>). The next place is introduced when you get to 256<sub>10</sub>, which is written as 100<sub>16</sub> (1 × 16<sup>2</sup> + 0 × 16<sup>1</sup> + 0 × 16<sup>0</sup>).

Do you remember how I said that octal and hexadecimal are used because they have these nice ratios to binary digits (one octal digit to three binary digits, one hexadecimal digit to four binary digits)? We can look at a couple of examples. Take a look at this table.

|Binary|Octal|Hexadecimal|Binary|Octal|Hexadecimal|
|:-----|:----|:----------|:-----|:----|:----------|
|0000 0000|00|00|0001 0000|20|10|
|0000 0001|01|01|0001 0001|21|11|
|0000 0010|02|02|0001 0010|22|12|
|0000 0011|03|03|0001 0011|23|13|
|0000 0100|04|04|0001 0100|24|14|
|0000 0101|05|05|0001 0101|25|15|
|0000 0110|06|06|0001 0110|26|16|
|0000 0111|07|07|0001 0111|27|17|
|0000 1000|10|08|0001 1000|30|18|
|0000 1001|11|09|0001 1001|31|19|
|0000 1010|12|0A|0001 1010|32|1A|
|0000 1011|13|0B|0001 1011|33|1B|
|0000 1100|14|0C|0001 1100|34|1C|
|0000 1101|15|0D|0001 1101|35|1D|
|0000 1110|16|0E|0001 1110|36|1E|
|0000 1111|17|0F|0001 1111|37|1F|

If you compare the binary and the octal, you will notice that the right-most octal digit cycles four times from 0 to 7 and each matches perfectly with the same three right-most digits in the binary column. Because of the 1:3 ratio between octal and binary and the 1:4 ratio between hexadecimal and binary, you can use a lookup table like this to switch between the three. If I write BD<sub>16</sub> (189<sub>10</sub>), we can use the table to translate that to 1011 1101<sub>2</sub>, move the spaces around (10 111 101<sub>2</sub>), and translate that to 275<sub>8</sub>. Do you see how that works? Try this exercise with some other numbers.

## How is data measured?

Data and memory are measured in bits, nibbles, bytes, and pseudo-metric extensions of bits and bytes. A bit is stored with a single switch and its value can be represented by exactly one binary digit. A nibble is four bits and its value can be represented by exactly one hexadecimal digit. A byte is eight bits (two nibbles) and its value can be represented by two hexadecimal digits.

### Measuring bytes

What do I mean by pseudo-metric extensions of bits and bytes? A kilometer is 1,000 meters, right? When first measuring large amounts of memory, metric prefixes were used to represent powers of two approximately equal to the corresponding metric prefix. Thus, a kilobyte was 1,024 (2<sup>10</sup>) bytes, not 1,000 bytes. A megabyte was 1,024 kilobytes, not 1,000 kilobytes. Even though the <abbr title="International Electrotechnical Commission">IEC</abbr> has recommended the use of modified prefixes (kibi-, mebi-, gibi-, etc.), many people still use the standard metric prefixes.

|Unit|Exponent|Number of bytes|
|:---|:-------|:--------------|
|kibibyte, KiB|2<sup>10</sup>|1 024|
|mebibyte, MiB|2<sup>20</sup>|1 048 576|
|gibibyte, GiB|2<sup>30</sup>|1 073 741 824|
|tebibyte, TiB|2<sup>40</sup>|1 099 511 627 776|
|pebibyte, PiB|2<sup>50</sup>|1 125 899 906 842 624|
|exbibyte, EiB|2<sup>60</sup>|1 152 921 504 606 846 976|

### Measuring bits

To add to the confusion even more, metric prefixes will sometimes be applied to bit as well, particularly in reference to network speeds. Network speeds have always been measured in bits per second because that was the equivalent for computers to the baud rate (named for Émile Baudot), a standard measure for telegraph and telephone transmission. Computers still transmit information over telephone wires (credit card machines, dial-up internet connections) and coaxial cable (broadband cable internet) as they did when connecting at 300 bps (bits per second), but technology has advanced to the point that many dial-up connections are capable of at least 33.6 Kbps and broadband connections are capable of several Mbps.

Network speeds do tend to use the decimal version of the metric prefixes, but notice that they are multiplied by bits. Most memory is measured in bytes, but data speeds are measured in bits. So, when you see that your computer has a 100 mega<u>bit</u> network connection, remember that it is only transmitting about 12 mega<u>bytes</u> per second.

## How does it help to know about memory sizes and hexadecimal?

So, a bit is actually an abbreviation for a "binary digit", meaning that it is either a zero or a one. A byte is eight bits, eight binary digits. Since byte and bite are homophones, half a byte is a nibble (four bits). Remember how a hexadecimal digit exactly represents four binary digits? A nibble equates to a hexadecimal digit, so it is often represented that way. A byte, being two nibbles, is often represented by two hexadecimal digits.

One of the primary uses of hexadecimal in web development is color codes. Though this is not the place to delve deeply into color in web development, I will introduce the use of hexadecimal. Historically, web browsers have accepted 24-bit color codes, eight bits for each of the three primary colors of light: red, green, and blue. (This is why these are also known as RGB codes.) These color codes would be represented in hexadecimal, each color ranging from 00 to FF. Since the absence of light is black, black was represented by \#000000. Since the presence of all light is white, white was represented by \#FFFFFF. Along similar lines, \#FF0000 was bright red ("red"), \#00FF00 was bright green ("lime"), and \#0000FF was bright blue ("blue"). You could also provide darker colors by using lower numbers: \#800000 ("maroon"), \#008000 ("green"), and \#000080 ("navy").

