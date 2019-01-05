---
layout: post
title:      "Understanding Big O Notation"
date:       2019-01-05 22:10:09 +0000
permalink:  understanding_big_o_notation
---


It hasn't yet clicked completely for me, but I'm on my way to working out the kinks. Join me. 

The simple part: 

**What is Big O Notation?**

*Big O Notation is a way to represent how long an algorithm will take to execute. It enables a software Engineer to determine how efficient different approaches to solving a problem are.*

Ok this makes me feel better, I feel like I must then in a non technical way go through Big O Notation in *everything* I do in my life.  It's one of my big pet peeves actually, people who do things inefficiently.  Especially things that aren't fun to do... 

like.... taking the dishes out of the dishwasher and sorting each item to its respective spot ... or packing a car full of suitcases that you don't actually know will fit.. until they do. 

I know I'm not the only one. 

**Common Time Complexities**

O(1) - Constant time complexity

Constant time complexities will always take the same amount of time to be executed regardless of what the approach is. 

```
var arr = [ 1,2,3,4,5];
arr[2]; // => 3


time complexity : O(1) 
```

 It means that it takes the same amount of time to look up a value in your collection whether you have a small number of items in your collection or very very many items.

**O(n)  - Linear time complexity**

An algorithm has a linear time complexity if the time to execute the algorithm is directly proportional to the input size n . Therefore the time it will take to run the algorithm will increase proportionately as the size of input n increases.

Analogy:  reading a book, where n is the number of pages.

```
for (var i = 0; i < array.length; i++) {
  console.log(array[i]);
}

array = ['Sally', 'Kim', 'Sandy', 'John'] // 4 steps 
array = ['Jim', 'Jacob'] // 2 steps 
```

**O(log n) - Logarithmic time complexity **

This is when it starts to get trickier. 

An algorithm has logarithmic time complexity if the time it takes to run the algorithm is proportional to the logarithm of the input size n. An example is binary search, which is often used to search data sets:

* this example was taken from Cracking the Code Interview: 



```
search 9 within {1, 5, 8, 9, 11, 13, 15, 19, 21} 
compare 9 to 11 -> smaller. 
search 9 within {1, 5, 8, 9, 11}
compare 9 to 8 -> bigger
search 9 within {9, 11}
compare 9 to 9
return
```
We start off with an N-element array to search. Then, after a single step, we're down to n/2 elements. One
more step, and we're down to n/4 elements. We stop when we either find the value or we're down to just
one element.

The total runtime is then a matter of how many steps (dividing N by 2 each time) we can take until N
becomes 1. // this is the part that really matters, how many steps does it take? 

```
N = 16
N= 8  // divide by 2 
N= 4 // divide by 2 
N= 2 // divide by 2 
N =1 // divide by 2 

``` 

We could look at this in reverse (going from 1 to 16 instead of 16 to 1 ). How many times we can multiply 1
by 2 until we get N?

```
N= 1 // multiply by 2 
N = 2  // multiply by 2 
N= 4  // multiply by 2 
N 8   // multiply by 2 
N= 16
```

Other O(log N) Example: 

```
for (var i = 1; i < n; i = i * 2)
  console.log(i);
}
```

Other O(log N) Example:

```
for (i = n; i >= 1; i = i/2)
 console.log(i);
}

```

When you see a problem where the number of elements in the
problem space gets halved each time, that will likely be a 0( log N) runtime. 


**O(n^2) - Quadratic time complexity**

An algorithm has quadratic time complexity if the time to execution it is proportional to the square of the input size.

Quadtratic time complexity can be found in nested for loops. In fact, the deeper nested loops will result in O(n^3), O(n^4), etc.

```
for(var i = 0; i < length; i++) {     //has O(n) time complexity
    for(var j = 0; j < length; j++) { //has O(n^2) time complexity
      // More loops?
    }
}

```

**Drop the Constants and Non-Dominant Terms**: 

Sometimes we're working with algorithms that have large numbers (N^2 or even 2^N) that the constants like (2N) don't matter. For example if N= 10 and we wanted to figure out N^2 * 2^N + 2N= 1144 but of that 1144 2N makes up just 20 while N^2 is 100 and 2^N is 1024. Think about what would happen if N = 100? As a result, drop the constants and non-dominant terms. 

Which of the following are equivalent to O(N)? Why?

```
O(N + P), where P < X
```

Explanation:

 If P < X, then we know that N is the dominant term so we can drop the 0( P) => O(N)

```
0(2N)
```

Explanation:

0(2N) isO(N) since we drop constants


```
O(N + log N)
```

Explanation: 

O(N) dominates O(log N), so we can drop theO(log N). See graph for help: 

![](https://qph.fs.quoracdn.net/main-qimg-dc31e536ddf8f450632a848c33c5cc03)

```
O(N + M)
```

Explanation: 

There is no established relationship between N and M, so we have to keep both variables in there.

Therefore, all but the last one are equivalent to O(N). 


There's a significant amount more to understand as I dive deeper into Big O Notation but I find these concepts are a good start to making things click, and I hope you found it helpful! 

