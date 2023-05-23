# Hello World

> commands to know `gcc` `printf` `puts` `putchar`
<br/>

> 0. Write a script that runs a C file through the preprocessor and save the result into another file : **Preprocessor**
> - The C file name will be saved in the variable $CFILE
> - The output should be saved in the file c
>```console
> gcc -E $CFILE -o c
>```  
>```console
> cpp $CFILE c
>``` 
<br/>

> 1. Write a script that compiles a C file but does not link : **Compiler**
> - The C file name will be saved in the variable $CFILE
> - The output file should be named the same as the C file, but with the extension `.o` instead of `.c`.
>   - Example: if the C file is `main.c`, the output file should be `main.o`
>```console
> gcc -c $CFILE
>```   
<br/>

> 2. Write a script that generates the assembly code of a C code and save it in an output file. : **Assembler**
> - The C file name will be saved in the variable $CFILE
> - The output file should be named the same as the C file, but with the extension `.s` instead of `.c`.
>   - Example: if the C file is `main.c`, the output file should be `main.s`
>```console
> gcc -S $CFILE
>```   
<br/>

> 3. Write a script that compiles a C file and creates an executable named cisfun.
> - The C file name will be saved in the variable $CFILE
>```console
> gcc $CFILE -o cisfun
>```
>```console
> gcc -o cisfun $CFILE
>``` 
<br/>

> 4. Write a C program that prints exactly "Programming is like building a multilingual puzzle, followed by a new line.
> - Use the function `puts`
> - You are not allowed to use `printf`
> - Your program should end with the value 0
>   - Example: if the C file is `main.c`, the output file should be `main.o`
>```c
> #include <stdio.h>
> 
> /**
>  * main - Prints "Programming is like building a multilingual puzzle
>  *
>  * Return: 0 if the program executes successfully
>  */
> int main(void)
> {
> 	puts("\"Programming is like building a multilingual puzzle");
> 	return (0);
> }
>```   
<br/>

> 5. Write a C program that prints exactly with proper grammar, but the outcome is a piece of art,, followed by a new line.
> - Use the function `printf`
> - You are not allowed to use `puts`
> - Your program should return `0`
> - Your program should compile without warning when using the `-Wall gcc` option
>```c
> #include <stdio.h>
> 
> /**
>  * main - Prints "with proper grammer, but the outcome is a piece of art,"
>  *
>  * Return: 0 if the program executes successfully
>  */
> int main(void)
> {
> 	printf("with proper grammar, but the outcome is a piece of art,\n");
> 	return (0);
> }
>```   
<br/>

> 6. Write a C program that prints the size of various types on the computer it is compiled and run on.
> - You should produce the exact same output as in the example
> - Warnings are allowed
> - Your program should return `0`
> - You might have to install the package `libc6-dev-i386` on your Linux to test the `-m32` `gcc` option
>```c
> #include <stdio.h>
> 
> /**
>  * main - Prints the size of various types
>  * on the computer this file is compiled and run on
>  *
>  * Return: 0 if the program executes successfully
>  */
> int main(void)
> {
> 	printf("Size of a char: %li byte(s)\n", sizeof(char));
> 	printf("Size of an int: %li byte(s)\n", sizeof(int));
> 	printf("Size of a long int: %li byte(s)\n", sizeof(long int));
> 	printf("Size of a long long int: %li byte(s)\n", sizeof(long long int));
> 	printf("Size of a float: %li byte(s)\n", sizeof(float));
> 	return (0);
> }
>```   
<br/>

> 7. Write a script that generates the assembly code (Intel syntax) of a C code and save it in an output file.
> 
> - The C file name will be saved in the variable $CFILE.
> - The output file should be named the same as the C file, but with the extension `.s` instead of `.c`.
>   - Example: if the C file is `main.c`, the output file should be `main.s`
> ```console
> gcc -S -masm=intel $CFILE
> ```
<br />

> 8. Write a C program that prints exactly and that piece of art is useful" - Dora Korpar, 2015-10-19, followed by a new line, to the standard error.
> 
> - You are not allowed to use any functions listed in the `NAME` section of the man (3) `printf` or man (3) `puts`
> - Your program should return `1`
> - Your program should compile without any warnings when using the `-Wall gcc` option  
> NB: this solution is betty compliant -> 101-quote.c:12 WARNING: quoted string split across lines
> ```c
> #include <stdio.h>
> 
> /**
>  * main - Prints "and that pice of art is useful
>  * - Dora Korpar, 2015-10-19"
>  *
>  * Return: 0 if the program executes successfully, 1 if errors
>  */
> int main(void)
> {
> 	fprintf(stderr, "and that piece of art is useful\" - "
> 			"Dora Korpar, 2015-10-19\n");
> 	return (1);
> }
> ```
