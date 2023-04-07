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
![power button](https://user-images.githubusercontent.com/111486111/229915329-cc5e5c3b-cfd7-4313-8c57-f2a02e36c3bb.png)

Do you see how the iconic power button is comprised of a zero and a one? The zero represents the device being off, and the one represents the device being on.


### How Do you Read Binary?
> Since binary is a base two system, we can count in binary by


# Boolean Expressions
> definition here



### Truth Tables
> <mark>Truth tables</mark> represent the possible inputs and outputs of the logical operations of AND, OR, NOT, and XOR.

![truth tables]({{site.baseurl}}/assets/images/truthtables.png)


# How is Binary Related to Boolean Expressions?

<mark>Binary and Boolean expressions</mark> are closely related because Boolean expressions are typically used to evaluate binary values, which can either be true or false (1 or 0).

Binary values are used to represent information. Boolean expressions are used to express the logical operations performed on these binary values(AND, OR, and NOT). 

|Operator|	Logical Operation|
|---|---|
|and	|Conjunction|
|or	|Disjunction|
|not	|Negation|


<pre><code>
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
> Here is an example of the use of boolean expressions in real life.


<pre><code>
age = 18
citizen = True

if age >= 18 and citizen:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote.")

You are eligible to vote.

</code></pre>

