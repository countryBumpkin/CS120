# *Dynamic Arrays and Function Calls with Pointers*
* How to pass pointers to functions
* How to initialize and use dynamic arrays

## Function Calls With Pointers

    void change_ptr(int* temp){ // <- This is the call with function
      * temp = 99; //
    }

To pass a pointer to a function, namely the one above, use the following code:

    int* pntr;
    change_ptr(pntr);

## Dynamic Arrays
Dynamic Arrays can be used to save memory by resizing arrays with 'new' operator.

  Example:

    double* d;
    d = new double[10]; // Creates a dynamically sized array with 10 elements

    // Delete the array
    delete [] d; // requires the brackets to remove the array
