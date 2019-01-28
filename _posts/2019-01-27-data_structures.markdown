---
layout: post
title:      "Data Structures "
date:       2019-01-28 01:58:18 +0000
permalink:  data_structures
---


This post is dedicated to an introduction to basic data structures.

As I approach more interviews, I'm refamiliarizing myself with the different types of data structures available. Coding mainly in Javascript, I've had my hands on arrays most recently but there are quite a few data structures I'd not only not heard of, but needed to refamiliarize myself with. 

 **Arrays**

An array organizes items sequentially, one after another in memory.

Each position in the array has an index, starting at 0.

Strengths:
* Fast Lookups:  Retrieving the element at a given index takes O(1)O(1) time, regardless of the length of the array.
* Fast appends. Adding a new element at the end of the array takes O(1)O(1) time.

Weaknesses:
* Fixed size. You need to specify how many elements you're going to store in your array ahead of time. 
* Costly inserts and deletes. You have to "scoot over" the other elements to fill in or close gaps, which takes worst-case O(n)O(n) time.


**Linked Lists **

A linked list organizes items sequentially, with each item storing a pointer to the next one.

Strengths:
* Fast operations on the ends. Adding elements at either end of a linked list is O(1)O(1). Removing the first element is also O(1)O(1).
* Flexible size. There's no need to specify how many elements you're going to store ahead of time. You can keep adding elements as long as there's enough space on the machine.

Weaknesses:
* Costly lookups. To access or edit an item in a linked list, you have to take O(i)O(i) time to walk from the head of the list to the iith item.
* An item in a linked list is called a node. The first node is called the head. The last node is called the tail.



**Queue**

A queue stores items in a first-in, first-out (FIFO) order. Picture a queue as if you are literally in a 'queue' or line at the store, you will only get to the front by waiting in line. 

Strengths:
* Fast operations. All queue operations take O(1)O(1) time.

**Stacks**
A stack stores items in a last-in, first-out (LIFO) order.

Picture a pile of dirty plates in your sink. As you add more plates, the first plates become buried under the newer plates being added to the stack in a "Last in, first out" order. 

Strengths:
* Fast operations. All stack operations take O(1)O(1) time.

**Hash Table**

A hash table organizes data so you can quickly look up values for a given key. In Javascript, these are objects. 

Strengths:
* Fast lookups. Lookups take O(1)O(1) time on average.
* Flexible keys. Most data types can be used for keys, as long as they're hashable.

Weaknesses:
* Slow worst-case lookups. Lookups take O(n)O(n) time in the worst case.
* Unordered. Keys aren't stored in a special order. If you're looking for the smallest key, the largest key, or all the keys in a range, you'll need to look through every key to find it.
* Single-directional lookups. While you can look up the value for a given key in O(1)O(1) time, looking up the keys for a given value requires looping through the whole dataset—O(n)O(n) time.
* Not cache-friendly. Many hash table implementations use linked lists, which don't put data next to each other in memory.

At this moment, we're missing one more major data structure, a tree.  To be continued... 


