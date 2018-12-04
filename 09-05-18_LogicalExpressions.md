# *Logical Expressions*
* Precedence
* C++ Keywords

## Precedence:
|Precedence| Logical Expression|
| --- | --- |
|5  | 	a*b   a/b   a%b 	Multiplication, division, and remainder
|6  | 	a+b   a-b 	Addition and subtraction
|7  | 	<<   >> 	Bitwise left shift and right shift
|8  | 	<=> 	Three-way comparison operator (since C++20)
|9  | 	<   <= 	For relational operators < and ≤ respectively >  |  >= 	For relational operators > and ≥ respectively
|10 | 	==   != 	For relational operators = and ≠ respectively
|11 | 	& 	Bitwise AND
|12 | 	^ 	Bitwise XOR (exclusive or)
|13 | || 	Bitwise OR (inclusive or)
|14 |	&& 	Logical AND
|15 |	|| 	Logical OR
|16 |	a?b:c 	Ternary conditional[note 2] 	Right-to-left
|throw | 	throw operator
|= 	| Direct assignment (provided by default for C++ classes)
|+=   -= |	Compound assignment by sum and difference
|*=   /=   %= |	Compound assignment by product, quotient, and remainder
|<<=   >>= 	| Compound assignment by bitwise left shift and right shift
|&=   ^=   |= 	| Compound assignment by bitwise AND, XOR, and OR

      Examples:
        x and y are greater than z          => x > z && y > z
        x is equal to 1.0 or 3.0            => x == 1.0 || x == 3.0
        x is in the range z to y, inclusive => x >= z && x <= y
        x is outside the range z to y       => x < z || x > y

#### Note:
  if a = 100,
  a == 100 && !a => false, any nonzero number will be evaluated as true


## Misc Keywords:
|Keyword | Description|
|--- | --- |
|new | Used to add allocate storage to a variable, most commonly an array. This can be risky because the memory is not destructed until a matching delete-expression.
|delete| Used to deallocate memory
      Example:
          char* ptr = new char[sizeof(T)]; // allocate memory
          T* tptr = new(ptr) T;            // construct in allocated storage ("place")
          tptr->~T();                      // destruct
          delete[] ptr;                    // deallocate memory

