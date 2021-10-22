# Pointers in C++

## What are they?

Pointers are very useful for managing and manipulating memory. A pointer is an integer that stores a memory address. Referring to locations by address is much more efficient than referring to locations by themselves, much like the real world (think of the analogy of a neighborhood).

## Raw Pointers

A void pointer is a type-less pointer. It really is just used to hold an address where the type is not important.

```cpp
// To define a pointer and assign a value

int a = 42;
int* ptr = &a; // The & character tells the compiler we want the address of variable a, not the variable itself.
```

Dereferencing a pointer lets one access the data at the address of the pointer. It can be used to either read or write to that data.

```cpp
// To write and then print the contents of the pointer to screen

*ptr = 56;
std::cout << *ptr << std::endl;
```

# References in C++

## What are they?

In terms of purpose, pointers and references are very similar. It is how one writes and uses them that varies. It's syntactic sugar pretty much.

References must reference already existing variables.

```cpp
// To define a reference

int var = 69;
int& ref = var;
```

Keep in mind the variable `ref` only exists in code. When compiled it only really acts an alias.

```cpp
// The following code wil not work as expected.

void increment(int val)
{
    val++;
}

// The following code will work as expected.

void increment2(int& val)
{
    val++;
}

// Keep in mind this code is functionality the same as

void increment3(int* val)
{
    (*val)++;
}
```

Once a reference is defined, the memory address it is referencing cannot be changed. References cannot have a null value either. For this reason, they are safer than pointers as a wild reference is unlikely to exist.

### When should references be used?

References are a very powerful concept to learn and master. They should be used when passing in an argument to a function that is going to be modified, or passing a value in to a `for` loop that will be modified. References avoid copying large data structures which makes your program more memory efficient for only a few more clock cycles (almost no overhead in a modern machine). References could be passed in to `for` loops for this very reason.
