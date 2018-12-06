# _**Writing and Reading From Files**_ #
These notes cover reading from and writing to files using the ``fstream`` library in C++.

## _**Writing to Files**_ ##
Writing to files uses the ``ofstream`` library. Below is example code outlining how to to open the file, write some text to it, and then close the file:

    #include <fstream> // This is the only library needed
    
    int main(void){
      std::ofstream outfile; // Declare a file to write to. At this point **outfile** is not linked to a file
      
      /* Alternatively, we can declare and open the file on one line using: 
        std::ofstream outfile("filepath"); // Opens the file at the path
      */
       
      outfile.open("filepath"); // Open the file
      outfile << "some text"; // Write some text to the file
      
      outfile.close(); // Close the file
      
      return 0;
    }
    
## _**Reading From Files**_ ##
In order to read from a file we need the ``ifstream`` library and the following code:  

    #include <fstream>
    #include <string>
    
    int main(void){
      std::ifstream infile; // Or infile.open("filepath")
      
      infile.open("filepath"); // Open file
      
      std::string some_text;
      infile >> some_text; // Store the next word from the file in some_text
      
      infile.close(); // Close the file
      
      return 0;
    }
    
Reading numbers and single characters from files is just as easy as reading whole words.

    infile >> num;
or
    infile >> character;
or
    infile >> double_number; // etc
    
Reading whole lines from a file can also be done with the following code:

    std::getline(infile, string_holder); // The line from the file is stored in string_holder using pass-by-reference
