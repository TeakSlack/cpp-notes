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

## Constructors

Constructors are a special method ran every time a class or class derivative is instantiated. They are typically used to clear the memory in a newly instantiated class.

```cpp
class Example
{
public:
    int A, B;

public:
    Example()
    {
        A = 0;
        B = 0;
    }
};
```

### Default Constructors

In C++, constructors are provided even when not explicitly defined. These are called default constructors. They essentially do nothing but are there regardless.

### Parameterized Constructors

Constructors can be overloaded as many times as a developer would like, given they have different parameters. This is similar to regular functions.

```cpp
class Example
{
public:
    int A, B;

public:
    Example()
    {
        A = 0;
        B = 0;
    }

    Example(int a, int b)
    {
        A = a;
        B = b;
    }
};
```

## Destructors

Destructors are called every time an object is destroyed. They are typically used to clean any memory that class has used.

```cpp
class Example
{
public:
    int A, B;

public:
    Example()
    {
        a = 500;
        b = 499;
    }

    ~Example()
    {
        a = 0;
        b = 0;
    }
};
```

## Structs

Struct is short for structure. Functionally there is very little different between a struct and a class. All members in a struct are public by default. Structs remain in C++ for backwards compatibility with C.

How structs are used differs from coding style to coding style, there is no one right way. A common practice however seems to be to use them to lump together just plain old groups of data.
