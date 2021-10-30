# Strings in C++

Strings are a group of characters, represented in many different forms.

`char*`'s are not heap allocated, and therefore do not have to be deleted. `char*` or `char[]` strings are actually just arrays, and therefore have a set length that cannot be changed.

Strings are ended by a null termination character (`0x00`).

## C++ strings

In C++, a class called `std::string` is available. It is a templated structure that can be expanded in length and exposes many helpful functions.

```cpp
#include <string>

std::string example = "This is an example string";
```

Read-only strings passed in to functions should be by a `const` reference.

```cpp
void StrFunc(const std::string& exString);
```