---
layout: post
title: Binary Search Lesson
description: Binary Search In-Depth
image: assets/images/dude.jpeg
nav-menu: true
---

## What is Binary Search?
> Binary search is an algorithm for finding the position of a target value within a sorted array. It works by repeatedly dividing the search interval in half, comparing the middle element of the interval with the target value, and narrowing the search interval based on the comparison.

## Another way to think about it

Imagine you are looking for a particular word in a dictionary with thousands of pages. Instead of starting at the first page and flipping through every page until you find the word (which would take a long time), you can use a binary search algorithm to quickly find the word.

> Here's how it works:

1. First, you open the dictionary to the middle page.

2. You compare the word on the middle page with the word you are looking for.

3. If the word you are looking for is equal to the word on the middle page, you have found it and you are done.

4. If the word you are looking for is less than the word on the middle page, you know that the word must be on one of the pages to the left of the middle page. So, you discard the right half of the dictionary (i.e., all the pages to the right of the middle page) and repeat the process on the left half of the dictionary.

5. If the word you are looking for is greater than the word on the middle page, you know that the word must be on one of the pages to the right of the middle page. So, you discard the left half of the dictionary (i.e., all the pages to the left of the middle page) and repeat the process on the right half of the dictionary.

6. You continue this process, dividing the remaining pages in half each time, until you find the word or determine that it is not in the dictionary.

> Using binary search in this way is much faster than flipping through every page of the dictionary, especially for large dictionaries. Similarly, binary search is very efficient for finding a particular value in a sorted list or array, and can save a lot of time compared to searching through the entire list or array linearly.

## How can binary search be used?

> Here are two ways as examples, but there are more.

1. Finding an element in a sorted array: Suppose you have a sorted array of integers and you want to find the index of a specific value in the array. You can use binary search to quickly locate the index of the value by repeatedly dividing the search space in half. For example, if you are looking for the value 10 in the array [1, 3, 5, 7, 10, 13, 15], binary search would first compare the middle value (7) to 10, discard the left half of the array since 10 is greater than 7, and then repeat the process on the right half of the array. In this way, binary search can quickly find the index of the value (in this case, index 4).

2. Finding the square root of a number: Suppose you want to find the square root of a positive number x. You can use binary search to quickly approximate the square root by repeatedly dividing the search space in half and comparing the square of the midpoint to x. For example, if you are looking for the square root of 25, binary search would first check the midpoint (5) and compare its square (25) to the target value. If the square of the midpoint is greater than 25, binary search would discard the right half of the search space and repeat the process on the left half of the search space (in this case, [0, 5]). In this way, binary search can approximate the square root of a number with a high degree of accuracy.


### Activity Idea with students:

1. Write down a list of numbers (e.g., 1, 3, 5, 7, 9, 11, 13, 15) on a piece of paper or whiteboard.

2. Ask your partner to choose a number from the list (without telling you which one they chose).

3. Your partner will then try to guess your number using binary search. Begin by guessing the middle number in the list (in this case, 7).

4. Ask your  partner whether their number is greater than, less than, or equal to your guess of 7.

5. Based on their response, eliminate either the left or right half of the list and repeat the process, guessing the middle number of the remaining half.

6. Continue this process of dividing the remaining numbers in half and guessing the middle number until you guess your partners number correctly.

- For example, if your partner chose the number 9, the process might look like this:

    - Guess 7
    -  says their number is greater than 7
    - Eliminate the left half of the list (1, 3, 5, 7)
    - Guess 11 (the middle number of the remaining half)
    -  says their number is less than 11
    - Eliminate the right half of the remaining numbers (13, 15)
    - Guess 9 (the middle number of the remaining half)
    -  says you guessed their number correctly!

## Advantages of Binary Search:
- Binary search is faster than linear search, especially for large arrays. As the size of the array increases, the time it takes to perform a linear search increases linearly, while the time it takes to perform a binary search increases logarithmically.
- Binary search is more efficient than other searching algorithms that have a similar time complexity, such as interpolation search or exponential search.
- Binary search is relatively simple to implement and easy to understand, making it a good choice for many applications.
- Binary search is well-suited for searching large datasets that are stored in external memory, such as on a hard drive or in the cloud.
- Binary search can be used as a building block for more complex algorithms, such as those used in computer graphics and machine learning.

## Disadvantages of Binary Search:
- We require the array to be sorted. If the array is not sorted, we must first sort it before performing the search. This adds an additional O(N * logN) time complexity for the sorting step, which makes it irrelevant to use binary search.
- Binary search requires that the data structure being searched be stored in contiguous memory locations. This can be a problem if the data structure is too large to fit in memory, or if it is stored on external memory such as a hard drive or in the cloud.
- Binary search requires that the elements of the array be comparable, meaning that they must be able to be ordered. This can be a problem if the elements of the array are not naturally ordered, or if the ordering is not well-defined.
- Binary search can be less efficient than other algorithms, such as hash tables, for searching very large datasets that do not fit in memory.

## Applications of Binary Search:
- Binary search can be used as a building block for more complex algorithms used in machine learning, such as algorithms for training neural networks or finding the optimal hyperparameters for a model.
- Commonly used in Competitive Programming.
- Can be used for searching in computer graphics. Binary search can be used as a building block for more complex algorithms used in computer graphics, such as algorithms for ray tracing or texture mapping.
- Can be used for searching a database. Binary search can be used to efficiently search a database of records, such as a customer database or a product catalog.














