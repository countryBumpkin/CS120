# *Pointers and Memory*
* Pointers
    * How to initialize pointers and use them with memory operations
* Memory
    * Stack and Heap Memory

## Review
Pointers are addresses. Even though they are technically 'numbers' they can not be used as integers or doubles.

Pointers store the address of some variable or array and can only be used with primitive data types.

## Stack
The Stack is a special region of your computer's memory that stores temporary variables created by each function, including the main() function.

* Stack is top down, meaning that the first element goes at the top of the stack
* Very fast
* Don't have to de-allocate variables explicitly
* Space is managed efficiently by the CPU, memory will not become fragmented
* Local variables only
* Variables can not be resized

## Heap
The Heap is a region of your computer's memory that is not managed automatically for you, and is not as tightly managed by the CPU.

* Heap is bottom up, meaning that the first variable is at the bottom of the Heap
* Heap access is slower than stack access
* Variables can be accessed globally
* Variables can be resized

## 'new' Operator
Creates a new dynamic variable that can be resized and returns a pointer to the new variable.

    int *p1;
    p1 = new int; // p1 gets the address of the new integer, the new integer is nameless, so can only be accessed using p1

##### Basic Pointer Example:

    int main(void){
      int *p1, *p2;

      p1 = new int; // New integer on the heap
      *p1 = 42;     // Assign a value to be stored by the nameless int
      p2 = p1;

      // Print the values pointed to by the pointers
      cout << "*p1 == " << *p1 << endl;
      cout << "*p2 == " << *p2 << endl;

      *p2 = 53;
      cout << "*p1 == " << *p1 << endl; // Both print 53
      cout << "*p2 == " << *p2 << endl;

      p1 = new int;
      *p1 = 88;
      cout << "*p1 == " << *p1 << endl; // 88
      cout << "*p2 == " << *p2 << endl; // 53

      cout << "Hope you got those right!" << endl;
      return 0;
    }

##### Checking Success of 'New' Operator
For older compilers, if the pointer is equal to NULL then it has not been initialized.

Newer compilers, on the other hand, will automatically check to make sure the pointer is initialized. If it is not initialized the program will terminate.

## 'delete' Operator
This operator is used to de-allocate dynamic memory.

    int *p;
    p = new int(5); // initialize variable with value of 5
    // do some math...
    delete p; // de-allocate memory

* Used when memory is no longer needed

##### Note
After de-allocating memory using delete, the pointer is not NULL and still points to the memory address. This is known as a "dangling pointer" and if dereferenced will produce an unpredictable result, potentially disastrous.
Instead, pointers should be set to NULL so that they do not point to anything.

###### Example:

    delete p;
    p = NULL;

## 'NULL' Keyword
This means that there is nothing in the variable.

## Dynamic and Automatic Variables:
* Dynamic Variables
    * Created with the 'new' operator
    * Memory must be de-allocated
    * Initialized on the Heap
* Automatic Variables
    * Created on the Stack
    * Automatically de-allocated at the end of the program

## Pointer Variables and Math
Pointers can be indexed using mathematical functions.

##### For Example:

    double *DoublePtr;
    double my_array[20] = {1,2,3,4,5,6,7,8};
    DoublePtr = my_array; // Pointer now points to the first element of the array

Now the value of DoublePtr is the address of my_array[0], DoublePtr + 1 would be the address of my_array[1], and so on.

This means that we can access memory beyond the array by using the indexing improperly, which could cause problems.
