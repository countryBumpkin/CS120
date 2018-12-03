# *Data Types and Memory:*

| Data Type | Size(Bytes) |    Range  |
| ---
|char    |   1 byte    | -127 to 127 or 0 to 255
|u char  |   1 byte    |  0 to 255
|s char  |   1 byte    | -127 to 127
|int     |   4 bytes   | -2,147,483,648 to 2,147,483,647
|u int   |   4 bytes   |  0 to 4294967295
|s int   |   4 bytes   | -2,147,483,648 to 2,147,483,647
|sh int  |   2 bytes   | -32,768 to 32,767
|u sh int|   ?Range?   |  0 to 65,535
|s sh int|   ?Range?   | -32,768 to 32,767
|l int   |   4 bytes   | -2,147,483,648 to 2,147,483,647
|s l int |   4 bytes   |  same as above
|u l int |   4 bytes   |  0 to 4,294,967,295
|float   |   4 bytes   | +/- 3.4e +/- 38 (~7 digits)
|double  |   8 bytes   | +/- 1.7e +/- 308 (~15 digits)
|l double|   8 bytes   | +/- 1.7e +/- 308 (~15 digits)
|wchar_t | 2 - 4 bytes | 1 wide character

|Key |
| ---
|u = unsigned
|s = signed
|l = long
|sh = short

## Initialization and Overflow Handling:
1. *Global and static variables are set to a value of 0 if not given a value when created.*

2. *Variables that are members of functions are given whatever random value is stored in the memory address it is assigned.*

3. *When a variable exceeds the max memory allocation of the data type the excess is called overflow. The variable is reset, to 0(see example below), and assigned the value of max_data_val - variable_value(the overflow)*

If largest number of data type is exceeded, the variable is reset to 0.
example:
short int excess = 32767; //Max positive value of int data type
excess++; //Increment excess by one
std::cout << excess << std::endl; //Prints 0


## Program Data Usage Example:
If the following variables are initialized in a program, what is the minimum amount
of memory required for the program to run?

min(int) = 4 bytes
max(int) = 4 bytes
temp_value(float) = 4 bytes
max_value(double) = 8 bytes
char_1(char) = 1 byte
current_num(const int) = 4 bytes
PI(double) = 8 bytes

Therefore, the memory size required is:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Total Program Memory Usage: 33 bytes |
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Remember, 1 Byte = 8 bits, therefore 4 bytes = 32 bits or 8^31

## Misc Notes:
Const Keyword: *cannot be changed after initialization*
