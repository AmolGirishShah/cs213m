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

### Converting int to string
`#include <string> 
std::string s = std::to_string(42);
`
is therefore the shortest way I can think of. You can even omit naming the type, using the auto keyword:
`
auto s = std::to_string(42);

# Advanced Python concepts
more complex list comprehensions</br>
map, filter, and reduce with lambdas </br>
locals and globals</br>
context managers</br>
decorators and class decorators</br>
generators</br>
https://blog.usejournal.com/python-from-intermediate-to-superhero-1a86e518bb77

There are various ways to remove spaces from a string in Python. This tutorial is aimed to provide a short example of various functions we can use to remove whitespaces from a string.</br>
Python String is immutable, so we can’t change its value. Any function that manipulates string value returns a new string and we have to explicitly assign it to the string, otherwise, the string value won’t change.</br>
`s = '  Hello  World   From Pankaj \t\n\r\tHi There  ' `</br>Python String strip() function will remove leading and trailing whitespaces.If you want to remove only leading or trailing spaces, use lstrip() or rstrip() function instead.
</br>`>>> s.strip()
'Hello  World   From Pankaj \t\n\r\tHi There'
`</br>We can use replace() to remove all the whitespaces from the string. This function will remove whitespaces between words too.
</br>`>>> s.replace(" ", "") 
'HelloWorldFromPankaj\t\n\r\tHiThere'`
</br>If you want to get rid of all the duplicate whitespaces and newline characters, then you can use join() function with string split() function.
</br>`>>> " ".join(s.split())
'Hello World From Pankaj Hi There'`</br>
If you want to get rid of all the whitespaces as well as newline characters, you can use string translate() function.</br>
`>>> import string </br>`
`>>> s.translate({ord(c): None for c in string.whitespace})
'HelloWorldFromPankajHiThere'`

</br>Python Remove Whitespaces from String using Regex
We can also use a regular expression to match whitespace and remove them using re.sub() function.</br>
Ref: https://www.journaldev.com/23763/python-remove-spaces-from-string




### Random things
h >> 4 means h is multiplied by 2^4

friend ostream &operator <<(ostream &os,const B& B_obj)\
const B& B_obj vs B obj(Passing by value) : Saves expense of copying

Arrays are always passed by reference, so no extra care is required for passing an array.\
However, it is a safe and good practice for a caller to pass the size of the array as an
additional parameter by value.


### Pending questions
How to check large number of test cases for a program?
