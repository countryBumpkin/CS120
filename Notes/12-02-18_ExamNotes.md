# **CS120 Final Exam Topics** #
***

**These topics will be the focus of the final:**
* Arrays & 2-D Arrays
  * *Declaring & Initializing Arrays*
  * *Passing Arrays to Functions*
* Struct & Class
  * *Parameters(pass-by-reference & call-by-reference)*
  * *Function Overloading and Ambiguity*
* Pointers
  * *Pointer Declaration & Dereferencing*
  * *New and Delete Operators*
  * *Pointer Math*
* Linked Lists
  * *Know how to write code for this stuff*
* Sorting and Search
  * *Binary Search*
  * *5 Types of Sorting*
* Recursion

## Exam Sections And Point Breakdown ##
---

###### *True or False(20pts):* ######

###### *Short Answer(15pts):* ######
* Software Engineering (development, testing)
* Recursion
* Sorting/Searching
* Dynamic memory (Linked Lists)
* Ethics

###### *Program Analysis(20pts):* ######
* Evaluate program output

###### *Programming Section Contents(50pts):* ######
* Recursion
* Linked Lists
* Classes


## *Recursion* ##
---
**recursion:** any function that calls itself
Be able to write recursive fuctions for simple math calculations such as:
* power
* fibonacci
* factorial


    int power(int base, int exponent){
      if (exponent < 0){
          cout "Illegal argument";
          exit(1);
      }
      if(exponent > 0){
        return (power(base, exponent - 1) * base);
      }else{return 1;}
    }
    
    

## *Structures* ##
---
**declaration:** Can be initialized at declaration, generally don't have a constructor.

    struct struct_type{
      int var_1, var_2, var_3;
    }

    struct_type pet = {1, 2, 4}; //Variables are initialized sequentially
    
    

## *Scope* ##
---
1. Block
   * Anything in {}
2. File/Global
   * Essentially global scope
3. Local/Function
   * Only within a function
   
   

## *Professional Ethics for Computer Programmers* ##
---
* Privacy and Misuse of data
* Plagiarism and Software Piracy
* Misuse of a Computer Resource



## *Software Design and Engineering* ##
---

###### **Top-Down Design:** ######
Focuses on working out the high level structure of the program first. This is used for large scale projects.

###### **Bottom-Up Design:** ######
Focuses on writing the base functionality of the program first.

