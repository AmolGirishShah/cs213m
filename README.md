## Welcome!

### Difference between fstream and iostream
ofstream derives from ostream, the fstream header includes the iostream header, so you could leave out iostream and it would still compile. But you can't leave out fstream because then you don't have a definition for ofstream. fstream is needed for file operations

### More on fstream
fstream is another C++ standard library like iostream and is used to read and write on files.

These are the data types used for file handling from the fstream library:

Data type: 	Description</br>
ofstream: 	It is used to create files and write on files.</br>
ifstream: 	It is used to read from files.</br>
fstream: 	It can perform the function of both ofstream and ifstream which means it can create files, write on files, and read from files.</br>
Add fstream::out to make a txt file that doesnt exist while using file.open

### srand()

See Lec1 code for generating same/different random output

#include <time.h> </br>
time_t t;</br>
srand((unsigned) time(&t));

The srand() function in C++ seeds the pseudo random number generator used by the rand() function. The seed for rand() function is 1 by default.

It means that if no srand() is called before rand(), the rand() function behaves as if it was seeded with srand(1).

It is a good practice to seed the pseudo random number generator only once at the beginning of the program and before any calls of rand(). It should not be seeded every time we need to generate a new set of numbers.

The standard practice is to use the result of a call to time(0) as the seed. The time() function returns the number of seconds since 00:00 hours, Jan 1, 1970 UTC (i.e. the current unix timestamp). The value of seed changes with time. So every time we run the program, a new set of random number is generated.


### Random things
h >> 4 means h is multiplied by 2^4

friend ostream &operator <<(ostream &os,const B& B_obj)\
const B& B_obj vs B obj(Passing by value) : Saves expense of copying

Arrays are always passed by reference, so no extra care is required for passing an array.\
However, it is a safe and good practice for a caller to pass the size of the array as an
additional parameter by value.


### Pending questions
How to check large number of test cases for a program?
