# Member Initializer Lists in C++

In constructors, members are typically initialized by using the equals operator. Member initializer lists are a different way of initializing members (as the name may imply) but also have at least one major advantage over the conventional way of initializing class members.

```cpp
class Material
{
private:
    std::string m_Name;

public:
    Material()
        : m_Name("Material")
    {
    }
}
```

Initializer lists are always initialized in the order class members are defined in. Member initializer lists give code more clarity by hiding the fairly monotonous task of assigning values to members. The major advantage of member initializer lists is it only constructs objects once. In code not using initializer lists, objects are initialized once with their default constructor then again in the class's constructor.
