# Printf

This project is about writing our own version of the printf function in C programming language. The function, which will be called _printf in this project, will be capable of printing a variety of formats such as strings, characters, integers, decimals, and special characters to the standard output.

## Authorized functions and macros

The following functions and macros are authorized for use in this project:

  - write (man 2 write)
  - malloc (man 3 malloc)
  - free (man 3 free)
  - va_start (man 3 va_start)
  - va_end (man 3 va_end)
  - va_copy (man 3 va_copy)
  - va_arg (man 3 va_arg)

## Compilation

The code will be compiled using the following flags:

$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 -Wno-format *.c

Be careful not to push any C file containing a main function in the root directory of the project. You can have a test folder containing all your test files, including main functions.

The main files will include your main header file (main.h):

  **#include main.h**
  
You might want to look at the gcc flag -Wno-format when testing your _printf function with the standard printf.


## Function Prototype

The prototype for the _printf function is:

  - **int _printf(const char *format, ...);***

The function returns the number of characters printed (excluding the null byte used to end output to strings) and writes output to stdout, the standard output stream.

The format argument is a character string. The format string is composed of zero or more directives. See man 3 printf for more detail.

## Conversion Specifiers to Handle

The following conversion specifiers need to be handled:

  - c
  - s
  - %
  - d
  - i
  - u
  - o
  - x
  - X
  - p

The c, s, and % conversion specifiers are standard and are included in the C library printf function. The remaining conversion specifiers need to be implemented.

The following features do not need to be handled for any conversion specifier:

  - Flag characters
  - Field width
  - Precision
  - Length modifiers


## Custom Conversion Specifiers

The following custom conversion specifier needs to be handled:

  - b: the unsigned int argument is converted to binary
  - S: prints the string. Non-printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters)
  - r: prints the reversed string
  - R: prints the rot13'd string

## Flags and Length Modifiers to Handle

The following flag characters need to be handled for non-custom conversion specifiers:

  - +
  - space
  - \#

The following length modifiers need to be handled for non-custom conversion specifiers:

  - l
  - h

Authors:

:computer: Aranza B

:computer: Emilio S.

:computer: Diego E.

:computer: Josue H.

:computer: Mateo Q.
