# **Pointers** #
---
Pointers are typed, which means they are not of type ``int``, ``double``, or other primitive data types. They are their own data type and can be read as "variable 'a' is a pointer to some other variable".

Pointers can also be assigned like normal variables... and can be used to change the value at the memory address they are storing.

## Pointer Declaration ##
Pointers must be the same type as the variable they are pointing to so that the pointer can access all the data in the memory address.

_**For Example:**_

    double *a; // This is a pointer to a double variable

_**And more generically:**_

    datatype *pointer_variable;

**Note:**
*the pointer operator does not need to directly follow the data type or variable name which can lead to confusing syntax.*

# **Pointer Dereferencing Operator (*)** #
---
Pointer variables can be dereferenced to return the value stored at the location in memory.

_**For Example:**_

    int b = 7;
    int *a = &b;
    std::cout << "value of b = " << *a << std::endl; // Prints the value stored at the memory address held by variable a


# **& Operator (Address of Operator)** #
---
This operator returns the address of the variable it is attached to

  Example:

    int a;
    std::cout << "Address of a is " << &a << std::endl; // This will print the location in memory of the variable
