# Arrays
  Hypothetical Question:
    How would you collect the scores of 30 students and calculate the average
    score of the students.

  _**Definition:**_

    A collection of data members of the same data type

###### Declaring and Initializing Arrays:
    int score[5];

    int score[5] = {0, 1, 2, 3, 4};
    int score[5] = {0, 1, 2, 3, 4, 5}; // Error will be thrown

    int score[5] = {0,1,2,3}; // score[4] will be initialized to 0


# Looping
  C++ will allow you to go beyond the max or min index of the array which will result in some funky and unpredictable behavior.

_**Tips and Best Practice:**_
* Use const int to store the size of the array. This makes the array fixed. If the array is not declared using a const qualifier, the array may be resized to include more memory. This is dangerous because you may create memory leaks or share memory allocation with another program.



# Call By Reference

  Call by reference passes a reference to a function instead of a data type.
This means that any assignment to the variable inside the function will modify the value of the variable outside of the function also.

_**Example:**_
    #include <iostream>
    
    void myFunction(int &a, int &b){
      a = a * b; // This changes the value of a outside the function
    }
    
    int main(void){
      int a = 4;
      int b = 3;
      
      myFunction(a, b);
      
      std::cout << "a = " << a << std::endl; // Prints: a = 12
      std::cout << "b = " << b << std::endl; // Prints: b = 3
      
      return 0;
    }
