# Time Complexity And Space Complexity

Let there be some algorithm.

## *Time Complexity*
The valid algorithm takes a finite amount of time for execution.
 
The time required by the algorithm to solve given problem is called time complexity  of the algorithm. It quantifies the amount of time taken by an algorithm to run as a function of the length of the input.

Let us consider the following algorithm for addition of two scalar variables.
```
Algorithm ADD(int a, int b){
    int c = a + b;
    return c;
}
```
The above algorithm requires one operation, which takes constant time. Hence we say that time complexity of this algorithm is $O(1)$. (remember the big-oh notation?)

Now, take a note of the following algorithm to generate *n*<sup-th</sup- fibonacci series member
```
Algorithm fib(int n){
    if (n == 1) return 0;
    else if (n == 2) return 1;
    else return (fib(n-1) + fib (n-2));
}
```
In the above code, we created a function named fib(), which has an integer as the parameter and return value data type. In the main function, we iterate over a loop from 1 to n times, and at each iteration, called the fib() function. In fib() function, if the parameter passed is 0 or 1, we will return the same value; otherwise, we will return the sum of recursive calls with parameter values one and two less than our current parameter, which is **fib(i-1)+fib(i-2)**.

We can easily find out that the time taken to execute the above recursion is $O(2^n)$ as to calculate each fib(n), we have to calculate f(n-1) and f(n-2), and same repeats for them.

## *Space Complexity*
The space complexity of an algorithm is the amount of memory space required to solve an instance of the computational problem as a function of characteristics of the input. Similar to time complexity, space complexity is often expressed asymptotically in big O notation.

If we need to create an array of size n, this will require $O(n)$ space. If we create a two-dimensional array of size $n^2$, this will require $O(n^2)$ space.

In recursive calls stack space also counts. 

Consider the following algorithm
```
int add (int n){
    if (n <= 0){
        return 0;
    }
    return n + add (n-1);
}
```

here each call add a level to the stack :

1.  add(4)
2.  -- add(3)
3.  --- add(2)
4.  ----- add(1)
5.  ------- add(0)

Each of these calls is added to call stack and takes up actual memory.
So it takes $O(n)$ space.

-----
[< Previous](./02_revision.md)  &ensp;  [Next -]()

[Open Table of Content](./00_table_of_content.md) 

-----