# Pointers and Arrays Continued

### Passing Arrays to Functions Using Pointers
    void change_ptr(int *ptr); // Declare the function to pass the pointer to

    int main(void){
      int *func_ptr;
      func_ptr = new int;
      *func_ptr = 77;
      change_ptr(func_ptr);

      return 0;
    }

  Pointers can be passed to a function using a pointer like so:

    double sum(double *arr_ptr, int size);


  In this case, the address of the first element of the array is passed to the function. Then, by incrementing and decrementing the pointer we can access the various elements of the array, provided that we know the size of the array. By knowing the size of the array we can ensure that we will never go out of bounds.

  It is effectively the same as this:

    double sum(double arr_ptr, int size);

  In that both pass a pointer to the function.

  Also, both can be called like so:

    double arr[2] = {1,2};
    sum(arr, 2);

##### Note:
*Arrays can not be returned from functions, but pointers to arrays can.*

### Returning Arrays from Functions
Looking at the following code snippet we can see there are a few problems...

    int* my_function(void){
      int arr[100]; // Create a new array
      return arr; // Return the array to the calling function so that it can be used
    }

The primary problem is that the array of 100 elements that we create is deconstructed after the function returns. Therefore, the pointer we return will point to nothing.

There are a couple of ways to get around this:

    //first
    int* my_function(void){
      int arr = new int[100]; // Using the 'new' operator
      return arr;
    }
    // Note: make sure you use the destructor to delete the array when you are done with it
    // This is because the variable is initialized on the heap

    //second
    int* my_function(void){
      static int arr[100]; // This array is initialized at the beginning of the program
      return arr;
    }

Hooray!

### Dynamic Objects and Arrays of Objects
When we create a dynamic object

    object *my_object = new object();

The object must be referenced with a pointer like the one above. We can still use the '.' operator on the pointer to our object, but we must make sure to dereference the object first.

    (*my_object) = new object();

### Arrow Operator (->)
This can be used to combine the dereference operator, '*', and the dot operator,'.'. There is no functional difference, but the syntax is slightly simpler.

    my_object->name = "ALICE";
    my_object->getName();

### Destructors (~)
When using a class with dynamic memory operations we will always want to delete the variables we have created when we are done with the class. To perform these operations we will use a destructor function which is designated by the '~', or tilde. Only one destructor may be specified per class and it is just like a constructor in that it has no parameters and no return type.

Example:

    // prototype is included in class definition like so
    // ~MyClass();
    MyClass::~MyClass(){
      // delete some stuff
    }
