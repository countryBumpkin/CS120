# _**Structures and Classes**_ #
C++ is an object oriented programming language. It allows the programmer to manipulate computer memory to create blocks of memory that form _objects_. Objects are uniform data sets that the programmer can compare, store, and perform operations on. There are two fundamental types of objects called _classes_ and _structures_.

## Structures ##
Structures are the simplest of objects. They are meant to efficiently store data in the from of smaller data types, often primitive data types such as ``int``, ``char``, etc. Structures have low overhead memory.

Example:
    
    struct apple{
      int weight; // First member variable
      char color[5] = "green"; // Second member variable
    };
    
Instances of ``struct apple`` can be created using:

    struct apple red_delicious; // Creates a new apple without initializing the two member variables
    apple granny_smith; // Does the exact same thing as the first example
    apple fuji = {5, "yellow"}; // Although this example creates a new instance of apple, it also sets the weight to 5 and color to "yellow"
    
    
Although this works in C++, it is interesting to note that in C an error will be thrown if the following code is used:

    apple red_delicious;
   
This is because ``apple`` is defined in the tag namespace for ``struct``s while other objects are part of the ordinary identifiers. This has the potential to cause bugs when compiling C programs as C++. Instead use:
    
    // Declare the struct like so:
    typedef struct apple{...};

    // Then this will work just fine:
    apple red_delicious;
    
Again, this is beyond the scope of this class but knowledge is power.

## Classes ##
In C the differences between ``struct`` and ``class`` are significant, but in C++ there is little difference. In general though, you should try to only use classes when the objects are going to have specific functions that are performed on them.

    class fruit{
    private: // Private data members and functions can only be accessed/called by the other functions in the class
      int weight;
      int height;
      
    public: // Any function or variable here can be accessed from any function or outside functions
      fruit(int, int);
      fruit(); // Default constructor
      ~fruit(); // Deconstructor
      
      int func1(); // Function prototype, function implementation is outside class
      int func2(int a){ // Functions can be declared and defined in the class
        weight = a;
      }
    };
    
    fruit::fruit(){ // Since this function is defined outside the class, the scope modifier must be used to to link the function to the class
      //...
    }
    
    fruit::fruit(int weight, int height){
      this->weight = weight;
      this->height = height;
    }
    
    fruit::~fruit(){
      // Delete all member variables created on the heap
      // See [Pointers](https://github.com/countryBumpkin/CS120/blob/master/10-31-18_Memory%26Pointers.md)
    }
    
    fruit::func1(){ // This function must also be implemented outside the class
      //...
    }
    
 That sums up the basics of classes...
 
_**NOTE:**_ To learn more about heap memory see [Pointers & Memory]()
