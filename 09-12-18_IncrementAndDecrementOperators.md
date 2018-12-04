# _**Operators**_ #

### Increment Operator(++) ###

  The increment operator increases the value of the variable by one each time it is used.

  _**Example:**_

    int c = 0;
    c++; // Or ++c, both do the same thing
    std::cout << c << std::endl; // Prints "1"


### Decrement Operator(--) ###
  This operator decreases the value of the variable by one every time the operator is called.

_**Example:**_

    int c = 1;
    c--; // Or --c, both do the same thing
    std::cout << c << std::endl; // Prints "0"



### While-Loops ###
  While loops are the simplest form of loop. They continue to execute code as long as the qualifiying expression is true.

_**Example:**_

    int count = 0;

    while(count < 3){
      std::cout << "Hi"; //Show that the loop ran
      count++; // Increment the count
    }

  There are several keywords that can be used to modify the behavior of the loop.

_**Example:**_

    continue;

Causes the loop to skip any remaining code and proceed to the next iteration of the loop.

    break;

Causes the loop to skip any remaining code and stop running the loop.


### Do-While Loop ###
  A do-while loop will execute the code in the loop at least once and then evaluate the qualifiying expression.

_**Example:**_

    int count = 0;

    do{
      std::cout << "Hello World" << std::endl; //Prove that the loop ran at least once
      count++; // Increment the count
    }while(count < 3);

  All forms of while loops are dangerous because they can potentially create an infinite loop which will eventually destroy computer memory.

_**Example:**_
    int count = 0;

    while(count < 3); //  Infinite Loop!
    {
      std::cout << "Hello World" << std::endl;
      count++;
    }
