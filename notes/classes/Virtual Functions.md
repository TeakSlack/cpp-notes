# Virtual Functions in C++

## What are they? Why is this grouped in with classes?

Virtual functions are defined in base classes and are later overwritten in derived classes. This mainly is used to achieve runtime polymorphism. Virtual functions are typically implemented by `vtables`, which only take two extra clock cycles in modern machines (this very much negates worries about performance overhead). `vtables` do however take up a little bit more memory.

```cpp
class Component
{
public:
    //This is later to be overwritten in a derived class
    virtual std::string GetName() { return "Generic Component" };
};

class Lever : public Component
{
public:
    // These should always be marked with override to make code more readable
    std::string GetName() override { return "Lever" };
};
```

## Pure Virtual Functions (Interfaces)

In a base class, a virtual function is defined without an implementation and subclasses are made to be the ones to implement functionality. These are very common in OOP.

```cpp
class Component
{
public:
    virtual std::string GetName() = 0;
};

class Lever : public Component
{
public:
    std::string GetName() override { return "Lever" };
};
```

With this little change, the previously defined component class becomes an interface.
