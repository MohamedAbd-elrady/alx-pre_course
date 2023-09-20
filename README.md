# 0x11. C - printf
## _printf()
> In this project, we recreated our custom virsion of the `printf` function found
> in the `stdio.h` library in the C programming language. This function allows
> us to print any argument given to the terminal and similar printing functions
> can be found in any programming language. This means we can print any combinations
> of strings, intergers, and other different data types.

### Synopsis
> This repository holds all the code necessary for our custom `_printf`
> function to run. Our custom virsion currently handles conversion specifiers:
> `c`, `s`, `%`, `d`, `i`, `b`, `u`, `o`, `x`, `X`, , `p`, `r`, `R` and does not
> yet support field width, precision, flag characters, or length modifiers. Unique
> to our `_printf` is our `S` for printing non-printable in hexa after `\x`, `r`
> reverse conversion and the `R` rot13 conversion. In essence, you can print any
> character, string, integer, or decimal number, print non-printable, reverse your
> strings, transform any number to binary and octal bases, and encrypt your string
> with rot13 encryption.

### Description of what each file shows:
```
man_3_printf ----------------------- custom manpage for custom _printf function
_prinf.c --------------------------- holds custom _printf main function
main.h ----------------------------- holds prototypes of functions spread across all files
printf_helper.c -------------------- holds get_type, create_buffer and buffer_overflow to help with functionality
printf_tools.c --------------------- holds custom-made _strlen, _write_buffer, _memcpy function to deal with buffer
printf_functions.c ----------------- handles %s to print a string of characters, %c to print a single character and %%
printf_binary.c -------------------- handles %b to convert numbers passed into base 2
printf_integers.c ------------------ handles %d, %i, %u to print (d)ecimal/(i)ntegers in base 10
printf_hexadecimal.c --------------- handles %x, %X convert numbers passed into in base 16
printf_octal.c --------------------- handles %o to convert numbers passed into base 8
printf_memory_address.c ------------ 
printf_string_manipulator.c -------- handles %R to move each character 13 alphabet letters down, %r to reverse string and %S for non-printable
```
### Environment
* Language: C
* OS: Ubuntu 20.04 LTS
* Compiler: gcc 9.4.0
* Style guidelines: [Betty style](https://github.com/alx-tools/Betty/wiki)

### How To Install & Compile
```
(terminal)$ git clone https://github.com/MohamedAbd-elrady/printf.git
(terminal)$ cd printf
```
Sample main program inside print.c:
```
int main(void)
{
	_printf("%s %ch%dre", "Hi", "T", 3);
	return (0);
}
====================================
(terminal)$ gcc -Wall -Werror -Wextra -pedantic -Wno-format *.c -o print
(terminal)$ ./print
Hi Th3re
(terminal)$
```

### To Do

##### mandatory
- [x] bulid main structure and handle `%c`, `%s`, `%%`
- [x] handle `%d`, `%i`

##### advanced
- [x] handle `%b`
- [x] handle `%u`, `%o`, `%x`, `%X`
- [x] Use a local buffer of `1024` chars in order to call `write` as little as possible.
- [x] handle `%S`
- [x] handle `%p`
- [ ] handle `+`, space, `#` flags
- [ ] handle `l`, `h` flags for `%d`, `%i`, `%u`, `%o`, `%x`, `%X`
- [ ] handle width
- [ ] handle precision
- [ ] handle `0` flag
- [ ] handle `-`
- [x] handle `%r`
- [x] handle `%R`
- [ ] Make sure all the above options work well together.

---
### Authors
- Mohamed Abd-elrady [Linkedin](https://www.linkedin.com/in/mohamed-abd-elrady-mosa/)
- Mohamed khaled [Linkedin](https://www.linkedin.com/in/mohamed-k-kamal/)
