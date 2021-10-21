# Class Inheritance in C++

## What is it?

Inheritance is a way to avoid code duplication. It most typically follows the example of a base class in which other classes with similar functionalities brach off of.

```cpp
class Entity
{
public:
    float X, Y;

    void Move(float xa, float ya);
}

class Player : public Entity
{
public:
    const char* name;

    void ChangeName(const char* newname);
}
```

This example comes from [Cherno](https://www.youtube.com/watch?v=X8nYM8wdNRE). The player class now inherits all the properties of its base class (`X`, `Y`, and the `Move` function) as well as implements its own logic needed for the player.

One should note that anything not made private by the super class is accessible by the child class.
