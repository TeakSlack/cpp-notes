# Constructors & Destructors in C++

## Constructors

Constructors are a special method ran every time a class or class derivative is instantiated. They are typically used to clear the memory in a newly instantiated class. Constructors always have to be placed in the public section of a class. Constructors always have the same name as their class.

### Default Constructors

In C++, constructors are provided even when not explicitly defined. These are called default constructors. They essentially do nothing but are there regardless.

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

### Parameterized Constructors

Constructors can be overloaded as many times as a programmer would like, given they have different parameters. This is similar to regular functions.

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

### Copy Constructors

Copy constructors initialize a class using another instance of that class by essentially copying the memory of that class to the current class instance. A logical follow-up question is why can't one use an assignment operator instead of a copy constructor? The difference is copy constructors are called whenever a class is initialized while assignment operators are used on an already initialized class.

## Destructors

Destructors are called every time an object is destroyed. They are typically used to clean (or deallocate) any memory that class has used. Per class, there can only be one destructor.

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

### Virtual Destructors

Using a non-virtual destructor in a derived class results in undefined behavior (it differs from compiler to compiler to compiler). Because of this, it is best practice to use a virtual destructor in a base class whenever virtual functions are used, even if the destructor does nothing. This is for the exact same reason that virtual functions are used in the first place.
