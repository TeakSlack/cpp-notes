# Visibility in C++ Classes

## Private

This is the default visibility mode in classes. When a variable is private, only the class it is contained inside can read and write to them, unless it has a friend class or function. Not even derived classes can access a base classes private data.

## Protected

This visibility mode is similar to private in the way that only the class it is contained in can access the data, but derived classes can access that data as well.

## Public

This visibility mode lets anyone access the data that is marked as public.
