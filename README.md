## Welcome!

### Difference between fstream and iostream
ofstream derives from ostream, the fstream header includes the iostream header, so you could leave out iostream and it would still compile. But you can't leave out fstream because then you don't have a definition for ofstream. fstream is needed for file operations
