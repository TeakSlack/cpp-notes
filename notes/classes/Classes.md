# Classes in C++

C++ does not enforce OOP. However classes are very useful and many choose to use them regardless.

## What Are They?

At their core, classes are ways to group data (variables and functions). They don't add any extra functionality, one can write code with the same function with or without classes.

```cpp
class Example
{
public:
    int a, b;

public:
    void mutateA(int newA)
    {
        a = newA;
    }
}; // It must have a semicolon at the end!
```

Note the use of the `public` keyword. This denotes the visibility of the members defined below it.

## Structs

Struct is short for structure. Functionally there is very little different between a struct and a class. All members in a struct are public by default. Structs remain in C++ for backwards compatibility with C.

How structs are used differs from coding style to coding style, there is no one right way. A common practice however seems to be to use them to lump together just plain old groups of data.
