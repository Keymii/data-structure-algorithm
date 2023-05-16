# Revision

Before we proceed, we shall look back into some of the basics. 

## *Pointers*

A pointer is a variable that stores the memory address of another variable as its value.

A pointer variable points to a data type (like int) of the same type, and is created with the * operator in C++. 

```
 datatype *var_name;
 ```

## *Referencing and Dereferencing*

Every data or every variable is stored at some definite location in the memory, called its address. In C++, this can be obtained by using the referencing operator ("&"),

```
int var = 12;
int *ptr = &var;     //address of variable var
cout << ptr << endl;     //prints address of variable var
```
Sometimes we want to obtain the values out of the pointer. For this purpose, we use the dereferencing operator (*).

```
cout << *ptr << endl;       //prints 12
```

## *Arrays*

An array is a collection of similar items stored at contiguous memory locations. This makes it easier to calculate the memory location/position of each element. Usually, arrays are 0-indexed.

In C++, the name of the variable assigned to the array is also a pointer of the 0th element of the array. In most languages, elements of an array is accessed using [] operator. For example,

```
int arr[5]={1,5,7,8,2};
cout << arr[2] <<endl;      //prints 7
```

## *Asymptotic Notations* 

### **Big O**
Mathematically, for some function f(n), f(n) is O(g(n)) if there exist positive constant C and n<sub>0</sub> such that,

$0 \leq f(n) \leq Cg(n)$, \
for all n $\geq$ n<sub>0</sub> 

### **Little O**
For some function f(n), f(n) is O(g(n)) if there exist positive constant C and n<sub>0</sub> such that,

$0 \leq f(n) \lt Cg(n)$, \
for all n $\geq$ n<sub>0</sub> 

### **Big $\Omega$** 
For some function f(n), f(n) is $\Omega$(g(n)) if there exist positive constant C and n<sub>0</sub> such that,

$0 \leq Cg(n) \leq f(n)$, \
for all n $\geq$ n<sub>0</sub> 

### **Little $\omega$** 
For some function f(n), f(n) is $\omega$(g(n)) if there exist positive constant C and n<sub>0</sub> such that,

$0 \leq Cg(n) \lt f(n)$, \
for all n $\geq$ n<sub>0</sub>

### **Big $\Theta$**
For some function f(n), f(n) is $\omega$(g(n)) if there exist positive constants C<sub>1</sub>, C<sub>2</sub>  and n<sub>0</sub> such that,

$ 0 \leq C_1g(n) \leq f(n) \leq C_2g(n)$, \
for all n $\geq$ n<sub>0</sub>

**\# Note: There is no little-theta notation!**

-----
[< Previous](./01_introduction.md)  &ensp;  [Next >]()

[Open Table of Content](./00_table_of_content.md) 

-----