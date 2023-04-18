---
layout: post
title: Main Binary Lesson
description: Learn the basics of binary!
image: assets/images/mainlesson.jpg
nav-menu: true
---

# Binary 

### What is Binary?
 - According to [Computer Hope](https://www.computerhope.com/jargon/b/binary.htm): <mark>Binary is a base-2 number system</mark> invented by Gottfried Leibniz that's made up of <mark>only two numbers or digits: 0 and 1.</mark> This numbering system is the basis for all binary code, which writes digital data such as the computer processor instructions **used with your devices every day.**

 - 0 = represents OFF
 - 1 = represents ON
 

### Fun Fact! Connections with Binary

<img src="https://user-images.githubusercontent.com/111486111/229915329-cc5e5c3b-cfd7-4313-8c57-f2a02e36c3bb.png"  width="800">

Do you see how the iconic power button is comprised of a zero and a one? The zero represents the device being off, and the one represents the device being on.


### Binary Vocabulary

<mark>Bit</mark>= A binary digit = the minimum unit of binary information stored in a computer system (only two states: 1 or 0)
<pre><code>
ex. 1 or 0
</code></pre>

<mark>Nibble</mark>= 4 bits or half of a byte
<pre><code>
ex. 0001
</code></pre>

<mark>Byte</mark>= 8 bits or 2 nibbles
<pre><code>
ex. 01110101
</code></pre>


# Boolean Expressions
> A Boolean expression is a logical statement that is either TRUE or FALSE
- compare data to test if data is equal to, greater than, or less than other data


### How is Binary Related to Boolean Expressions?

<mark>Binary and Boolean expressions</mark> are closely related because Boolean expressions are typically used to evaluate binary values, which can either be true or false (1 or 0).

Binary values are used to represent information. Boolean expressions are used to express the logical operations performed on these binary values(AND, OR, and NOT). 

|Operator|	Logical Operation|
|---|---|
|and	|Conjunction|
|or	|Disjunction|
|not	|Negation|


### Truth Tables
> <mark>Truth tables</mark> represent the possible inputs and outputs of the logical operations of AND, OR, NOT, and XOR.

![truth tables]({{site.baseurl}}/assets/images/truthtables.png)


<pre><code>
Examples:

AND:
5 > 3 and 5 == 3 + 2
true
5 < 3 and 5 == 5
false

OR:
5 == 5 or 5 != 5
True
5 < 3 or 5 != 5
False

</code></pre>


### What About a Real Life Example?
> Here is an example of the use of boolean expressions in a real life situation.


<pre><code>
age = 18
citizen = True

if age >= 18 and citizen:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote.")

You are eligible to vote.

</code></pre>


# Conversions with Binary

### Converting Binary to Decimal
> Since binary is a base two system, we can count in binary by using powers of two. 

<img src="https://user-images.githubusercontent.com/111486111/230675163-d49a20b5-f8f4-4997-bb19-c10d5ca72a76.jpg"  width="800">

1. Read from right to left.
2. Each digit is the placeholder for a power of two. As you work your way left, you add one to the power of 2. For an example:
<img src="https://user-images.githubusercontent.com/111486111/230678754-be59dac2-e44d-4902-95a8-730fd72dfcc4.png"  width="800">

Above, you can see that you start with 2<sup>0</sup>, then 2<sup>1</sup>, 2<sup>2</sup> and so on.

3. When you see the digit (bit) as a 1, it means that you are adding that power's value to your "total" Look below for an example:

<mark>Make sure that you are starting with 2<sup>0</sup>, NOT 2<sup>1</sup> </mark>
<pre><code>
ex.
2<sup>0</sup>= 1, so:
0001 = 1

2<sup>1</sup>= 2, so:
0010 = 2

2<sup>2</sup>= 4, so:
0100 = 4

Now add them up!
0111 = 4 + 2 + 1 = 7
</code></pre>


### Converting Binary to Hexadecimal



### Converting Binary to ASCII

<img src="https://user-images.githubusercontent.com/111486111/230680279-a725350e-3e97-4be3-9d21-9eed903f270b.png"  width="800">


**You can play round with [this tool](https://www.computerhope.com/cgi-bin/convert.pl) to convert your text to binary and vise versa**

**[Click Here](https://drive.google.com/file/d/1t9TInY5K0yCfZnKKIW3VBNkqJsw8IzgB/view) to view a full conversion table between binary, hexadecimal, and ASCII**



# Binary Search
> Binary search is an algorithm that helps find an item in a **sorted list** of items by dividing the list in half until the desired item is found. The binary search algorithm starts at the middle of a sorted data set of numbers and eliminates half of the data; this process repeats until the desired value is found or all elements have been eliminated.

<img src="https://user-images.githubusercontent.com/111486111/232641209-44233e34-bff5-4cf1-9c0e-81caeaacb87d.png"  width="800">


- In this example, the target number is 7. Since 7 is greater than 2, the midpoint of the list, we now only search the higher side. When searching the higher side, 7 is still greater than the middle number so we search the higher side again until we reach the target number of 7.


Binary search is an efficient way to scan through larger arrays. A binary search is often more efficient than sequential/linear search when applied to sorted data. This is due to the greatest number of steps required following the format: **log<sub>2</sub>(n)+1**, in which n is the number of items in the array.


- For an example, an array with 10,000 items would only require a maximum of 14 steps (log<sub>2</sub>(10,000)+1 = 14) instead of 10,000 steps for a sequential/linear search. As lists grow larger, binary search can be a great help in decreasing program time and increasing efficiency.

<img src="https://user-images.githubusercontent.com/111486111/232644470-c0212a9d-a94e-49ff-8942-e3b682ef5e51.png"  width="800">

- Binary search also works with a list of strings. We can sort them alphabetically and use the same method to find the desired string.

### Binary Search Trees
> We can represent binary searches with binary tree diagrams. These diagrams help represent the number of iterations required to find a desired item. 

<img src="https://user-images.githubusercontent.com/111486111/232642475-44f78505-45de-47db-9868-b0851889831c.png"  width="800">


# Hacks

<mark>STUDENTS</mark>: COMPLETE HACKS IN NOTEBOOK
    wget here: LINK HERE

<mark>You will NOT be awarded any points for sections that are INCOMPLETE</mark>


<!-- Table -->

<div class="table-wrapper">
	<table>
		<thead>
			<tr>
				<th>Hack</th>
				<th>Grade</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>note taker (fill in the blanks in notebook)</td>
				<td>0.1</td>
			</tr>
			<tr>
				<td>lesson quiz [here]() LINK LESSON <mark>INCORRECT ANSWERS= 0.2 will be awarded</mark></td>
				<td>0.2</td>
			</tr>
			<tr>
				<td>binary conversions practice <mark>IF INCORRECT = 0.2 will be awarded</mark></td>
				<td>0.3</td>
			</tr>
			<tr>
				<td>binary search questions <mark>IF INCORRECT = 0.2 will be awarded</mark></td>
				<td>0.3</td>
			</tr>
			<tr>
				<td>EXTRA CREDIT: translate to octal (show work and explain thought process so no translator)</td>
				<td>0.1</td>
			</tr>
		</tbody>
		<tfoot>
			<tr>
				<td colspan="1"></td>
				<td>/1</td>
			</tr>
		</tfoot>
	</table>
</div>
Meets all expectations (no extra credit): 0.9/1
