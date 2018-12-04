# _**Random Number Generators**_ #


#### Nim ####
Game starts with 23 objects and user removes 1, 2, or 3 objects at a time.
Computer or opponent can also remove 1-3 objects per round. The goal is to never always leave some objects at the end of your turn.


### Generating Random Numbers ###
A random number generated between ``0 and RANDMAX``. ``RANDMAX`` varies based on the
implementation but is guaranteed to be at least 32767. It may be required to include the <cstdlib> to run the random number generator.

_**To generate a number within a specific range use the following code:**_

    int randomNum = rand() % 10 // Generate a number 0-10

The random number generator is not random at all, so it is necessary to use a seed to mix up the random numbers. Use ``#include <ctime>`` library to seed the random number generator. time() function gets the current time.

_**Use the time to seed the gnerator:**_

    srand(time(NULL)); // seed random function uses the seed we proided for calc
                       // time(NULL) is time since 1970 in seconds

    // Call random function after seeding to get "random" numbers
    rand();
