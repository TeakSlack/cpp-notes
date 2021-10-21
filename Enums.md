# Enums in C++

## What are they?

Enums serve as wrappers for integers. They are used to give names to those values that can later be checked in `if` statements and such. Enums start from zero and automatically increment. Enums can be set to specific values as well.

```cpp
enum  MoveDirection : int // The colon defines type (defaults to integer)
{
    North, East, South, West
};
```

Enums become especially useful whenever the values checked in an `if` statement should be limited to certain values, as well as making code much more readable.

```cpp
MoveDirection direction = North;

if(direction == North)
    return 0;
```

The name of the enum does not act as a namespace. The values simply exist in the scope they are defined in.
