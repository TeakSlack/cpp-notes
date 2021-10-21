# Enums in C++

## What are they?

Enums serve as wrappers for integers. They are used to give names to those values that can later be checked in `if` statements and such. Enums start from zero and automatically increment. Enums can be set to specific values as well.

```cpp
enum  Direction : int // The colon defines type (defaults to integer)
{
    North, East, South, West
};
```

Enums become especially useful whenever the values checked in an `if` statement should be limited to certain values, as well as making code much more readable.

```cpp
// This limits the values of this variable to what is defined inside the enum
Direction direction = North;

if(direction == North)
    return 0;
```

The name of the enum does not act as a namespace. The values simply exist in the scope they are defined in, as shown in the example above. Enum types have some limitations however, such as they limit the names of all enums to be used only once and are not type-safe. There is a solution for this however.

## Enum Classes

Introduced in C++11, enum classes are strongly typed and scoped. They don't allow conversion to ints and cannot be compared with enums from other enum classes.

```cpp
enum class Direction {North, East, South, West};

Direction dir = Direction::East;

if(direction == Direction::South)
    return 0;
```

The following code will not compile as it breaks how enum classes are used.

```cpp
enum class Direction {North, East, South, West};

Direction dir = Direction::East;

if(direction == 1)
    return 0;

// or

enum class Direction {North, East, South, West};

enum class Color {Red, Green, Blue};

Direction dir = Direction::East;

if(direction == Color::Green) // This otherwise would compile with standard enums
    return 0;
```
