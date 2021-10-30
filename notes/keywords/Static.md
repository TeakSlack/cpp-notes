# Static in C++

## What Is It? (Outside of Classes/Structs)

Setting a variable as static globally means that the variable will not be linked outside of that translation unit. Be very careful with this. It essentially makes a global variable private.

## What Is It? (Inside Classes/Structs)

Declaring a variable as static inside a class/struct makes the variable shared between all instances of that class. Note that static methods cannot access non-static class members. Static methods don't have a class instance passed to them.

## Static Variables in Functions
In future calls to the function, the value of that variable will remain. Essentially it extends the lifetime of that variable to that of the application. It helps to reduce global variables.