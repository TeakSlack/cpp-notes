# Const in C++

## Const without pointers

```cpp
const int a = 5;
```

This sets the value `a` to have a constant, unchangeable (with some exceptions) value of 5. There isn't much more to `const` in this context than that.

## Const pointers

```cpp
int a = 11;
const int* b = &a;

// or

int const* c = &a;
```

The following code will not let the developer change the contents of the value that is being pointed to. This doesn't mean the pointed to value is constant, it merely means it cannot be modified through that pointer.

## Pointer consts?

```cpp
int* const b = &a;
```

An int pointer followed by the const keyword will make the address of the pointer constant. It is like a reference in this regard.

## Const functions

```cpp
class Example
{
private:
    int m_A;
public:
    int GetA() const
    {
        return m_A;
    }
};
```

The final usage of `const` is in methods. It lets the compiler know that this method will not change the variables it is operating on. This is most commonly seen in getters.
