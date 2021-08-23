# get_next_line
May it be a file, stdin, or even later a network connection, you will always need a way to read content line by line. It is time to start working on this function, which will be essential for your future projects. 


![Image alt](https://github.com/Sviridovamd/get_next_line/blob/master/get_next_line_logo.png)

This project is your very first project as a student at 42. You will need to recode a few functions of the C standard library as well as some other utility functions that you will use during your whole cursus. 

![Image alt](https://github.com/Sviridovamd/get_next_line/blob/master/get_next_line.png)


This project will not only allow you to add a very convenient function to your collection,
but it will also allow you to learn a highly interesting new concept in C programming:
static variables.

Mandatory part - Get_next_line
Function name get_next_line
Prototype char *get_next_line(int fd);
Turn in files get_next_line.c, get_next_line_utils.c,
get_next_line.h
Parameters File descriptor to read from
Return value Read line: correct behavior
NULL: nothing else to read or an error occurred
External functs. read, malloc, free
Description Write a function which returns a line read from a
file descriptor
• Calling your function get_next_line in a loop will then allow you to read the text
available on the file descriptor one line at a time until the end of it.
• Your function should return the line that has just been read. If there is nothing
else to read or if an error has occurred it should return NULL.
• Make sure that your function behaves well when it reads from a file and when it
reads from the standard input.
• libft is not allowed for this project. You must add a get_next_line_utils.c file
which will contain the functions that are needed for your get_next_line to work.
• Your program must compile with the flag -D BUFFER_SIZE=xx which will be used
as the buffer size for the read calls in your get_next_line. This value will be
modified by your evaluators and by the moulinette.
• The program will be compiled in this way:
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c.
• Your read must use the BUFFER_SIZE defined during compilation to read from
a file or from stdin. This value will be modified during the evaluation for testing
purposes.
• In the header file get_next_line.h you must have at least the prototype of the
function get_next_line.
Get Next Line Reading a line on a fd is way too tedious
Does your function still work if the BUFFER_SIZE value is 9999? And
if the BUFFER_SIZE value is 1? And 10000000? Do you know why?
You should try to read as little as possible each time get_next_line
is called. If you encounter a newline, you have to return the
current line. Don’t read the whole file and then process each line.
Don’t turn in your project without testing. There are many tests to
run, cover your bases. Try to read from a file, from a redirection,
from standard input. How does your program behave when you send a
newline to the standard output? And CTRL-D?
• lseek is not an allowed function. File reading must be done only once.
• We consider that get_next_line has undefined behavior if, between two calls, the
same file descriptor switches to a different file before reading everything from the
first fd.
• Finally we consider that get_next_line has undefined behavior when reading from
a binary file. However, if you wish, you can make this behavior coherent.
• Global variables are forbidden.
• Important: You should always return the line that has been read followed by a ’\n’
unless you have reach end of file and the is no ’\n’.
A good start would be to know what a static variable is:
https://en.wikipedia.org/wiki/Static_variable
